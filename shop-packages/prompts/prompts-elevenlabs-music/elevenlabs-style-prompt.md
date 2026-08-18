# ElevenLabs Music — style prompt

Decide these five or the model averages them: **genre, mood, instruments, tempo, production era**.

Vocal delivery words belong here (or in plan styles): `whispered`, `belted`, `close and intimate`, `soft female vocal`.

## UI prompt shape

```
dark electric blues, 80 BPM, E minor, spare guitar, dry room, understated male vocal, late-night kitchen
```

Narrate arrangement with *start with / then / bring in* when the UI is a single prompt:

```
dark electric blues, 80 BPM — start with spare guitar, then bring in a dry vocal; no crowd, no shine
```

## Plan styles (writer-facing, not code)

Put the same ideas in the section’s **positive styles** list. First chunk: at least a handful of real styles (genre, vocal, instruments, tempo). Negative styles: what to avoid (`crowd chant`, `EDM drop`).

Generic “great production” is a weak extra, not the whole list.

## Don’t

- Put `soft female vocals` in lyric parentheses
- Leave all five questions open (“upbeat electronic track”)
- Paste Suno comma-tags into lyrics brackets
