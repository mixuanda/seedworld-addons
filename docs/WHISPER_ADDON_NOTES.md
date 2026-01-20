# Whisper Add-on Notes

## Components

1. **whisper.cpp binary**: the local inference engine that runs on the user's machine.
2. **GGML model files**: the actual Whisper model weights used for transcription.

## Recommended starting models

- **tiny**: fastest and smallest; best for quick tests.
- **base**: balanced speed and accuracy.
- **small**: higher accuracy with increased compute cost.

## Upstream context

OpenAI Whisper is the upstream model research and training source, while **whisper.cpp** provides the local inference implementation optimized for CPU usage.
