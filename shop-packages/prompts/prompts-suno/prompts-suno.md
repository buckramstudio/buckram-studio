# Suno — Custom Mode wrap

**This kit formats paste for Suno Custom Mode only.** Write the song first (`prompts-lyrics` if installed). Do not mix Udio, ElevenLabs, or Mureka tags.

Prompt-only. No APIs, no Buckram auto-render.

Community-observed 2026 V5.x habits — not a hard-coded API. If the host UI disagrees, follow the UI.

## Two fields

| Field | Job |
|-------|-----|
| Style of Music | Plain descriptors. **No square brackets.** |
| Lyrics | One structure tag per line, then lyric lines. |

## Companions

| File | Use when |
|------|----------|
| `suno-lyrics-tags.md` | Structure, parameterized, delivery tags |
| `suno-style-prompt.md` | Style field order; no brackets |
| `suno-paste-templates.md` | Ready two-field paste |
| `suno-failure-modes.md` | Brackets in style, missing chorus repeats |

## Light workflow

1. Write the song (one promise, chorus first). Plain `[Verse]` / `[Chorus]` is enough until this wrap.
2. Fill **Style** from the brief: genre, mood, instruments, vocals, production, BPM/key if known.
3. Wrap **Lyrics**: tag on its own line, then lines. Repeat chorus by **pasting the chorus words again**.
4. Delivery (`[Whispered]`, `[Belted]`, `[Choir]`) in the lyrics field only.

## Must-not-break

- Song first; wrap second.
- No brackets in Style.
- One host kit per paste.
- Do not teach songwriting here.
