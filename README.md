# VideoRobot Studio Pro Notebook

This repository tracks the fully refactored **VideoRobot Studio Pro** Colab notebook. The latest build delivers a production-ready workflow that stabilizes environment setup, modularizes media processing, and exposes a streamlined Gradio studio interface.

## Highlights of the Refactor
- **Deterministic bootstrap:** Centralized apt/pip helpers configure locale, encoding, and dependency checks so Colab sessions start reproducibly.
- **Structured workspace:** A `StudioPaths` dataclass standardizes cache, assets, model, and render directories while enforcing consistent seeding and logging.
- **Modular media pipeline:** Dedicated modules cover utilities, asset discovery, audio mastering, Whisper transcription, caption authoring, and FFmpeg rendering for clarity and reuse.
- **Interactive studio UI:** A refreshed Gradio Blocks app reuses the workflow orchestration, safely persists uploads, and reports live progress through a queued launch.
- **Font-aware rendering:** Caption styling now validates local font availability, lets you upload custom families, and refreshes the font cache automatically so FFmpeg subtitles stay on-brand.

## Usage
1. Open `VideoRobot_Studio_Pro (1).ipynb` in Colab or Jupyter.
2. Run the cells sequentially under Python 3.12+; each cell is self-contained and ends with a ✅ marker when it finishes successfully.
3. Use the final Gradio interface to select or upload audio/background assets, tweak Whisper and rendering options, and launch renders.

The notebook compiles cell-by-cell under Python 3.12+ and is tuned for "studio-ready" reliability, determinism, and maintainability.
