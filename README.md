# refine-talking-reels

An agent skill for refining existing talking-head footage into a vertical reel with animated or translated subtitles, story-led cutaways, and optional reaction inserts. It coordinates the edit and calls out unverified translation, timing, or playback.

Once this skill is merged, install it with:

```sh
npx skills add arm-pz/refine-talking-reels --skill refine-talking-reels
```

Ask it things like:

- “Improve my talking-head reel with animated subtitles and relevant cutaways.”
- “Use generated visuals for the story, and keep me on screen for the reveal.”
- “Add this reaction clip over a freeze frame without losing the next line.”

The skill works with existing video, caption and image-generation tools available to the agent. `embedded-captions` is the better fit for caption-only changes; `reverse-any-video` is for shot-for-shot reconstruction. Tool availability and results depend on the host environment.

The [trigger cases](tests/trigger-cases.md) are written examples, not results from independent agent evaluations. The skill was developed from a real reel-editing session; the earlier output used cue-level English timing and was not fully reviewed with sound. The workflow explicitly calls for those checks on future edits.
