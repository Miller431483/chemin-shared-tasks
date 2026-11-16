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

## Image Generation Rules (added by Florence, 2026-11-16)

Source: "AI Image Creation Basics in Studio" lesson guide
(01-ai_image_creation_basics_guide.pdf) plus Florence's mapping of
Studio onto our stack.

- What AI image generation actually is: not random prompting. Best
  results combine four elements — prompt, model, settings, and
  references. Repeatable and learnable once those four are
  understood. The loop is generate, review, adjust, repeat.
- The prompt bar: three modes (image, video, audio), each with its
  own settings — in our stack these are separate tools (Gemini for
  images, Flow for video, ElevenLabs for audio). Assist / Wise
  Enhance turn rough ideas into detailed AVB prompts; always check
  the enhanced prompt still matches the original intent before
  generating.
- Model and settings:
  - The model is the engine; different models suit realism, editing,
    speed, quality, reference-following. If results stay
    unsatisfying, switching models is a valid fix — add it to the
    AVB diagnosis before re-rolling the same model.
  - Aspect ratio: choose once and stick to it per project. 16:9
    YouTube/cinematic, 9:16 TikTok/Reels/Shorts (our default),
    1:1 profile/product/static.
  - Quality: test cheap and fast while exploring; highest quality
    only for finals. Cost is shown before generating; multiple
    outputs and high quality cost more.
  - Outputs: generate several variations (up to 4) and pick the
    strongest; never judge an idea from one generation.
- Reference images:
  - Upload a reference to show what words cannot; use for character
    consistency, products, clothing, poses, locations, style,
    colours.
  - ALWAYS state in the prompt what the reference is for and what
    to preserve: "use as character reference, keep face, hairstyle
    and skin tone, place her in..." An unexplained reference gets
    the wrong element copied (pose instead of face, background
    instead of outfit).
  - If identity: preserve face, hair, skin tone, body type. If
    outfit: preserve clothing, change location. If product:
    preserve packaging, logo, shape, colour, material. If pose
    only: say pose reference, NOT identity reference.
  - This is the mechanism behind our character-continuity rule: the
    series anchor still is an identity reference and every later
    prompt must say so explicitly.
  - Saved characters/products (@ button) → our equivalent: the
    episode package's reference stills, re-added each time (Flow
    "ingredients" where Flow is usable).
- Credits and navigation: test ideas with fewer outputs or a faster
  model before committing credits to high-quality runs. Project
  reality: Gemini web has no Veo model/quality selector; Flow DOES
  have it, and Flow work runs in FLORENCE'S OWN browser (his
  instruction, 2026-11-16) — the cloud browser cannot run Flow, his
  can. So Flow steps (Veo quality selection, scene builder,
  ingredients) are done through his browser when it is available;
  otherwise the credit discipline is the account rotation plus the
  Gemini-first + pause rule, and where a cheaper test generation
  exists, use it before the final render.

## Cinematography Rules (added by Florence, 2026-11-16)

From Florence's note (Granola: "Cinematography fundamentals: depth,
framing, and lighting for AI image generation"). These deepen the
AVB Camera and Lighting elements; every image and video prompt is
built with them.

### Building depth with layers
- AI generates flat images by default: subject pasted onto
  background like a sticker. Every strong frame has 3 layers:
  foreground, midground, background.
  - Background: the world behind the subject (street, sky, room).
  - Midground: where the subject lives.
  - Foreground: the most forgotten layer, closest to the camera
    (grass, smoke, leaves, a railing).
- Adding a foreground is the fastest way to make any AI shot look
  cinematic: out-of-focus elements close to the lens make the eye
  travel front to back.
- Atmosphere is the second depth tool: haze, fog, mist, dust,
  smoke. Distant things get lighter and softer, which the brain
  reads as space. Light haze pushes backgrounds back; low fog
  physically separates layers; god rays make air visible.
- Key question when a shot feels flat: what's in the foreground,
  and what's in the air?

### Composition and subject placement
- Dead center is the most static placement: reads like a passport
  photo.
- Rule of thirds: divide the frame into a 3x3 grid, place the
  subject on a line or intersection. Off-center subjects create
  space for the eye to travel into.
- Leading lines pull the viewer's eye toward the subject: roads,
  walls, fences, light beams.
- Lead room: leave space in the direction the subject is looking
  or moving. Crowding the front of the frame makes the shot feel
  trapped.
- Center framing is still valid when chosen deliberately: hero
  shots, raw symmetry, direct lens stare.

### Lighting logic
- "Cinematic lighting" in a prompt means nothing; name the actual
  source. Motivated light: a window, sun, lamp, fire, headlights,
  light through a doorway. The source doesn't need to be in frame;
  shadows reveal its direction.
- Hard vs. soft light: hard (small source) = strong defined
  shadows, dramatic and tense; soft (large/diffused source) =
  smooth transitions, calm and expensive.
- Direction changes mood: side light is the most cinematic, carves
  shape and texture; backlight separates subject from background,
  good for silhouettes; front light flattens, used for beauty and
  fashion.
- Color temperature sets emotion: warm (gold/orange) = intimate,
  alive, nostalgic; cool (blue/gray) = distant, lonely, modern;
  green tint = unease, artificial, something is wrong. Warm
  subject against cool background is the strongest color contrast.
- Material reaction makes shots feel physical: describe how light
  behaves on each surface (metal highlights, glossy reflections,
  fabric absorbing light). Catchlight in the eyes is small but
  critical: without it, eyes look dead.
- Consistency across shots: lock source, direction, temperature,
  and shadow depth in a prompt block and copy it across every
  shot of the sequence.

### Camera angle, shot size, and lens
- Angle answers: where is the viewer standing? Eye level = honest
  baseline; low angle = powerful, heroic; high angle = vulnerable,
  exposed; Dutch angle = diagonal, instantly tense and unstable;
  profile = distant, locked in thought; back shot = mystery;
  POV = viewer becomes the character.
- Shot size answers: what does the viewer need to read right now?
  Extreme wide (world is the subject, person tiny), wide/full
  (body, posture, silhouette, outfit), medium (most versatile,
  natural conversation distance, monotonous alone), medium
  close-up (shift from behavior to reaction), close-up (eyes,
  breath, smallest change), extreme close-up (one detail, maximum
  emphasis). A close-up only hits hard after holding the viewer at
  a distance.
- Lens answers: how does the space feel? Wide 16-24mm exaggerates
  depth, viewer feels inside the scene; normal 40-50mm calm, no
  optical trick; 85mm separates subject from background and pulls
  the background closer; 200mm+ compresses space, stacks distant
  planes. Focal length controls field of view; camera position
  controls perspective. Shallow depth of field (low f-number)
  requires distance between subject and background to work.
- Camera bodies carry distinct character: ARRI Alexa (all-round
  drama benchmark), Sony Venice 2 (low light and night), RED
  V-Raptor (sharp modern digital, action), Hasselblad medium
  format (luxury commercial, products).

## Project overrides (unchanged, win on any conflict)

- Rajo approves the exact text of every post and every finished video
  before posting; no salesy voice; Rajo stays anonymous.
- No new subscriptions: Gemini Pro, ChatGPT Plus, ElevenLabs, free
  tiers only.
- TheMAN never replies to messages/comments and never does the
  30-minute check — Lucky only.
- Captions: CAPTION-METHOD.md (faster-whisper word timings,
  CAP_Y=1320). Narration: no delivery tags, ends with a statement.
