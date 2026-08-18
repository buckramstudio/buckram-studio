# ElevenLabs Music — lyrics / plan text

Same grammar for the UI lyrics field and composition-plan `text` blocks.

## Section names

Square brackets: `[Verse 1]`, `[Verse 2]`, `[Chorus]`, `[Pre-Chorus]`, `[Bridge]`, `[Outro]`, `[Intro]`

Section name on its own line (or at the start of the block), then lyric lines.

## Lyrics

Plain lines. One line per sung line. Line breaks matter.

## Phonetics

Parentheses: `(ooh)`, `(yeah)`, `(hmmm hmmm)`

These are **sounds**, not vocal-style directions.

## Musical cues

Curly braces: `{guitar solo}`, `{scratching}`, `{instrumental break}`

Short inline directions only. Broader genre / vocal style does **not** go here.

## Don’t

```
[Verse]
(soft female vocals) I've been waiting
(instrumental break)
for you
```

## Do

Lyrics:

```
[Verse]
I've been waiting
{instrumental break}
for you
```

Vocal style (“soft female vocals”) belongs in the UI prompt or the plan’s **styles**, not in parentheses.

## Timing (plans)

Each section about **3–120 seconds**. First section’s styles set the whole track.
