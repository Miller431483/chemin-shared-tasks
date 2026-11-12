# Caption method — standing rule for Lucky and TheMAN

Every video with captions, on either Page, must follow this method.
It is the method proven on the 127 Rituels v6 (approved by Rajo).
Do not use any other caption timing method.

## The method (in order)

1. Finish the narration audio FIRST. Do not time captions from a script
   estimate, a draft take, or a different audio file.
2. Run faster-whisper on the FINISHED narration audio:
   model `small`, language `fr`, `word_timestamps=True`.
   This gives the start and end time of EVERY spoken word.
3. Build the caption chunks from the SCRIPT, using the whisper word times:
   - Max 4 words per chunk.
   - A new chunk starts after each period.
   - Chunk start = the first word start time.
   - Chunk end = the last word end time (end-exclusive: end one frame
     before the next chunk starts, so two chunks never overlap).
   - The caption text must match the narration WORD FOR WORD. Read the
     script and the whisper transcript side by side. If a word is in the
     narration but not in the captions, the caption list is wrong.
4. The red highlight must follow the SPOKEN word, not the chunk.
   Within a chunk, the highlight moves to each word as it is spoken,
   using the whisper word times.
5. Caption style (approved): Noto Sans Black, ALL CAPS, white bold,
   black outline, bottom of frame, current word in a RED box (#FF0000),
   font size 56, max 4 words per chunk.

## Never do this

- Never estimate caption timing from the text (words per second,
  dividing the duration evenly, guessing). The narration has pauses
  between sentences; estimation always drifts.
- Never nudge individual chunks to fix a sync problem. If the captions
  are off, the caption list or the timing source is wrong. Re-run
  faster-whisper on the finished audio and rebuild ALL timings.
- Never deliver a video whose caption text is missing a word from the
  narration. A missing word shifts every later chunk early.
- Never use a caption tool that does not give word-level timings from
  the actual audio (for example CapCut auto-captions or manual timing).

## Verification checklist — run before delivering ANY video

Watch the finished video from start to end, with sound on, and check:

1. Every caption chunk appears exactly when its first word is spoken,
   not before, not after. (Tolerance: 0.1s.)
2. Every word in the narration appears in the captions. Read the
   narration script, then watch: no word skipped, no word added.
3. The red highlight moves to the word being spoken. It must not stay
   on the first word of a chunk.
4. No chunk appears before its first word is spoken. If the viewer can
   read the next sentence before hearing it, the captions are early.
5. No two captions overlap on the same frame.

If ANY check fails, do not deliver the video. Re-run faster-whisper
on the finished audio and rebuild the timings. Do not patch by nudging.

## Why this rule exists

2026-11-12, Noces lot-drawing short (TheMAN Build V5.4): the captions
were in sync for the first 13 chunks, then ran 0.7-1.4s early for the
last 4 chunks. Root cause: the word "grimper" was missing from the
captions, so every chunk after it started too early. Five rounds of
nudging individual chunks did not fix it, because the caption list
itself was missing a word. The fix was to re-derive all timings from
the audio with "grimper" included (18 chunks). Correct timings are in
Lucky file `noces-short-caption-diagnosis-2026-11-12.md`.
