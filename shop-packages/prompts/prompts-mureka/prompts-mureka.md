# Mureka — lyrics-first wrap

**This kit formats paste for Mureka only.** Write the song first (`prompts-lyrics` if installed). Do not mix Suno, Udio, or ElevenLabs tags.

Prompt-only. No APIs, no Buckram auto-render. No curl.

Lyrics carry structure tags. Style lives in the host **prompt** field.

## Companions

| File | Use when |
|------|----------|
| `mureka-lyrics-tags.md` | Locked tag list |
| `mureka-style-prompt.md` | Style prompt field |
| `mureka-paste-templates.md` | Lyrics + prompt paste |
| `mureka-failure-modes.md` | Long lines, extra invented tags |

## Light workflow

1. Write the song. Short lines (~6–10 words). Chorus simpler than verses.
2. Default map: Verse → Chorus → Verse → Chorus → Bridge → Chorus → Outro.
3. Wrap with the locked tags. Style descriptors go in the prompt field, not as fake lyric tags.
4. Repeat chorus by pasting the chorus words again.

## Must-not-break

- Lyrics-first; prompt is style
- Locked tags only
- One host kit
- Do not teach songwriting here
