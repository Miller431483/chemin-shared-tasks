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

## Course Library Rules (added 2026-11-16, from the full Drive library)

The whole AVB course library (143 PDFs, ~172,000 words, nine
modules) was read and extracted; the full attributed extraction is
in COURSE-LIBRARY-EXTRACTION.md in the project files. What follows
is everything that ADDS to or SHARPENS the rules above. Where the
course assumes tools we do not use (Kling, Seedance, HeyGen,
Midjourney, PromptWise Studio), only the transferable technique
was taken; the tool itself was not adopted.

### Briefing Wise (the chat step, systematised)
- Every brief to Wise follows the Simple Formula: Context, Goal,
  Details, Output Format. Master shape: "I'm working on [what]. My
  goal is [outcome]. The audience is [who]. The style should be
  [tone/mood/visual/pacing/realism]. I want to avoid [negatives].
  Help me by [exact task]. Format the answer as [script / prompt /
  table / checklist / JSON]."
- Follow-up commands are standard tools, not afterthoughts: "make
  the hook stronger", "cut this by 30%", "explain what is weak
  about this", "give me 5 stronger versions", "convert to JSON".
- Diagnose with the chat using problem→question prompts (fake
  look, boring idea, robotic script, weird motion) instead of
  regenerating blindly — blind regeneration is how credits die.
- Hook Writer discipline: hooks are produced in named categories
  (curiosity, pain-point, contrarian, direct benefit, story,
  beginner-friendly, premium/authority). BANNED generic hooks:
  "You need to see this", "This changed everything", "Nobody is
  talking about this", "This is a game changer", "I wish I knew
  this sooner" — and their French equivalents.
- Script Doctor check on every narration before production: hook
  strong enough? where does it lose energy? what sounds robotic?
  what is too generic? what should be cut?

### Stills: QC gate, realism system, model split
- Five-question QC gate on EVERY still before it may animate: (1)
  consistent with the other scenes? (2) lighting matches the mood?
  (3) person/product believable? (4) aspect ratio correct? (5)
  real, or obvious AI gloss? Any "no" = fix or regenerate; never
  proceed on a failed still.
- Realism lock block, appended to still prompts when realism
  matters: candid, natural ambient light, visible skin texture,
  muted colour, slight imperfection, no glamour retouch, no beauty
  filter. Standard negatives: no cartoon, no CGI/3D render look,
  no plastic skin. With GPT Image, end the prompt with
  "photorealism".
- The three avatar killers, checked on every character still:
  plastic airbrushed skin; studio lighting where it couldn't
  exist; perfect staged camera/background. Most real social
  content is phone-shot; "shot on iPhone, candid" breaks the
  staged look.
- Model split by job: GPT Image 2.0 for anything text-critical
  (labels, character sheets) and surgical edits; NanoBanana Pro
  (Gemini) for fast realistic iteration. Same prompt in both when
  unsure; keep the winner per job. Midjourney not adopted.
- Character consistency pipeline: pick the believable base face
  first; the reference must be clean (sharp, natural light) — a
  bad reference means bad consistency almost every time. Build a
  six-angle turnaround sheet from it (generated 16:9 even for
  vertical content — a deliberate exception, the sheet is a tool,
  not a post). New scenes prompt "same person + location + outfit
  + camera + lighting + expression + realism details".
- Multi-object scenes: assemble and LABEL the composite in Canva
  first, then reference the labels — loose multi-object uploads
  into Gemini fail most of the time. Gemini-app stills carry a
  bottom-right watermark; remove with Canva Magic Edit when it
  shows.
- Canva pre-animation pass on stills: BG Remover, Magic Eraser
  for single small flaws instead of regenerating, Magic Expand
  for format fixes; normalise warmth/brightness across a sequence
  so the video does not inherit mismatched worlds.
- UPSCALE BEFORE ANIMATING, ALWAYS: 2x (1K→2K) or 4x (1K→4K)
  with a non-repainting upscaler (NanoBanana Pro / GPT Image
  2.0). More pixels in the still = visibly clearer video.
  Skipping it on a hero image is a false economy.

### Prompt weighting and locked blocks
- The end of a prompt is weighted heavily: colour grade and
  style keywords go LAST, after the scene. Full formula: [scene]
  + [lighting source] + [grade style] + [film reference].
- Lighting block technique: the lighting block (source, lit
  side, temperature, shadow depth) is written once, placed at
  the end of the prompt, and copied VERBATIM into every shot of
  a sequence; change only action and shot size between shots.
  A broken shot is regenerated with the same block.
- Locked character/setting/style blocks are pasted verbatim into
  every shot prompt of a sequence, with the full negative list —
  never paraphrased (paraphrase drifts identity and style).
- Aperture needs distance: a low f-number against a wall stays
  sharp; describe the subject–background DISTANCE, not only the
  f-number. Focal length controls field of view; camera POSITION
  controls perspective (a wide lens does not distort a face —
  pushing the camera close does).
- Kelvin numbers when precision helps: 5600K daylight, 2800K
  warm sconces; mixed temperatures stated per source.

### Video generation
- ONE-MOVE RULE: one main subject movement + one main camera
  movement + one clear scene per clip. Overcrowded motion is the
  top cause of glitching and morphing.
- The video prompt starts with the camera move, and the source
  image is designed to complement it. Never re-describe what is
  visible in the start frame; prompt only what should HAPPEN.
  Four motion components: camera, subject, environment, lighting
  change.
- Timed-sequence prompting for complex clips: second-by-second
  blocks, each with its own action (and SFX note), with the
  locked style/camera/character blocks repeated — the technique
  behind the Live Filmset format.
- Scene chaining: export a clip's last frame and use it as the
  next clip's start frame to build long sequences (Flow: a
  second connected image becomes the end frame automatically).
- If Veo native audio is ever used: the voice is a locked asset
  — one verbatim voice block (accent + tone + pacing +
  personality) pasted into every prompt; always specify an
  accent (few voices per accent forces consistency); keep lines
  short; punctuation and "..." are delivery direction. Our
  default remains muting Veo audio and using ElevenLabs.
- Dialogue timing: AI dialogue defaults about 2x too slow;
  specify roughly 4.2 words per second, and word-count any
  spoken text to the clip's duration (too many words = sped-up
  speech, too few = gibberish). This is also why our narrations
  are written to length, not trimmed to fit afterwards.
- AI video editing (in-footage fixes): the risk is
  over-regeneration — always compare against the original clip
  (face, hands, lips, background drift); one change at a time.

### Sound (ElevenLabs discipline)
- Sound is added LAST, after the visual edit. Voice =
  information, music = emotion, SFX = physicality.
- SFX generation: ~4-5 seconds per effect, generate 4 samples,
  keep the best; layer effects with distance-based volumes
  (close sounds louder, far sounds quieter).
- Ambient audio matched to the scene (footsteps, rain, crowd,
  fabric) is part of the finish, not an optional extra.

### Edit and export
- Realism pass on finished clips, in order: lower contrast
  heavily → saturation slightly down → small highlight lift →
  camera shake turned down until barely noticeable.
- Export for TikTok: 1080p at 30fps maximum. 4K/60 exports get
  downgraded by TikTok (to 720p) and look worse than a clean
  1080p30 upload. (YouTube may take 4K/60; not our channel.)
- Text and captions are added in the EDIT, never generated by
  the video model.

### Scripts and hooks (educational content)
- T.E.A.C.H., the authority-video structure: Teach something
  genuinely valuable first → Expand with mechanism and depth →
  Align with the audience → Credentialize (specifics: numbers,
  names, citations) → Hand off the action as the natural next
  step. It maps onto our promise/build/payoff: the payoff IS the
  credentializing specificity.
- Gradualization: never open with a claim the audience does not
  yet believe; start from a belief they hold, stack agreements,
  deliver the big claim as the obvious conclusion. Companions:
  one desire per video; mechanization (show HOW so they believe
  THAT); redefinition (kill an objection by changing the
  comparison set).
- Hook timing: 1-2 seconds to survive the scroll; the hook must
  land inside the narration's FIRST LINE, not as a separate
  cold-open. Odd-numbered countdowns (3/5/7) outperform even
  ones when a list structure is used.
- Testing is purposeful variation: name the variable being
  tested (hook, format, style), the metric that proves it, and
  what changes next. Never bet a series on one version.
- Variation math for reuse: one concept × 3 hooks × 2 pacing ×
  2 tones = 12 variants; regenerate surgically (a new hook means
  regenerating only the opening, not the whole piece).

### Retention and posting mechanics (Social module)
- Watch time is the #1 metric; if viewers leave at 2 seconds,
  the NEXT video gets fixed, not this one reposted.
- First clip of a video ≤ 3 seconds; a 5-second wait for a
  scene change loses the viewer. On-screen text = reading =
  still watching: our burned-in captions already buy retention.
- The first 1-2 hours after posting decide the push. All
  comment work in that window is LUCKY'S under the work split;
  TheMAN never replies.
- Max 4 hashtags. Post at the same time daily (our calendar
  already fixes the slots). Tick the AI-content label on
  upload: not required for reach, but the safe side.
- Never delete a post (set it private instead); never use
  Promote. The algorithm counts activity, not sentiment —
  corrections and debate push as hard as praise.
- Transferable formats: POV history (the viewer's hands in
  frame; the course's own examples are pyramid-building and a
  witch trial) and personifying an abstract concept as a
  character both fit occult-history subjects directly.

### Flow practice (Advanced Flows module, mapped to Google Flow)
- Build pipelines, not one-offs: connect steps once (image →
  video, the image becomes the start frame automatically), save
  working setups as reusable project templates.
- Run nodes one at a time while testing so the still is approved
  before video cost is committed — the same gate as our stills
  rule. Flow video steps deliberately do not auto-run.
- Reference mechanics: up to 8 image references into one image
  generation (character reference + product/object reference can
  be combined into a third); re-running stacks versions in a
  carousel instead of overwriting — the selected version is what
  flows downstream. Edit changes the current image; Rerun
  recreates from scratch with its references.
- Storyboard/continuation tools exist to kill the "one good
  image, no idea for the next five shots" block: continuations
  extend the story across scenes with subject and style locked.
- MagicFlow discipline: keep the concept prompt SHORT (direction,
  not scene detail); ~5 scenes suffices for a short piece; set
  the aspect ratio at build time; output quality tracks
  reference quality directly.
- Audio usually does NOT chain into the visual flow: voice and
  SFX are created separately and laid in at the final edit —
  which is exactly our ElevenLabs + ffmpeg finish.

### Explicitly NOT adopted from the course
- Planted-mistake comment bait (recommended in the Social
  module for history content): REJECTED. It conflicts with the
  page's source-verified payoff rule. An open question is fine;
  a planted error never is.
- Comment pods, second-account self-debate, keyword-filter
  games: not adopted. Comment work is Lucky's domain and runs
  honestly.
- Face/voice cloning of a real person as presenter (HeyGen,
  Clone Yourself module): not adopted — Rajo stays anonymous,
  no on-camera clone. The module's script and editing craft
  (natural spoken scripts, B-roll over weak sections, 1.1-1.2x
  delivery speed fix) is adopted as technique only.
- Kling, Seedance, HeyGen, Midjourney as tools: not adopted
  (no new subscriptions; Gemini-first + pause rule stands).
  Their transferable techniques are in the sections above.
- Ad funnel mechanics (offers, CTA engineering, paid testing):
  not adopted — the page is not salesy. The transferable script
  and psychology rules are in "Scripts and hooks" above.
- Entertainment-niche formats (stadium cam, anime filmset,
  absurdity prompt packs, celebrity likenesses): not adopted.

## Project overrides (unchanged, win on any conflict)

- Rajo approves the exact text of every post and every finished video
  before posting; no salesy voice; Rajo stays anonymous.
- No new subscriptions: Gemini Pro, ChatGPT Plus, ElevenLabs, free
  tiers only.
- TheMAN never replies to messages/comments and never does the
  30-minute check — Lucky only.
- Captions: CAPTION-METHOD.md (faster-whisper word timings,
  CAP_Y=1320). Narration: no delivery tags, ends with a statement.
