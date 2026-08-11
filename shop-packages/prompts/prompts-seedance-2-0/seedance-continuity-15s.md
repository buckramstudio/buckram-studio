# Seedance 2.0 — continuity (~15s) & stitch handoff

Stages via **Shot N**, end states, and joinable clips within 2.0 limits.

**Target:** 2.0 only. Do **not** use the 2.5 timestamp-first recipes from the other version pack.

## Light

Job: give multi-beat generations a **place to land** so motion budget doesn’t collapse.

Contract: each shot/stage = **one primary change** + **visible end state**. Next opens from that state.

Must-not-break:
- Shots continuous in event order; no overlapping budgets
- End state = on-screen observable — not emotional summary
- Continuity block for identity, headcount, clothing, ownership, orientation
- Empty time at max duration → wait/loop/slow-mo
- Shot N / rare timestamps pace events — **not** frame-accurate edit points

## Normal

### Stage template (Shot N)

```
[GOAL]
Generate a <video type>. Core subject <SUBJECT>; main event <physical summary>.
Duration: set in host (typical 2.0 ceiling ~15s).

[镜头1 / Shot 1]
Opens with:   <people, props, scene state>
Camera:       <one move or locked / cut in>
Main event:   <one primary action>
Ends with:    <person position, prop ownership, picture state>

[镜头2 / Shot 2]
Carried over: <must preserve from prior end>
Camera:       …
Main event:   <one primary action>
Ends with:    <observable state>

[镜头3 / Shot 3]
Main event:   <closing action>
Ends with:    <final picture state>

[KEEP CONSISTENT]
Keep <identity, headcount, clothing, prop ownership, spatial orientation> stable.
```

### Timing habit (2.0)

| Habit | Detail |
| ------- | -------- |
| **Prefer Shot N / 镜头 N** | Event order; do not force per-segment duration |
| **Avoid hard `0–3秒` windows** | Docs warn exact-second forcing can be unstable |
| Relative pace words | 快速 / 缓慢 / 随即 / 片刻后 instead of hard seconds |
| Total duration | Host panel + optional constraint words — not internal second math |

| Form | Use on 2.0 |
|------|------------|
| `Shot 1 / 镜头 1: …` | **Default** |
| Relative `Three seconds after…` / 随即 | Lag between events without pinning clocks |
| Range `0-5s: …` | **Avoid as default**; only if a specific host/workflow needs it — expect instability |

Field starting point: ~**3–4 meaningful beats per 15s**. Don’t timestamp every second. Too little → model invents. Too much → hard cuts or dropped beats.

### Duration matching (content, not vibes)

| Length | Fit |
|--------|-----|
| 4–5s | One clean beat; iterate here |
| ~8s | Micro-narrative, one arc |
| ~15s | Couple of connected Shot-N beats; **stage** |
| ~30s | **Not a native 2.0 single-pass flagship**  — plan separate gens |

### Continuity block checklist

- [ ] Same named subjects; no extras unless listed
- [ ] Clothing / colors stable
- [ ] Prop count + ownership (hands)
- [ ] Screen direction / axis
- [ ] Set layout landmarks
- [ ] Camera nest or explicit move handoff
- [ ] Speed: natural real-time unless stated
- [ ] Explicit bans that match real risks

### Extend / stitch within 2.0

2.0 covers **延长** / track join patterns: continue forward/back from `<视频N>`; combination tasks. Hard limits reported in guide syncs: few video inputs, **total ref video duration ≤15s** class — confirm on your host.

```
向后延长<视频1> / Extend @Video1 forward.
Keep character, scene, visual style, and sound relationships consistent.
Shot 1: hold / micro-settle from prior end — do not replay completed action.
Shot 2: first NEW action …
Ending state: …
```

**Edit vs reference phrasing:** for edit/extend, address the clip directly (`严格编辑<视频N>` / `Edit @Video1…`). Avoid “参考@视频N” phrasing that can be misread as R2V feature-borrow.

### Recurring description stability

Reuse the **same subject sentence** across prompts when a character works. Silent wording drift breaks continuity.

## Hard

**One change per Shot N** — two events in one shot softens the join.

**Carry-over line** — Shot N+1 starts with “Carried over: …” echoing prior end.

**Handoff packet**

| Field | From prior end |
|-------|----------------|
| Bodies | Positions + facing |
| Props | Ownership |
| Camera | Position + move trend |
| Light | Direction / quality |
| Forbidden replay | Actions already done |

| Failure | Fix |
|---------|-----|
| Mush / loop at 15s | Add Shot N; cut event count |
| Mid-clip identity drift | KEEP CONSISTENT + refs with exclusions |
| Prop teleport | Ownership every shot end |
| Forced-second mess | Drop `0–Xs`; use Shot N + relative pace |
| Extend jump / quality melt | Shorter extend chain; white-model repair tip in failure-modes |

**Uncertain / host-dependent:** exact max duration on your surface; whether first+last frame mode exists; audio level after extend.
