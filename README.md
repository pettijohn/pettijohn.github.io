# Travis Pettijohn - GitHub Portfolio
[https://linkedin.com/in/pettijohn](https://linkedin.com/in/pettijohn)

## Linux Kernel Module & Userspace app in Rust
- [https://github.com/pettijohn/corsair-ai-workstation-performance-level-linux](https://github.com/pettijohn/corsair-ai-workstation-performance-level-linux)
- Reverse engineered a Windows-only driver for a desktop PC's performance level button to replicate on Ubuntu 26.04 with 7.0 kernel.
- 100% Rust. Extremely efficient.

## Whisrs Voice Dictation 
- [https://github.com/y0sif/whisrs/pull/50](https://github.com/y0sif/whisrs/pull/50)
- Whisrs is a Linux-native voice dictation software in Rust with support for multiple speech recognition providers including cloud and local.
- Pull request added support for realtime dictation for OpenAI-compatible endpoints, namely [Lemonade](https://lemonade-server.ai/docs/api/openai/). 
- Before this PR, the app supported realtime for OpenAI cloud dictation, or batch transcription (process the whole recording when recording stops) for OpenAI-compatible, or realtime with Whisrs-hosted whisper.cpp ([CPU-only](https://github.com/y0sif/whisrs/issues/48)).
- Pull request refactored OpenAI realtime transcription to a shared component that OpenAI-native and OpenAI-compatible can use.
- Added over 100 unit tests. 
- End result: realtime, fully-local, fully-private, GPU-accelerated voice transcription for Linux in Rust.
- Merged and released in [v0.1.19](https://github.com/y0sif/whisrs/releases/tag/v0.1.19).
