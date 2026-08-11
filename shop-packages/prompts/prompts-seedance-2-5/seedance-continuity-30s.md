# Seedance 2.5 — continuity (~30s) & stitch handoff

Stages, **timestamps**, end states, and how to make clips joinable.

**Target:** 2.5 only. Do **not** use 2.0’s Shot-N-prefer / avoid-seconds default from the other version pack.

## Light

Job: give long generations a **place to land** every few seconds so motion budget doesn’t collapse.

Contract: each stage = **one primary change** + **visible end state**. Next stage opens from that state.

Must-not-break:
- Stages continuous; no overlapping time windows
- End state = on-screen observable (positions, props, camera) — not emotional summary
- `[KEEP CONSISTENT]` / continuity block for identity, headcount, clothing, ownership, orientation
- 30s without more events ≠ more story — empty time becomes wait/loop/slow-mo
- Timestamps pace events; they are **not** frame-accurate edit points in first-pass T2V

## Normal

### Stage template

```
[GOAL]
Generate a <video type>. Core subject <SUBJECT>; main event <physical summary>.

[STAGE ONE]
Opens with:   <people, props, scene state>
Main event:   <one primary action>
Ends with:    <person position, prop ownership, picture state>

[STAGE TWO]
Carried over: <must preserve from prior end>
Main event:   <one primary action>
Ends with:    <observable state>

[STAGE THREE]
Main event:   <closing action>
Ends with:    <final picture state>

[KEEP CONSISTENT]
Keep <identity, headcount, clothing, prop ownership, spatial orientation, sound relationships> stable.
```

### Timestamp habit (2.5 maker)

| Habit | Detail |
| ------- | -------- |
| **Second-level ranges** | `0–5s:`, `6–10s:`, `11–20s:` |
| Stages + timestamps | Skeleton first ; timestamps for handoffs / camera beats |
| Post-gen edit | timestamp-level **editing** after generate — edit-mode precision ≠ first-pass T2V frame lock |

| Form | Use on 2.5 |
|------|------------|
| Range `0-5s: …` | **Default** for multi-beat / ~15–30s |
| Point `At 5s the camera whips left…` | Pin one key event |
| Relative `Three seconds after the button…` | Wait / lag between events |
| `Shot 1 / 镜头 1: …` | Optional order label; not a substitute for timestamps when pacing matters |

Field starting point: ~**3–4 meaningful beats per 15s** for narrative. Don’t timestamp every second.

Too little in a window → model invents. Too much → hard cuts or dropped beats. Don’t demand high-frequency micro-actions (“shake 3× per second”).

### Duration matching (content, not vibes)

| Length | Fit |
|--------|-----|
| 4–5s | One clean beat; iterate here |
| ~8s | Micro-narrative, one arc |
| ~15s | Couple of connected beats |
| ~30s | Flagship; **must** stage |

### Continuity block checklist

- [ ] Same named subjects; no extras unless listed
- [ ] Clothing / colors stable
- [ ] Prop count + ownership (hands)
- [ ] Screen direction / axis
- [ ] Set layout landmarks
- [ ] Camera nest or explicit move handoff
- [ ] Speed: natural real-time unless stated
- [ ] Explicit bans that match real risks: no cuts, no slow-mo, no duplicate prop, no teleport

### Stitchable snippets (clip → next clip)

**Extension path:** multi-round **extension** from prior `@Video`, keeping subjects/scene/style/SFX consistent.

```
Extend the video. Continue from the visuals and subjects in @Video 1 and generate
another [duration] clip, keeping the character subjects, scene, visual style,
and sound effects consistent.
[new physical events…]
```

**Host pattern :** extract **final frame** of clip A → `@Image` as **exact first frame** of clip B.

```
Use @Image1 as the exact first frame and continue forward from that moment.
Preserve [identity, props, layout, framing, lens, camera position, light].
Do not replay [completed action from prior clip].
0–Xs: hold / micro-settle only.
X–Ys: first NEW action …
Ending state: …
```

Do **not** retell the whole prior clip.

| Method | Notes |
| -------- | ------- |
| Host extension / Seed extend | Preferred continuity path |
| Last-frame image ref | Strong visual lock |
| Stable subject blurb reused verbatim | Same hair/coat/glasses string |
| Shared `@Image` identity pack | Face/wardrobe; exclude pose/bg |
| `@Video` motion-only from prior | Risky — usually better last-frame + new text path |

### Seamless bridge between two existing clips (advanced — host)

Order : before video → after video → trigger → camera → visual morph → arrival state → audio join.
Aim is continuity of feel, **not** pixel-identical preservation of both sources.

### Recurring description stability

If a character works, **reuse the same sentence** across prompts. Silent wording drift breaks continuity more than the model alone.

## Hard

**One change per stage** — two events in one stage softens the join.

**Carry-over line** — Stage N+1 starts with “Carried over: …” echoing Stage N end.

**Handoff packet**

| Field | From prior end |
|-------|----------------|
| Frame / still | Final frame file (if using image handoff) |
| Bodies | Positions + facing |
| Props | Ownership |
| Camera | Position + move trend |
| Light | Direction / quality |
| Forbidden replay | Actions already done |

| Failure | Fix |
|---------|-----|
| 30s of mush / loop | Add stages; cut event count; match duration to beats |
| Mid-clip identity drift | KEEP CONSISTENT + refs with exclusions |
| Prop teleport | Ownership every stage end |
| Stitch jump cut | Extend prompt / last-frame first-frame + “do not replay” |
| Over-timestamped mess | Prefer stages; timestamps for handoffs/entrances/camera beats |

**Uncertain / host-dependent:** extension audio level match; whether first+last frame mode is exposed. Confirm on the surface you use.
