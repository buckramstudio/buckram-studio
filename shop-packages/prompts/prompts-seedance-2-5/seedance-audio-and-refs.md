# Seedance 2.5 — audio brackets & reference roles

Audio syntax and `@` asset binding — for **stage feel and consistency**, not score composition craft.

**Target:** 2.5 only. 30/10/10 ceilings and clay tags are 2.5 — do not copy into 2.0 jobs.

## Light

Job: route sound/text channels cleanly; give every reference **one job** (+ exclusions).

Contract: natural language works alone; brackets disambiguate when music/FX/dialogue/subs compete.

Must-not-break:
- Dialogue language/delivery **before** the line; only spoken words inside `{ }`
- `{dialogue}` ≠ on-screen text — repeat in `【 】` if both needed
- Every `@` asset: what to take **and** what not to take
- One subject/prop ↔ one primary defining file
- Don’t force every asset on screen at once — invoke per scene
- Organize refs by role (character / product / scene / camera / audio)

## Normal

### Bracket syntax (audio / text)

Bracket syntax for 2.5 audio/text routing.

| Bracket | Routes to | Example |
|---------|-----------|---------|
| `( )` / `（）` | Music / ambient beds | `(low cello drone)` `(sparse piano)` |
| `< >` | Sound effects | `<a bell rings in the distance>` |
| `{ }` | Spoken dialogue | `{We should go.}` |
| `【 】` | On-screen subtitles | `【Chapter One: Departure】` |

Keep FX short and physical. Two–three concrete effects beat a foley essay.

### Prose audio (also valid)

Hosts accept an `Audio:` clause without brackets:

`Audio: rain outside, door bell, cooler hum, footsteps, bottle on counter, one card-reader beep, quiet store room tone, no music.`

Put sound **next to the event** that causes it in timed stages.

### Useful negatives (end of prompt)

| Phrase | Use |
| -------- | ----- |
| No background music / No BGM; keep only dialogue, ambience, action effects | Strip score |
| No subtitles | Stop burned-in captions |
| No audio at all / No sound | Mute (or host `generate_audio: false`) |
| No logos, no readable text | Stage cleanliness |

### Dialogue performance (stage feel)

```
Dialogue language: [language + regional variant].
[Speaker] says [delivery]: {line}
Mouth moves only during own lines.
[Other] keeps mouth closed.
```

Non-Chinese lines: name language explicitly before `{ }`. multi-language prompting for localized variants.

### Reference tags & roles

Numbering follows **upload order**. Use `@Image N`, `@Video N`, `@Clay Render N`.

| Tag | Typical roles |
|-----|----------------|
| `@Image` / `@Image1` | Identity, wardrobe, product geometry, environment layout/light, last-frame continuity |
| `@Video` / `@Video1` | Camera path, performance rhythm, timing, coarse/fine blockout, edit master |
| `@Audio` / `@Audio1` | Voice timbre, specific line, ambience bed, music feel |
| `@Clay Render` | Spatial structure, poses, paths, camera (2.5) |

#### Role templates

```
@Image1 controls only [identity | product | wardrobe | environment].
Do not copy [pose, background, lighting, text, camera angle] from @Image1.

@Video1 controls only [camera path | performance | motion rhythm | timing].
Do not copy [subject, wardrobe, objects, setting] from @Video1.

@Audio1 defines [character/sound]'s [voice | line | ambience | music].
```

#### Multi-view same **object** (OK)

```
@Image1–@Image4 define front/left/right/back of ONE [object].
Only one [object] exists in the finished video.
```

Prefer **separate angle files**, not one collage grid.

#### People / identity refs

prefer **face close-up + full-body**, clear “face from Image N / wardrobe from Image M”. **Do not** feed a person multi-view sheet (ID drift).

#### Per-scene invocation

Name subjects → group by type (people / props / scenes / action+sound) → each scene lists **Uses / Event / Ends**. role-layered packs beat dumping files.

### Asset budgets (2.5)

Up to **30 images, 10 video, 10 audio** per pass. Also useful: smaller **stability** ranges (not hard API caps).

| Type | Hard cap | Stability range |
|------|--------------|----------------------------------|
| Images | up to 30 (≤4K each) | ~1–8 distinct subjects |
| Video | up to 10; ~30s combined | ~1–5 subjects; ~5–10s each |
| Audio | up to 10; ~30s combined | only what the task needs |
| Total | ≤50 files | fewer is stabler |

50 is a ceiling, not a target. Prefer fewer distinct subjects.

### Don’t make image + video do the same job

- Image → look / identity / product
- Video → motion / camera / timing
State exclusions so skater/cone/beach don’t leak into the car shot.

### When reference video already has the choreography

Inherit motion/camera/order; **do not** restate move-by-move. Still write final subject, scene, style in text if the ref is a white-box.

## Hard

**Edit master pattern** : `Edit @Video 1…` / keep characters/actions/style; change only the named scope (e.g. camera plan by timestamp). Prefer direct address over vague “reference” phrasing for edit tasks (prefer direct address).

**Clay / white-model refs** : `@Clay Render` for camera path, blocking, trajectories; pair with style/identity images; map each grey solid → final subject.

**Parameter locks** :

| Task | Often locks |
|------|-------------|
| Video editing | Aspect + ~duration of input |
| First / first+last frame | Aspect to first image; duration freer |
| Extension | Aspect to input; duration freer; audio level may drift |

| Failure | Fix |
|---------|-----|
| Wrong voice / language | Language + accent + delivery before `{ }` |
| Subs appear unwanted | `No subtitles` |
| Music fights FX | Use `( )` vs `< >`; or `No BGM` |
| Ref bleeds bg/pose | Explicit “Do not copy …” |
| Identity mashup | One file per subject; named binding |
| Upload order mismatch | Re-check `@ImageN` against upload sequence |
| 50-file mush | Cut distinct subjects; role-layer the pack |

**Uncertain:** bracket obedience strength vs prose `Audio:` varies by build; if brackets fail, fall back to labeled prose. Exact `@` spacing is host-specific.
