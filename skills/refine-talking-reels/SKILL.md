---
name: refine-talking-reels
description: Refine recorded talking-head footage or recut an existing short vertical reel. Use when the user wants a stronger opening, tighter pacing, a choice between recorded takes, or a story-led edit with subtitles, animated cutaways, and reactions. Hook and pacing fixes can trigger on their own. Not for caption-only work (use embedded-captions), graphic overlays on an untouched cut (use talking-head-recut), standalone motion inserts (use motion-graphics), or shot-for-shot reconstruction (use reverse-any-video).
metadata:
  version: "0.1.0"
---

# refine-talking-reels

Turn existing footage into a coherent, reviewable reel. Own the editorial decisions and final integration; use the available video, caption, image-generation, and rendering tools for their specialties. Do not promise engagement or treat a preset as a substitute for editing judgment.

Use [dependencies.md](references/dependencies.md) to check the chosen workflow's platform, tools, model downloads, and fallback before setup. Read [captions-and-cutaways.md](references/captions-and-cutaways.md) when designing or handing off either layer.

## Local audio processing

- Use file paths for audio and video. In Codex, keep audio bytes on disk unless the current session explicitly supports model audio input. Use `ffprobe` to check for an audio stream and FFmpeg to check that it decodes. A session error such as `Audio input is not available` indicates a rejected model input. If subsequent text-only turns also fail, start in a fresh chat with file paths and transcript text.
- For speech analysis, use a timestamped transcript that matches the source or run local speech-to-text, such as `faster-whisper` with a cached multilingual model. Set the spoken language when known and request word timestamps when the edit or captions need them. Use FFmpeg silence detection to locate candidate pauses and use the transcript to check proposed cuts. If transcription is unavailable or unreliable, flag the affected lines and use a supplied transcript if available. Preserve source dialogue and avoid inventing captions.
- Use local playback for listening checks when it is available. Otherwise, inspect the source and export locally using audio decode, levels, stream timing, and transcript alignment. Report those checks and identify any outstanding listening or language review.

## Inputs and editorial plan

1. Inventory the original media, previous edits, transcript, logo, visual references, and any requested reaction. Probe dimensions, duration, frame rate, audio, and whether captions are already burned in. When choosing among takes, compare the opening, delivery, framing, and pauses. Name the selected take and rebuild cue and insert timings if it changes. Preserve sources and export a new version.
2. Identify the audience, language, platform, target duration, message, speaker's key beats and any explicit constraints. Use any available account analytics to identify a retention problem and make a specific edit decision. For example, early skips favor a clearer opening and less lead-in. Base account-specific claims on the supplied or accessible insights. Infer routine choices and ask only when missing information would change the result. Distinguish reference style from footage the user wants reproduced or inserted.
3. Watch and listen to the source if possible; produce a timestamped transcript and a concise beat map: hook, setup, tension, reveal, conclusion. Mark uncertain words and translation. If listening, language review, or source access is unavailable, say so and avoid claiming an exact match.
4. Make the premise clear within the first three seconds of the reel using a strong recorded line, a concise visual hook, or both. Audition the line in context. Move a later line forward only if it stands on its own and the audio and picture cut cleanly. Keep the realization or emotional payoff in the story, with the setup and breathing room it needs.
5. Plan a short edit decision list mapping source ranges, output ranges, spoken phrases, caption cues, cutaways, and any inserted clip. Remove repetitions, dead air, awkward gaps, and lines that add nothing to the story. Keep intentional pauses and maintain continuity of voice and meaning. Favor natural cuts and use occasional tighter framing or subtle movement when the story calls for it. Keep transitions unobtrusive and respect explicit branding instructions.

## Captions and visuals

6. Distinguish code-switched Tamil-English captions, bilingual subtitles, and English translation of Tamil dialogue. Follow the requested format and preserve code-switching in verbatim captions. Review the transcript and any translation against the audio, including names and implied meaning. Preserve speaker and relevant non-speech information where needed. If language verification is unavailable, flag the affected text as unverified. Retain cue timings and, when useful, export a sidecar SRT/VTT.
7. Time cues to the final cut, including moved lines. When animated captions are requested, carry one recognizable visual treatment across every cue. Use restrained motion for supporting phrases and stronger emphasis for key words. Align translations by spoken phrase and reserve word-level highlighting for timing verified against the spoken words. Review contrast, glyphs, face clearance, platform safe areas, and readability in motion at phone size.
8. Match each cutaway to the line it serves. Choose the number and placement from the story beats and the stretches that need a visual change. When the user wants animated inserts, give each one clear on-screen action. Keep the speaker visible when an expression carries the line. Generate imagery when requested, inspect it, and save selected assets in the project. Use references as inspiration when that is their stated purpose. Identify stills with camera motion, motion graphics, and generated video accurately.
9. For a requested meme or reaction clip, inspect and listen to the actual source, identify the intended phrase and exact in/out times, and note baked-in text. Place it at the story beat; freeze or pause the original only as requested, then resume without losing or overlapping speech. Confirm the excerpt and audio by playback; if the moment cannot be verified, ask for a timestamp or source file rather than guessing. Keep original and extracted media separate.

For a caption or cutaway handoff, use the selected take and final output timeline. Integrate the editable layer or timed asset and recheck timing after further trims.

## Build and review

10. Choose an editable composition workflow suited to the request. For HyperFrames, follow its current composition contract and use its caption and general-video workflows as applicable; FFmpeg is useful for probing, trims, audio and deterministic assembly. Keep a readable timeline and assets with the project. If the caption or render workflow is unavailable, report the limitation instead of claiming it ran.
11. Render a short representative preview when visual direction is uncertain or explicitly requested. Include the opening and, when in scope, a regular caption, an emphasized caption, and an animated cutaway. Incorporate feedback before extending the treatment; do not treat silence as approval when approval is actually required.
12. For Instagram, default to a 9:16 MP4 with H.264 video and AAC audio at 48 kHz. Use 1080 × 1920 when appropriate to the source. Keep dialogue intelligible, avoid clipping, and keep any music below speech. Check the export dimensions, orientation, frame rate, streams, duration, and sync. Follow the [current Meta specs](https://www.postman.com/meta/instagram/folder/830j7my/reels-publishing) when the delivery route has specific limits.
13. Watch the full render with sound. Check the first three seconds, dialogue alignment across trims, caption continuity and readability at phone size, the timing of each insert, and the closing beat. Inspect the first and last frames and listen for clipped words or audible edit seams. If full playback is unavailable, say exactly what was checked and deliver it as a draft.
14. Deliver a link to the new video, its editable project, and any requested caption sidecar or selected images. Report the main changes, source/reference limitations, generated-still status, and any unverified translation, timing, audio, or rights issue. Never publish or send the reel without the user's instruction.
