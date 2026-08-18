# Udio — failure modes

Fix the failing axis only.

## Light

Must-not-break:
- Official spellings (`[Pre-chorus]`, not `[Pre-Chorus]`)
- Tags are guidance
- No Suno Style-field habits (brackets for BPM) in the Udio prompt
- One host kit

## Normal

| Don’t | Do |
|-------|-----|
| `[Pre-Chorus]` / `[Post-Chorus]` | `[Pre-chorus]` / `[Post-chorus]` |
| `[Verse: whispered vocals, acoustic only]` as default | `[Verse]` + put whisper in the prompt |
| `{guitar solo}` | `[Instrumental]` / `[Solo]` |
| `(ooh)` as ElevenLabs phonetics system | Plain lyric or `[Choir]` if it fits |
| Angry rewrite because a tag was “ignored” | Guidance; regenerate or simplify |
| Mixing Suno `[End]` / `[Final Chorus]` | Udio list only |

## Hard

If the prompt and lyrics fight (prompt says lullaby, lyrics say `[Drop]`), align them. Don’t add more tags.
