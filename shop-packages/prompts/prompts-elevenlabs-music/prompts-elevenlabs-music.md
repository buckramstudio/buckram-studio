# ElevenLabs Music — wrap

**This kit formats paste for ElevenLabs Music only.** Write the song first (`prompts-lyrics` if installed). Do not mix Suno, Udio, or Mureka tags.

Prompt-only. No APIs, no Buckram auto-render. **No SDK samples.**

Two paste surfaces, same lyric grammar:

1. **UI** — style prompt + lyrics
2. **Composition plan `text`** — section name + lyric lines + inline cues (styles live beside the text, not in this kit as code)

## Companions

| File | Use when |
|------|----------|
| `elevenlabs-lyrics-tags.md` | `[Verse 1]`, `(ooh)`, `{guitar solo}` |
| `elevenlabs-style-prompt.md` | Genre/mood/instruments/tempo/era — styles, not lyrics |
| `elevenlabs-paste-templates.md` | UI lyrics + plan `text` blocks (no SDK) |
| `elevenlabs-failure-modes.md` | Parentheses vs braces; style in lyrics |

## Light workflow

1. Write the song.
2. UI prompt: answer genre, mood, instruments, tempo, era.
3. Lyrics / plan `text`: section tags, then lines. Phonetics `(ooh)`. Musical cues `{guitar solo}`.
4. Genre and vocal style stay in the **style list / UI prompt**, not in parentheses inside lyrics.
5. Plans: first section’s styles set the track. Each section ~3s–120s.

## Must-not-break

- `{ }` = musical cue; `( )` = phonetics
- No SDK / curl in the writer paste
- One host kit
- Do not teach songwriting here
