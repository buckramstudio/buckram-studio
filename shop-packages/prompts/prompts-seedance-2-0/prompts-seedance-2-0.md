# Seedance 2.0 — visual prompt craft

**Target:** Seedance **2.0** only. Do not mix with the 2.5 pack. Caps, Shot-N timing, and ref budgets here are 2.0-only.

Prompt-only. No APIs, no Buckram auto-render.

Use during **chapter draft**: turn chapter beats into visible Seedance prompts (camera, staging, continuity) — not prose rewrite craft.

## What this set assumes (2.0)

| Topic | 2.0 habit |
|-------|-----------|
| Duration | Typically **~4–15s** single-pass (host UI sets length). ~30s usually means multi-clip + stitch. |
| Timing inside prompt | Prefer **`镜头 N` / Shot N** in event order. Avoid forcing exact `0–3秒` windows. |
| Formula | Advanced packaging: subject + action + scene + light/tone + camera + visual style + quality + constraints. |
| Refs | Lighter packs (~**12** combined refs). Don’t max the budget. |
| Audio brackets | `( )` / `<>` / `{ }` / `【】`. |

## Companions

| File | Use when |
|------|----------|
| `seedance-prompt-formula.md` | Slot order, paste templates, lighting/style |
| `seedance-camera.md` | Shot size, moves, one-move-per-shot |
| `seedance-staging.md` | Blocking, frame placement, depth |
| `seedance-continuity-15s.md` | Shot-N stages, stitch/extend within 2.0 limits |
| `seedance-audio-and-refs.md` | Brackets, ref roles, 2.0 asset budgets |
| `seedance-failure-modes.md` | Don’ts, ID drift, competing instructions |

## Light workflow

1. Fill **subject + visible action** (required).
2. Add **scene geography** only if placement matters.
3. Add **one camera plan** (size + move *or* cut plan).
4. Multi-beat clips: **Shot N + end states** (`seedance-continuity-15s.md`).
5. Bind refs with **use + exclude** (`seedance-audio-and-refs.md`).
6. Constraints: only fix the failure you saw last.

## Must-not-break

- Clarity beats prompt density.
- Subject motion ≠ camera motion — two clauses.
- End state is observable on screen.
- Every `@` / numbered ref has one job + explicit exclusions when refs are used.
- No giant generic negative lists; target the real failure.
