# Udio — guidance-tag wrap

**This kit formats paste for Udio only.** Write the song first (`prompts-lyrics` if installed). Do not mix Suno, ElevenLabs, or Mureka tags.

Prompt-only. No APIs, no Buckram auto-render.

Tags are **guidance**, not commands. `/` autocompletes recommended tags in Custom lyrics.

## Two surfaces

| Surface | Job |
|---------|-----|
| Prompt | Topic + comma-separated genres |
| Lyrics | Official guidance tags, then lines |

## Companions

| File | Use when |
|------|----------|
| `udio-lyrics-tags.md` | Published tag list (spellings locked) |
| `udio-style-prompt.md` | Prompt shape |
| `udio-paste-templates.md` | Ready paste |
| `udio-failure-modes.md` | Wrong hyphenation, command-thinking |

## Light workflow

1. Write the song.
2. Prompt: what it’s about, then genres (comma-separated).
3. Lyrics: pick tags from the published list. Type `/` in the host to autocomplete.
4. Do not treat a missed tag as a bug — guidance only.

## Must-not-break

- Use Udio spellings (`[Pre-chorus]`, not Suno `[Pre-Chorus]`).
- One host kit per paste.
- Do not teach songwriting here.
