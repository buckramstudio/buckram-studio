# Seedance 2.5 — prompt formula

Six-slot grammar for Seedance 2.5. Fill only slots you need to control.

**Target:** 2.5 only. Do not mix with the 2.0 advanced-packaging set.

## Light

Job: make intent legible as a shot brief — not a novel synopsis.

Contract: **Subject + Action** required. Scene / Style / Camera / Audio optional. Empty slot = model default.

Must-not-break:
- Slot order when filling multiple slots (helps the model parse)
- Do not restate the same action twice
- Do not put UI params (duration, aspect, resolution) in the prompt — set those in the host
- Competing style + camera adjectives → mush; pick one intent per axis
- Two–few clear sentences beat a stuffed paragraph

## Normal

### Six slots (order)

Six-slot order for 2.5.

| # | Slot | Controls | Required? |
|---|------|----------|-----------|
| 1 | **Subject** | Who/what is in frame (named, countable) | Yes (with 2) |
| 2 | **Action or event** | Visible process over time | Yes |
| 3 | **Scene and environment** | Place, time, weather, spatial relationships | Optional |
| 4 | **Visual style** | Light, color, materials, texture, grade/mood | Optional |
| 5 | **Camera movement or cut** | Shot size, position, move, focus, joins | Optional |
| 6 | **Audio** | Dialogue, timbre, ambience, FX, music (or silence) | Optional |

Macro → micro : plan 30s arc → organize refs by role → time-based sections → structure pass before detail.

### Paste template — short clip (~4–8s)

```
[DURATION / FORMAT note for you, not always needed in prompt]
[single take | cuts] · [real-time speed]

[SUBJECT] [main visible action] in [SCENE: place, time, spatial layout].
Visuals: [STYLE: light direction/quality, grade, materials, DOF].
Camera: [SHOT SIZE], [ANGLE], [MOVE or locked-off]; keep [subject] [screen position].
Audio: [ambience / contact sounds / dialogue or "no music"].
Constraints: [only real risks — identity, prop count, no cuts, no extras].
```

### Paste template — ~15–30s staged

```
[GOAL]
Generate a [video type]. Core subject: [NAME]. Main event: [one sentence physical summary].

[REFERENCES]  (if any — see seedance-audio-and-refs.md)
@Image1: [role]. Do not copy [bleed].
@Video1: [role]. Do not copy [bleed].

[SUBJECT + EVENT]
[Who] [does what] in [scene].

[ENVIRONMENT + STYLE]
[Location, geography, light, materials, mood.]

[CAMERA]
[Size, angle, move OR cut plan; screen-space position; when move starts/stops.]

[SEQUENCE]
0–Xs: [one primary change + camera + sound]. Ends: [visible state].
X–Ys: Carried over: [state]. Event: [one change]. Ends: [visible state].
Y–Zs: Closing event. Ends: [final picture state].
End state: [character positions, prop ownership, camera].

[KEEP CONSISTENT]
[Identity, headcount, clothing, prop ownership, spatial orientation, axis.]

[CONSTRAINTS]
[Targeted: no cuts / no slow-mo / no duplicate props / no logos / …]
```

### Slot → what to write (camera/stage focus)

| Slot | Prefer | Avoid |
|------|--------|-------|
| Subject | Named count: “one messenger”, “the same red helmet” | Vague “people”, “someone cinematic” |
| Action | Ordered contacts: approach → contact → result → settle | Abstract “drama unfolds” |
| Scene | Exits, depths, left/right of frame, what stays fixed | Tourist postcard with no geography |
| Style | Light direction + quality + grade + DOF | “Cinematic”, “epic”, “beautiful” alone |
| Camera | Crew terms + who it follows + start/end | “Dynamic camera”, stacked conflicting moves |
| Audio | Mix next to the event that causes it | Paragraph of unused foley |

### Lighting / style clauses that steer

| Phrase pattern | Effect |
|----------------|--------|
| Warm low sun from behind-left; long shadows | Golden-hour directionality |
| Bright even daylight from tall windows left | Clean commercial / gym look |
| Flickering streetlight; wet asphalt reflections; fine rain in beam | Night rain mood without “moody” alone |
| Shallow DOF; subject eyes sharp; background soft bokeh | Portrait isolation |
| Clean commercial grade / teal-amber night grade / warm 35mm film, soft halation | Color/texture register |
| Soft overhead museum light; pale wood floors | Environment material + soft key |

Prefer **direction + quality + what it hits** over named LUT brands (**Uncertain** transfer). Numeric f-stop/focal length OK but **visible result** is clearer than the number alone.

### Five-layer note (shot-led packaging)

Some hosts teach **shot · subject · action · light · audio**. Compatible with the six-slot formula: lead with shot when camera must win; still separate subject action from camera move.

## Hard

**Emotion as performance** — not “she is nervous”; eyes to door, shoulders tighten, pause before handle. (Guide-mirror craft; consistent with Seed physical performance examples.)

**Motion as physics** — direction, distance, speed, contact, recovery/settle.

**Cause before reaction** — contact → resulting motion → sound → look/react.

**Iterate one axis** — if 90% works, change only the failing clause.

| Failure | Fix |
|---------|-----|
| Generic floaty clip | Name shot first: “slow dolly-in” / “static locked-off” |
| Mush look | Drop competing style+camera adjectives |
| Prompt ignored late | Cut length; past a few hundred strong words clauses drop |
| Params in prose | Move duration/aspect/resolution to UI |

**Uncertain:** exact character-retention ceiling varies by host; treat “tighten before you add” as operational, not a hard word count.
