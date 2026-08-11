# Seedance 2.5 — prompt failure modes (camera / stage)

Patterns that break **visual** direction. Fix the failing axis only.

**Target:** 2.5 only. Timestamp/30s advice here — not the 2.0 Shot-N-prefer set.

## Light

Job: diagnose which channel failed (identity / timing / camera / motion / continuity / sound / overcrowding) before rewriting the whole prompt.

Contract: giant generic negative lists usually hurt. Targeted constraints after a real miss.

Must-not-break:
- Don’t stack contradictory camera intents (one move per beat)
- Don’t merge camera move into subject action prose
- Don’t pack two primary events into one stage
- Don’t restate choreography that a `@Video` / clay ref already owns
- Don’t treat timestamps as frame-accurate cuts in first-pass T2V
- Don’t dump 50 refs without roles

## Normal

### Don’t / do (camera & stage)

| Don’t | Do |
|-------|-----|
| “Cinematic / epic / dynamic camera” | Name move: push-in, orbit, locked-off, parallel track |
| “The camera follows somehow” | Height + screen position + trigger + stop |
| Emotion adjectives alone (“angry”, “tense”) | Observable performance (jaw, breath, gaze, hands) |
| “Jumps impressively / looks surprised” | Approach → contact → result → settle |
| Six events in one paragraph | Stages; one change + end state each |
| Empty 30s with one tiny action | Shorter duration **or** add real beats |
| Two refs defining same attribute | One job per file + exclusions |
| “Use @Video1 as a reference” on edit | “Edit @Video1…; change only [scope]” |
| Negative laundry list every gen | Constrain the failure you just saw |
| UI params inside prompt | Duration/aspect/resolution in host controls |
| Niche lens slang alone | Term + visible fg/bg change |
| “Realistic physics” alone | Force direction + end pooled/settled state |
| Force all 20 refs on screen | Per-scene Uses list; role layers |
| Micro-timing (“3 shakes per second”) | Whole-second budgets; natural rhythm |
| Person multi-view identity sheet | Face close-up + body (guide-mirror / series habit) |

### Boundaries (expect disappointment)

1. Timestamps allocate pacing — not frame-level cut points. Seed edit mode is more precise than first-pass T2V.
2. Edit prompts raise alignment odds — not frame-exact overlap.
3. Multi-ref = select/combine — not show everything at once.
4. Exact subs / formulas / signage / frame-precise timing → refs + post.
5. Edit mode often locks aspect + ~duration (±~0.3s).
6. First-frame modes lock aspect to first image; mismatched last frame can stretch.
7. Extension locks aspect; extended audio level may drift.
8. Image-order films need explicit order/mapping if it matters.
9. Seamless transitions aim for continuity — not pixel-identical sources.
10. Style drift when ref is photoreal but prompt wants anime — name style in text or restyle the ref first.
11. Complex multi-subject physics remains fragile.

### Symptom → likely cause

| Symptom | Likely cause | First fix |
|---------|--------------|-----------|
| Floaty undirected motion | No named camera move | Lead with static/push/orbit… |
| Subject and camera both mushy | Axes merged | Split camera vs subject clauses |
| Identity morph mid-clip | Weak consistency / no refs / multi-view person | Face+body refs; stable blurb; KEEP CONSISTENT |
| Extra people / twin props | Unbounded background; no counts | Counts + “no extras/duplicates” |
| Hands/props teleport | Missing ownership end states | Hand ledger each stage |
| Jump after walking behind object | Occlusion underspecified | Hidden duration + emerge invariants |
| Skips middle of 30s | Too many events / no stages | Stage + contiguous times |
| Loops / slow-mo padding | Duration > content | Cut duration or add one real beat |
| Ref background leaks | No exclusions | “Do not copy background/pose…” |
| Camera ignores you | Competing moves + adjectives | One camera plan; delete the rest |
| Dialogue lips wrong | No performance blocking | Timed lines; mouth only on own speech |
| Burned-in captions | Default text habit | `No subtitles` |
| Late prompt clauses drop | Overlong prompt | Tighten; retention ≠ char max |
| Clay look leaks | No “do not take grey look” | Map solids → final subjects + style images |

## Hard

**Iteration rule:** change one variable per regen when the take is mostly right.

**Overcrowding rule:** if clarity fails, remove a character, a move, or a stage event — don’t add adjectives.

**Montage vs narrative:** wrong mode looks like “failure.” Narrative wants clarity; montage wants option density.

| Failure class | Repair pack |
|---------------|-------------|
| Camera | `seedance-camera.md` |
| Blocking / props | `seedance-staging.md` |
| Long-clip drift | `seedance-continuity-30s.md` |
| Ref / audio routing | `seedance-audio-and-refs.md` |
| Slot soup | `seedance-prompt-formula.md` |

**Uncertain:** which negatives are strongest (`No BGM` vs `(no music)` vs prose) — prefer host-documented forms; keep one clear mute/music instruction, not three synonyms.
