# Suno — lyrics tags

Lyrics field only. One tag per line, then the lines for that section.

## Structure

`[Intro]`, `[Verse]` / `[Verse 1]`, `[Pre-Chorus]`, `[Chorus]`, `[Post-Chorus]`, `[Bridge]`, `[Hook]`, `[Breakdown]`, `[Instrumental]`, `[Outro]`, `[End]`, `[Final Chorus]`

Number verses when you have more than one: `[Verse 1]`, `[Verse 2]`.

## Parameterized

Add descriptors after a colon for per-section control:

`[Verse: whispered vocals, acoustic guitar only]`

`[Chorus: full band, belted vocal]`

Keep the list short. This is not a second Style field.

## Delivery (lyrics only)

`[Whispered]`, `[Belted]`, `[Choir]`

Place on their own line before the lines they color, or immediately after the structure tag.

## Repeat

A `[Chorus]` tag does **not** re-sing the words by itself. Paste the chorus lyrics again under the next `[Chorus]` or `[Final Chorus]`.

## Don’t

- Put these tags in the Style field
- Invent Udio spellings (`[Pre-chorus]` lowercase) here
- Stack three delivery tags on one line
