# ElevenLabs Music — failure modes

Fix the failing axis only.

## Light

Must-not-break:
- `( )` = phonetics; `{ }` = musical cue
- Vocal/genre style in the prompt or styles list, not lyric parentheses
- No SDK in the paste
- First plan section’s styles set the track
- One host kit

## Normal

| Don’t | Do |
|-------|-----|
| `(soft female vocals)` in lyrics | Styles / UI prompt |
| `(instrumental break)` | `{instrumental break}` |
| `[Whispered]` Suno delivery as the default | `whispered` in styles |
| `[Pre-chorus]` Udio spelling as the only form | `[Pre-Chorus]` or `[Verse]` / `[Chorus]` |
| 150-second section | Split; 3–120s per section |
| Empty first-section styles, dense later | Load styles up front |
| Python/TS compose snippets | Prompt + lyrics / `text` only |

## Hard

If the vocal is wrong, move one style — don’t add three synonyms. If structure is wrong, fix section names, not the poem.
