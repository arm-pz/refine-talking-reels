---
name: refine-talking-reels
description: Refine an existing talking-head video into a short vertical reel with translated or animated captions, story-led cutaways, and optional reaction inserts. Use when someone asks to improve, recut, or modernize their spoken reel across several of those elements. Not for caption-only work (use embedded-captions) or recreating another video frame by frame (use reverse-any-video).
metadata:
  version: "0.1.0"
---

# refine-talking-reels

Turn existing footage into a coherent, reviewable reel. Own the editorial decisions and final integration; use the available video, caption, image-generation, and rendering tools for their specialties. Do not promise engagement or treat a preset as a substitute for editing judgment.

## Inputs and editorial plan

1. Inventory the original media, previous edits, transcript, logo, visual references, and any requested reaction. Probe dimensions, duration, frame rate, audio, and whether captions are already burned in. Preserve sources; work from a clean source and export a new version.
2. Identify the audience, language, platform, target duration, message, speaker's key beats and any explicit constraints. Infer routine choices; ask only when missing information would change the result. Distinguish reference style from footage the user wants reproduced or inserted.
3. Watch and listen to the source if possible; produce a timestamped transcript and a concise beat map: hook, setup, tension, reveal, conclusion. Mark uncertain words and translation. If listening, language review, or source access is unavailable, say so and avoid claiming an exact match.
4. Plan a short edit decision list mapping source ranges, output ranges, spoken phrases, caption cues, cutaways, and any inserted clip. Record deliberate pauses and maintain continuity of voice and meaning. Avoid unnecessary logo interruptions; respect explicit branding instructions.

## Captions and visuals

5. For subtitles, distinguish verbatim captions from translated subtitles. Review the source-language transcript and translation against the audio, including names and implied meaning. Preserve speaker and relevant non-speech information where needed. If language verification is unavailable, mark translation as unverified. Retain cue timings and, when useful, export a sidecar SRT/VTT.
6. Design a caption treatment for the footage and tone: legible type, short phrase groups, sufficient contrast, face clearance, and room for platform overlays. Use hierarchy and motion to support speech; do not apply identical exaggerated animation to every phrase. Review animation in motion and test readability on a phone-sized view. For translated subtitles, align phrases to the corresponding spoken meaning; do not present mechanically staggered English words as speech-aligned karaoke.
7. Create a shot-by-shot visual plan: which moments retain the speaker, which use meaningful B-roll or generated stills, and why each cut helps the story. If references are inspiration, do not silently reuse them as final assets. Generate project-bound imagery when requested, inspect it, save selected assets to the project, and keep it coherent with the narrative. A zoom on a still is not generated video; describe the result honestly. Keep key emotional beats visible when that improves the edit.
8. For a requested meme or reaction clip, inspect and listen to the actual source, identify the intended phrase and exact in/out times, and note baked-in text. Place it at the story beat; freeze or pause the original only as requested, then resume without losing or overlapping speech. Confirm the excerpt and audio by playback; if the moment cannot be verified, ask for a timestamp or source file rather than guessing. Keep original and extracted media separate.

## Build and review

9. Choose an editable composition workflow suited to the request. For HyperFrames, follow its current composition contract and use its caption and general-video workflows as applicable; FFmpeg is useful for probing, trims, audio and deterministic assembly. Keep a readable timeline and assets with the project. If the caption or render workflow is unavailable, report the limitation instead of claiming it ran.
10. Render a short representative preview when visual direction is uncertain or explicitly requested. Include a speaker shot, animated captions, a cutaway, and a transition. Incorporate feedback before extending the treatment; do not treat silence as approval when approval is actually required.
11. Render the full edit. Check the complete video in motion with sound, not only isolated frames: first/last frames, cuts, freezes and resumes, voice audibility, translation and cue timing, visual artifacts, contrast, safe areas, and mobile readability. Inspect the exported file's duration, resolution, audio/video streams, and sync. Automated warnings require judgment and correction where real; do not call an unreviewed render verified. If full playback is unavailable, say exactly what was checked and deliver it as a draft.
12. Deliver a link to the new video, its editable project, and any requested caption sidecar or selected images. Report the main changes, source/reference limitations, generated-still status, and any unverified translation, timing, audio, or rights issue. Never publish or send the reel without the user's instruction.
