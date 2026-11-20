# Trigger and boundary cases

These are manual description checks, not independent agent evaluations.

| # | Request | Expected routing | Pass condition |
|---|---|---|---|
| 1 | Improve my talking-head reel with captions and cutaways. | refine-talking-reels | Plans and integrates both. |
| 2 | Modernize this vertical interview with animated subtitles and reaction clips. | refine-talking-reels | Plans a multi-element recut and verifies the reaction. |
| 3 | Turn my spoken video into an English-subtitled reel with AI visuals. | refine-talking-reels | Treats translation and visual generation as separate checks. |
| 4 | The speaker stays on screen too long and the text feels dated. | refine-talking-reels | Proposes story-led visual and caption edits. |
| 5 | My short video feels like a slideshow; make the storytelling stronger. | refine-talking-reels, if spoken footage | Inspects the source and plans cutaway rhythm. |
| 6 | Add captions to this talking head without editing the video. | embedded-captions | Does not alter the cut. |
| 7 | Recreate this reference video shot for shot. | reverse-any-video | Routes to reconstruction rather than a new edit. |
| 8 | Generate one thumbnail for my reel. | imagegen | Produces an image; does not recut video. |
| 9 | Write a script for a reel, no footage yet. | writing/script workflow | Does not pretend to edit an absent video. |
| 10 | Add a meme to my existing reel, preserving the rest. | video-editing or FFmpeg; refine-talking-reels if broader recut requested | Changes only the requested passage. |
| 11 | The first three seconds are weak. Can you find a better opening somewhere in the recorded take? | refine-talking-reels | Auditions recorded dialogue and keeps the payoff intact. |
| 12 | This reel drags, but give the realization a moment to land. | refine-talking-reels | Removes repetition and dead air while retaining the setup and deliberate pause. |
| 13 | Cut the slow bits from this Tamil-English reel, then retime the subtitles. | refine-talking-reels | Owns the cut and passes the final timeline and transcript into caption work. |
| 14 | Keep the cuts and audio as they are. Add lower-thirds and quote cards to my talking-head reel. | talking-head-recut | Adds synced graphics over the existing cut. |
| 15 | Check these Tamil-English subtitles for timing and keep the video edit as is. | embedded-captions | Revises only the subtitle layer. |
| 16 | Reframe the shot tighter on the reveal and shorten the setup, keeping the dialogue natural. | refine-talking-reels | Integrates the story cut and framing change. |
| 17 | My analytics show people skip in the first few seconds and these cutaways feel like a slideshow. Recut the reel. | refine-talking-reels | Uses the supplied retention evidence to strengthen the opening and replaces still-only moments with timed actions where they serve the story. |
| 18 | Tighten this cut and fix the animated subtitles that go plain halfway through. | refine-talking-reels | Carries a consistent treatment across all cues and retimes them to the new edit. |
| 19 | Here are two takes of the same reel. Pick the better take and add translated captions and animated inserts. | refine-talking-reels | Names the selected take and times both layers against its edit. |
| 20 | Make a two-second animation of a chat draft typing and deleting. I only need the insert. | motion-graphics | Delivers a standalone motion asset. |
| 21 | Keep my cut exactly as it is and make these subtitles less plain. | embedded-captions | Changes only the caption treatment and preserves the existing cut. |
