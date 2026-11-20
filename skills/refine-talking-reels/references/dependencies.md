# Dependencies by workflow

Choose the editing path first. Check that its tools and assets are available before running setup or starting a render.

| Workflow | Requirements |
| --- | --- |
| Local media edit and export | `ffmpeg` and `ffprobe` on PATH. Check for the required filters and encoders, including H.264 and AAC for the standard Instagram export. |
| Local speech-to-text, when needed | A timestamped transcript from the same take can be used directly. To generate one with `faster-whisper`, use Python and a compatible multilingual model. The offline path requires cached model weights. A first model download needs network access. |
| Local styled subtitles | FFmpeg built with `libass`, an editable ASS subtitle file, and installed fonts that cover the selected language. Check that Tamil and Latin glyphs shape correctly in the actual render. |
| HyperFrames embedded captions | HyperFrames CLI, Node.js, Bash, FFmpeg and ffprobe. The documented local preview helpers use Chromium via Puppeteer, Sharp, and GSAP. The transcription path may use WhisperX through `uvx`. Automatic transcription and subject matting may download model weights on first use. Follow the installed skill's runtime and platform guidance. |
| Animated cutaways | The tested Windows path uses Python, Pillow, NumPy, and FFmpeg. The PXL_2-style behind-speaker title also uses OpenCV for the foreground mask. Use installed fonts for drawn text. The installed HyperFrames `motion-graphics` workflow documents macOS on Apple Silicon and Linux x64, with Node.js and FFmpeg. |
| Image generation, when requested | Use the built-in ImageGen tool where available. It requires no API key. The optional ImageGen CLI uses `OPENAI_API_KEY` and requires the user's explicit request or approval. Keep selected assets with the edit. |
| Account analytics, when available | Use insights the user provides or that the session can access. Editing from those insights needs no Instagram API key. |

Keep raw audio on disk unless the current session explicitly supports model audio input. Pass file paths and timed transcript text between steps. If local transcription is unavailable, use a supplied transcript where possible and flag missing or uncertain language review. If a specialist workflow or platform is unavailable, use a compatible local renderer that can deliver the requested result and report any remaining limitation.
