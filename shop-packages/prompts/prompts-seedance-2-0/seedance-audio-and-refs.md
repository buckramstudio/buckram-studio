# Seedance 2.0 — audio brackets & reference roles

Audio syntax and numbered / `@` asset binding for **stage feel and consistency**.

**Target:** 2.0 only. Asset ceilings below are **not** the 2.5 “50 file” pack.

## Light

Job: route sound/text channels cleanly; give every reference **one job** (+ exclusions).

Contract: natural language works alone; brackets disambiguate when music/FX/dialogue/subs compete.

Must-not-break:
- Dialogue language/delivery **before** the line; only spoken words inside `{ }`
- `{dialogue}` ≠ on-screen text — repeat in `【 】` if both needed
- Every asset: what to take **and** what not to take
- One subject/prop ↔ one primary defining file
- Don’t force every asset on screen at once
- Put the **most identity-critical** refs early

## Normal

### Bracket syntax (audio / text)

Full-width `（）` also appears in CN docs; half-width `( )` is fine in English prompts.

| Bracket | Routes to | Example |
|---------|-----------|---------|
| `( )` / `（）` | Music / ambient beds | `(low cello drone)` |
| `< >` / `<>` | Sound effects | `<a bell rings in the distance>` |
| `{ }` | Spoken dialogue | `{We should go.}` |
| `【 】` | On-screen subtitles | `【Chapter One: Departure】` |

Keep FX short and physical. Two–three concrete effects beat a foley essay.

### Prose audio (also valid)

`Audio: rain outside, door bell, cooler hum, footsteps, bottle on counter, no music.`

Put sound **next to the event** that causes it in Shot N.

### Useful negatives (end of prompt)

| Phrase | Use |
|--------|-----|
| 保持无字幕 / No subtitles | Stop burned-in captions |
| No background music / No BGM | Strip score |
| 不要生成Logo / 不要生成水印 | Stage cleanliness |
| No audio / No sound | Mute (or host audio toggle) |

### Dialogue performance

```
Dialogue language: [language + regional variant].
[Speaker] says [delivery]: {line}
Mouth moves only during own lines.
[Other] keeps mouth closed.
```

Non-Chinese lines: name language explicitly before `{ }`.

### Reference tags & roles

Numbering follows **upload order**.

| Tag | Typical roles |
|-----|----------------|
| `@Image` / 图片N | Identity, wardrobe, product, environment layout/light |
| `@Video` / 视频N | Camera path, performance rhythm, timing, effects |
| `@Audio` / 音频N | Voice timbre, line, ambience, music feel |

#### Role templates

```
@Image1 / 图片1 controls only [identity | product | wardrobe | environment].
Do not copy [pose, background, lighting, text, camera angle].

@Video1 / 视频1 controls only [camera path | performance | motion rhythm | timing].
Do not copy [subject, wardrobe, objects, setting].

@Audio1 / 音频1 defines [character/sound]'s [voice | line | ambience | music].
```

#### Multi-view same **object** (OK)

```
@Image1–@Image4 define front/left/right/back of ONE [object].
Only one [object] exists in the finished video.
```

Prefer **separate angle files**, not one collage grid.

#### People / identity refs

Prefer **face close-up (大头照) + full-body**, with clear “face from Image N / wardrobe from Image M”.

**Do not** feed a person multi-view / three-view sheet — the model may treat angles as different people (ID drift). Same for collages that bury a small face.

Put the most precise identity asset **earlier** in the prompt.

### Asset budgets (2.0)

| Guidance | Cap / habit |
| ---------- | ------------- |
| Combined refs | About **~12** combined — lighter packs |
| Practice pack | ~1–2 face/body + 1 scene + optional motion video + optional audio |
| Don’t max the slot | Competing refs blur priority |

Do **not** copy 2.5’s 30/10/10 / ≤50 ceilings into 2.0 prompts.

### Don’t make image + video do the same job

- Image → look / identity / product
- Video → motion / camera / timing
State exclusions so wrong set leaks don’t land.

### When reference video already has the choreography

Inherit motion/camera/order; **do not** restate move-by-move. Still write final subject, scene, style in text if needed.

## Hard

**Edit master pattern:** declare sole video master; narrow edit scope; list preserved content. Prefer direct edit address over “reference” phrasing.

**Parameter locks** — host-dependent; confirm on surface:

| Task | Often locks |
|------|-------------|
| Video editing | Aspect + ~duration of input |
| Extension | Aspect to input; duration freer; audio level may drift |

| Failure | Fix |
|---------|-----|
| Wrong voice / language | Language + accent + delivery before `{ }` |
| Subs appear unwanted | `保持无字幕` / `No subtitles` |
| Music fights FX | `( )` vs `< >`; or No BGM |
| Ref bleeds bg/pose | Explicit “Do not copy …” |
| Identity mashup / multi-view person | Face+body only; one file per subject |
| Upload order mismatch | Re-check N against upload sequence |

**Uncertain:** bracket obedience vs prose `Audio:` by build; exact `@` spacing is host-specific.
