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
