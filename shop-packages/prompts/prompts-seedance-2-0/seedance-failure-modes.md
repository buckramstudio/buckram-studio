# Seedance 2.0 — prompt failure modes (camera / stage)

Patterns that break **visual** direction. Fix the failing axis only.

**Target:** 2.0 only. Timing advice here is Shot-N / avoid-forced-seconds — not the 2.5 timestamp-first set.

## Light

Job: diagnose which channel failed (identity / timing / camera / motion / continuity / sound / overcrowding) before rewriting the whole prompt.

Contract: giant generic negative lists usually hurt. Targeted constraints after a real miss.

Must-not-break:
- Don’t stack contradictory camera intents (one move per shot)
- Don’t merge camera move into subject action prose
- Don’t pack two primary events into one Shot N
- Don’t restate choreography that a `@Video` already owns
- Don’t treat Shot N / rare timestamps as frame-accurate cuts
- Don’t use person multi-view sheets for identity

## Normal

### Don’t / do (camera & stage)

| Don’t | Do |
|-------|-----|
| “Cinematic / epic / dynamic camera” | Name move: 缓慢推镜, 平稳横移, 固定镜头 |
| “The camera follows somehow” | Height + screen position + trigger + stop |
| Emotion adjectives alone | Observable performance (jaw, breath, gaze, hands) |
| Six events in one paragraph | Shot N; one change + end state each |
| Empty max-duration with one tiny action | Shorter duration **or** add real beats |
| Two refs defining same attribute | One job per file + exclusions |
| “Use @Video1 as a reference” on edit/extend | Direct edit/extend address + scope |
| Negative laundry list every gen | Constrain the failure you just saw |
| UI params fighting the panel | Align duration/aspect with host |
| Person three-view / multi-view sheet | Face close-up + full-body |
| Force hard `0–3秒` windows as default | Shot N + relative pace words |
| Micro-timing (“3 shakes per second”) | Natural rhythm; whole-shot budgets |

### Maker boundaries (expect disappointment)

1. Shot N allocates pacing — not frame-level cut points. Forcing exact seconds can hurt.
2. Edit prompts raise alignment odds — not frame-exact overlap.
3. Multi-ref = select/combine — not show everything at once.
4. Exact subs / formulas / signage → refs + post. “保持无字幕” lowers odds; not guaranteed.
5. Person multi-view / tiny face in collage → ID drift.
6. Style drift when ref is photoreal but prompt wants anime — name style in text or restyle the ref first.
7. Extend chains: jump/quality melt — shorter chains; white-model repair tip in guide syncs.
8. Too many distinct people in one pass (>~4) → unstable counts (guide syncs).

### Symptom → likely cause

| Symptom | Likely cause | First fix |
|---------|--------------|-----------|
| Floaty undirected motion | No named camera move | Lead with 固定/推镜/横移… |
| Subject and camera both mushy | Axes merged | Split clauses; one move |
| Identity morph mid-clip | Weak consistency / multi-view person | Face+body; stable blurb; KEEP CONSISTENT |
| Extra people / twin props | Unbounded bg; no counts | Counts + no extras/duplicates |
| Hands/props teleport | Missing ownership end states | Hand ledger each Shot N |
| Jump after occlusion | Occlusion underspecified | Hidden duration + emerge invariants |
| Skips middle / mush at 15s | Too many events / no Shot N | Stage; cut events |
| Forced-second weirdness | Exact `0–Xs` | Drop seconds; Shot N |
| Ref background leaks | No exclusions | “Do not copy background/pose…” |
| Burned-in captions | Default text habit | `保持无字幕` / `No subtitles` |
| Late prompt clauses drop | Overlong prompt | Tighten |

## Hard

**Iteration rule:** change one variable per regen when the take is mostly right.

**Overcrowding rule:** remove a character, a move, or a shot event — don’t add adjectives.

| Failure class | Repair pack |
|---------------|-------------|
| Camera | `seedance-camera.md` |
| Blocking / props | `seedance-staging.md` |
| Long-clip drift | `seedance-continuity-15s.md` |
| Ref / audio routing | `seedance-audio-and-refs.md` |
| Slot soup | `seedance-prompt-formula.md` |

**Uncertain:** which mute/music negatives are strongest on your host — keep one clear instruction, not three synonyms.
