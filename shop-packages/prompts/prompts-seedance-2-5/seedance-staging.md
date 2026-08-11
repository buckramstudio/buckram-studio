# Seedance 2.5 — staging & blocking

Where people/things sit in space and how they move through the set. Camera → `seedance-camera.md`. Continuity → `seedance-continuity-30s.md`.

**Target:** 2.5 only. Clay / white-box spatial referencing is 2.5-only — do not assume identical 2.0 support.

## Light

Job: make the set a navigable geography the model can keep — not a vibe caption.

Contract: positions, hands, props, entrances/exits, and depth are **stated**, not implied by plot.

Must-not-break:
- Count subjects and key props (“one bottle”, “the same red helmet”)
- Prop ownership (which hand / who holds) through the clip
- Screen direction stays coherent unless you reverse on purpose
- Occlusion: what stays true while hidden
- Depth: foreground / mid / background jobs
- Named stations on set when geography matters

## Normal

### Stage card (fill before prompting)

| Field | Fill |
|-------|------|
| Set shorthand | |
| Fixed architecture (doors, counter, column, cooler) | |
| Camera nest (where camera lives / may move) | |
| Subject A start position + facing | |
| Subject B / extras (stationary? path?) | |
| Props + ownership (left/right hand) | |
| Depth layers (fg insert / mid action / bg life) | |
| Entrances / exits (who, when, which edge) | |
| Axis / eyeline (who looks at what) | |
| End picture (positions + props + camera) | |

### Placement language that steers

Bind subjects to stage geography (`pianist by the piano`, `choir at the back of the stage`, `walks from center stage toward the front edge`). Exact “left third” phrasing is craft (**Uncertain** as official enum).

| Pattern | Effect |
| --------- | -------- |
| Named station on set (“by the piano”, “back of stage”) | Geography lock |
| Subject in left / center / right third | Composition lock |
| Foreground X; subject mid-ground; bg Y | Depth staging |
| Facing each other on the path; guitarist mid-background on bench | Spatial relationships + secondary life |
| Walks frame-left → frame-right beside yellow platform line | Screen direction + landmark |
| Camera stops inside; subject exits to rain; door closes | Entrance/exit geography |

### Blocking beats (physical order)

1. Approach / path
2. Contact (hand, tray, foot, prop)
3. Transfer of force / ownership change
4. Recovery / settle

### Eyelines & attention

| Write | Not |
|-------|-----|
| Eyes move to the door; gaze fixed on the other man | She becomes afraid |
| Looks down at impact, then to sketchbook | Looks surprised |
| Clerk small nod; messenger turns toward entrance | Emotional goodbye |

### Depth & layers

| Layer | Typical job |
|-------|-------------|
| Foreground | Occluder, reveal prop, parallax, wipe for transition |
| Mid-ground | Primary blocking / dialogue |
| Background | Atmosphere life that must **not** steal identity (“stationary”, “mid-background”) |

### Entrances / exits

- Name **edge** (door, frame left/right) and **limb** used.
- State whether camera follows out or **stays**.
- After exit: what remains in frame.

### Occlusion (hidden continuity)

- How long fully hidden
- Same identity, clothing, prop, direction, speed on re-exit
- “No person/prop on both sides at once”
- Landmark that stays fixed

### White-box / clay refs (2.5 — advanced staging)

**Clay render** referencing strengthens for spatial structure, poses, paths, and camera.

| Type | Supplies | Prompt must |
|------|----------|-------------|
| **Coarse** / clay blockout video | Paths, standing positions, entrances/exits, camera path, cuts, light changes, sound rhythm | Map each solid → final subject; **do not** take grey look |
| **Fine** blockout | Complete structure + action + camera | Keep structure/action/camera; re-render materials/cast/scene |

```
Refer to @Clay Render 1 for camera movement, pacing, shot-size transitions,
subject trajectory, and blocking. Refer to @Image 2 for character design,
scene, materials, lighting, color … and render the white model as [final look].
```

Use when multi-body choreography or camera path is load-bearing and text alone keeps failing.

### Environment clauses that matter for stage

| Include | Why |
|---------|-----|
| Time of day / weather that affects visibility | Silhouette, reflections, breath |
| Fixed props and their rest positions | Prevent teleport |
| “Store layout / court markings / bench orientation stable” | Geography lock |
| Background state (lamp already on; cooler closed) | Starting state |

## Hard

**Handedness ledger** — for any carried prop, name hand at start, after each action, at end.

**No teleport rule** — objects don’t reset when off-screen or behind occluders unless you say they do.

**Fluids / cloth / particles** — direction of force + final pooled/settled state.

**Dialogue blocking** — mouth moves only during own lines; silence during business; who keeps mouth closed.

| Failure | Fix |
|---------|-----|
| Extra limbs / duplicate props | Count + “no duplicated X”; one ownership line |
| Hands swap randomly | Repeat hand ownership each stage |
| Background steals scene | “mid-background”, “stationary”, exclude people from env refs |
| Same argument any room | Add exits/barriers/sightlines that force path |
| Jump after occlusion | Repeat invariant list on emerge |
| Text choreography fails | Clay / white-box `@Clay Render` + style/identity images |

**Uncertain:** model obedience on complex multi-person eyelines — keep to 2–4 primary bodies; park others as stationary.
