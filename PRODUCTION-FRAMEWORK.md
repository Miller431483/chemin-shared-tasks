# Production framework — the Golden Rule applied (Florence, 2026-11-14)

Standing rule for all Chemin de Lumière / Tia-Tek MG content production,
for Lucky and TheMAN.

**TheMAN's role in this framework: he IS the "me" of Step 1.** He owns
the Idea and gathers everything — source text, the fixed payoff, the
calendar slot, the approvals path — before any tool is opened, exactly
as production already runs. The six steps below are then executed end
to end without per-step approvals; the finished video goes to Rajo for
approval before posting.

## The Four AI Model Types

- LLMs (Large Language Models): text-based, used for writing,
  brainstorming, planning, and scripting
  - Key tools: ChatGPT, Claude, Gemini, DeepSeek, and Wise (built into
    PromptWise, free)
  - Best use: develop ideas and prompts before generating anything
- Image models: convert text descriptions into visuals
  - Different models suit different styles (realism vs. abstract)
  - Multiple options exist; choosing the right one matters
- Video models: take text or images and produce moving clips
  - Strengths vary: cinematic quality, lip-sync, human motion
  - Quality has reached near-cinematic realism
- Audio/voice models: voiceover, voice cloning, sound effects, music
  - Often built into video tools; layering extras adds immersion

## The AI Creation Workflow

Six-step process: Idea → Plan/Chat → Image → Refine → Video → Edit
and Post

- Step 1: Idea: define what you're making, where it's going, who it's
  for, and what it should feel like before opening any tool.
  (TheMAN: idea + gathering — source, payoff fixed from the primary
  text BEFORE Wise is briefed, slot, audience promise per the CONTENT
  OUTCOME RULE: promise, build, payoff.)
- Step 2: Plan with chat (Wise, ChatGPT, etc.): develop the concept,
  build the prompt, write the script. The Golden Rule: the chat is a
  conversation, not a single shot — the first draft is never final;
  consult Wise before any image or video, before wasting credits, and
  before giving up on a bad result. Offer two alternate hooks with
  every narration; Florence picks the opener.
- Step 3: Generate images first, even if the final output is video.
  Images are cheaper, faster, and easier to control. Lock in
  composition, character, lighting, and feel before moving to video.
  (Character continuity: identity-reference stills across a series;
  scene variety across episodes.)
- Step 4: Refine: fix issues (background, lighting, hands) before
  animating. Upscale if needed for better video output. If the concept
  is fundamentally wrong, go back to Step 2.
- Step 5: Video: animate the refined image using a video model.
  (Project rule: Gemini first for animation; if ALL Gemini accounts
  are out of usage, PAUSE and report — never finish on a fallback.
  Video prompts describe motion only. Verify clips are 9:16 on disk
  and frame-check them locally.)
- Step 6: Edit and post: pacing, captions, and sound all affect the
  final feel. (Project finish standard: pure ffmpeg montage, Tia-tek
  Voice on ElevenLabs, captions per CAPTION-METHOD.md at CAP_Y=1320,
  3.5s CapCut end card, 1080x1920.)

## Prompting Framework (AVB)

A prompt is direction, not just description: subject, environment,
camera, lighting, mood, style.

- Subject: describe age, hair, clothing, expression, posture, and
  action; avoid vague labels like "a man"
- Environment: specific place, time of day, weather, background
  objects, atmosphere
- Camera: shot size (wide, medium, close-up), angle (low, high, POV),
  and movement for video
- Lighting: describe the source and direction, not just the effect
  ("warm table lamp on the left" vs. "warm lighting")
- Mood: 1-2 words to guide emotional tone (e.g. "quiet and
  reflective", "tense and paranoid")
- Style: optional; over-stylizing (e.g. "hyper-detailed", "cinematic
  masterpiece") can produce a fake, plastic look
- Prompt Ladder: start with a seed idea, then layer in each framework
  element one by one
- JSON prompting: structures prompts into labeled sections, forces
  clarity, easier to edit and repeat
- Wise Enhance: paste a rough idea, hit enhance, and Wise builds a
  full optimized prompt (also reads reference images)

## Diagnosing Bad Outputs and Building a Prompt Library

- When a result is bad, identify which framework element failed:
  - Generic image: subject or environment too vague
  - Fake/plastic look: over-polished style words or unrealistic
    lighting
  - Boring composition: no camera angle or shot size specified
  - AI ignored a detail: move it to the start of the prompt
  - Too busy: simplify and remove unnecessary details
- Talking to AI chats effectively: five rules
  1. Give context about who you are and what you're making
  2. Be specific about the outcome (length, platform, audience, tone,
     goal)
  3. Iterate: treat the first response as a draft, push back and
     refine
  4. Use it for feedback: paste in your own work and ask for a
     critique
  5. Diagnose failures with the chat rather than regenerating blindly
- Prompt Library: save every strong prompt (in our setup: inside the
  episode package in the project files, so the winning structure is
  reused instead of starting from zero each time)

## Tool Stack Mapped to the Workflow

- Tools: ChatGPT, Gemini (incl. Veo, Imagen/Nano Banana), Google
  Flow, ElevenLabs, Mistral AI, Canva
- Model types covered
  - LLM chat: ChatGPT (ideation, scripts), Gemini (research, prompts
    feeding Flow), Mistral (alternative drafts)
  - Image: Gemini image gen (drops straight into Flow), ChatGPT,
    Canva
  - Video: Veo via Gemini and Google Flow (text-to-video,
    image-to-video, frames-to-video, extend, scene builder; Veo 3
    has native audio)
  - Audio: ElevenLabs (voiceover, cloning, SFX, music) + Veo 3
    native audio for in-clip sound
- Workflow with this stack
  - Step 1 Idea: define output, platform, audience, feel, aspect
    ratio (Flow supports 16:9 and 9:16)
  - Step 2 Plan: ChatGPT or Gemini → AVB-framework image prompt, then
    separate video prompt with camera movement; shot list for
    multi-shot pieces
  - Step 3 Image: generate in Gemini; keep reference images for
    Flow's "ingredients" for recurring characters/products
  - Step 4 Refine: Canva for backgrounds, text, hand fixes,
    upscaling; regenerate rather than polish a bad base
  - Step 5 Video: Flow image-to-video from the refined still;
    extend/scene builder to chain shots; Veo is the expensive step,
    so fix the image first
  - Step 6 Edit/post: Flow scene builder for rough cut → Canva or
    CapCut for captions, pacing, overlays; add ElevenLabs
    voiceover/SFX/music (keep Veo audio if good enough, otherwise
    mute and replace)
- Feedback loop: drop bad outputs into ChatGPT/Gemini and ask which
  AVB element failed before spending more Veo credits
- Replacing PromptWise features
  - Wise Enhance → ask Gemini/ChatGPT to "expand this into a detailed
    AVB-style prompt"
  - Prompt Library → Flow project history + save winning prompts in
    the episode package (project adaptation, see above)
- Net: Gemini + Flow + ElevenLabs + Canva cover all four model types
  and all six steps; ChatGPT and Mistral are optional extras for
  ideation

## Project overrides (unchanged, win on any conflict)

- Rajo approves the exact text of every post and every finished video
  before posting; no salesy voice; Rajo stays anonymous.
- No new subscriptions: Gemini Pro, ChatGPT Plus, ElevenLabs, free
  tiers only.
- TheMAN never replies to messages/comments and never does the
  30-minute check — Lucky only.
- Captions: CAPTION-METHOD.md (faster-whisper word timings,
  CAP_Y=1320). Narration: no delivery tags, ends with a statement.
