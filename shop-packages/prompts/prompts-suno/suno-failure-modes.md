# Suno — failure modes

Fix the failing axis only.

## Light

Must-not-break:
- No brackets in Style
- Chorus words pasted on every chorus
- No Udio / ElevenLabs / Mureka tags in this paste
- Song exists before wrap

## Normal

| Don’t | Do |
|-------|-----|
| `[120 BPM], dark blues` in Style | `dark blues, 120 BPM` |
| One `[Chorus]` and no lyric repeat | Paste chorus lines each time |
| Style sentences (“make it cinematic and epic”) | Comma tags |
| `[Pre-chorus]` (Udio spelling) | `[Pre-Chorus]` |
| `{guitar solo}` (ElevenLabs cue) | `[Instrumental]` or parameterized tag |
| Mixing two host kits | This kit only |
| Writing the song inside Style | Lyrics field |

## Hard

If the take is mostly right, change **one** of: style tags, section tags, or one verse — not all three.
