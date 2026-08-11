# Seedance 2.0 — prompt formula

Advanced packaging for Seedance 2.0.

**Target:** 2.0 only. Do not mix with the 2.5 six-slot set.

## Light

Job: make intent legible as a shot brief — not a novel synopsis.

Contract: **精准主体 + 动作细节** required. Scene / light / camera / style / quality / constraints optional. Empty axis = model default.

Must-not-break:
- Do not paste a full screenplay as the prompt
- Do not restate the same action twice
- Duration / aspect / resolution → host UI (may also appear as constraint words; don’t fight the panel)
- Competing style + camera adjectives → mush
- Two–few clear sentences beat a stuffed paragraph

## Normal

### Advanced packaging (order)

| # | Slot (CN / EN) | Controls | Required? |
|---|----------------|----------|-----------|
| 1 | **精准主体** / Subject | Who/what; countable; stable tags | Yes (with 2) |
| 2 | **动作细节** / Action | Visible process; body + speed/force | Yes |
| 3 | **场景环境** / Scene | Place, spatial relationships | Optional |
| 4 | **光影色调** / Light & tone | Direction, quality, grade | Optional |
| 5 | **镜头运镜** / Camera | Size, move, cut join | Optional |
| 6 | **视觉风格** / Visual style | Look / materials / genre look | Optional |
| 7 | **画质** / Quality | Clarity / filmic finish words | Optional |
| 8 | **约束条件** / Constraints | No subs / logo / watermark; targeted bans | Optional |

Per-shot write order when staging beats : ① camera or cut → ② subject action/expression → ③ position/spatial change → ④ audio.

### Paste template — short clip (~4–8s)

```
[SUBJECT] [main visible action] in [SCENE].
Light/tone: [direction + quality + grade].
Camera: [SHOT SIZE], [one MOVE or locked-off]; keep [subject] [screen position].
Audio: [ambience / FX / dialogue] — see seedance-audio-and-refs.md for brackets.
Constraints: [only real risks — identity, prop count, no subs, no logos].
```

### Paste template — multi-shot (~8–15s)

```
[GOAL]
Core subject: [NAME]. Main event: [one sentence physical summary]. Length: [host duration ≤15s typical].

[REFERENCES]  (if any — see seedance-audio-and-refs.md)
@Image1 / 图片1: [role]. Do not copy [bleed].
@Video1 / 视频1: [role]. Do not copy [bleed].

[SUBJECT + EVENT]
[Who] [does what] in [scene].

[ENVIRONMENT + LIGHT + STYLE]
[Location, geography, light, materials, mood, quality words.]

[SEQUENCE — Shot N, not forced seconds]
Shot 1 / 镜头1: [camera] · [action] · [spatial change] · [audio]. Ends: [visible state].
Shot 2 / 镜头2: Carried over: [state]. [camera] · [one change]. Ends: [visible state].
Shot 3 / 镜头3: Closing. Ends: [final picture state].

[KEEP CONSISTENT]
[Identity, headcount, clothing, prop ownership, spatial orientation.]

[CONSTRAINTS]
[Targeted: 保持无字幕 / no logos / no duplicate props / …]
```

### Slot → what to write

| Slot | Prefer | Avoid |
|------|--------|-------|
| Subject | Named count + stable label | Vague “people”, “cinematic someone” |
| Action | Ordered contacts; limb + speed/force | Abstract “drama unfolds” |
| Scene | Exits, depths, left/right of frame | Tourist postcard with no geography |
| Light | Direction + quality + what it hits | “Moody” alone |
| Camera | Standard terms; **one move per shot** | Stacked push+pan+tilt+orbit |
| Style / quality | Concrete look + finish | “Epic / beautiful” alone |
| Constraints | Short, targeted | Giant negative laundry lists |

### Lighting / style clauses that steer

| Phrase pattern | Effect |
|----------------|--------|
| Warm low sun from behind-left; long shadows | Golden-hour directionality |
| Bright even daylight from tall windows left | Clean commercial look |
| Flickering streetlight; wet asphalt reflections | Night rain without “moody” alone |
| Shallow DOF; subject eyes sharp; bg soft | Portrait isolation |
| Soft overhead museum light; pale wood floors | Environment + soft key |

Prefer **direction + quality + what it hits** over named LUT brands (**Uncertain** transfer).

## Hard

**Emotion as performance** — externalize as body detail, not abstract mood words (eyes to door, shoulders tighten, pause before handle).

**Motion as physics** — direction, distance, speed, contact, settle; prefer low continuous motion over stacked high-burst stunts when stability matters.

**Cause before reaction** — contact → resulting motion → sound → look/react.

**Iterate one axis** — if 90% works, change only the failing clause.

| Failure | Fix |
|---------|-----|
| Generic floaty clip | Name shot first: “缓慢推镜” / “固定镜头” |
| Mush look | Drop competing style+camera adjectives |
| Prompt ignored late | Cut length; tighten before you add |
| Params fighting UI | Align duration/aspect with host panel |

**Uncertain:** exact character-retention ceiling by host; treat “tighten before you add” as operational.
