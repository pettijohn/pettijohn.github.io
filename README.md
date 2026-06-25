# Travis Pettijohn - GitHub Portfolio
[https://linkedin.com/in/pettijohn](https://linkedin.com/in/pettijohn)

## Rust Linux Kernel Driver for Corsair AI Workstation Performance Selector
- [https://github.com/pettijohn/corsair-ai-workstation-performance-level-linux](https://github.com/pettijohn/corsair-ai-workstation-performance-level-linux)
- Developed a Rust Linux kernel module that integrates unsupported Corsair workstation firmware controls with Linux via ACPI/WMI and sysfs.
- Reverse-engineered WMI method/event payloads to decode real-time performance states: Quiet, Balanced, Max, and Super.
- Built an event-driven GNOME status indicator that blocks on kernel notifications instead of polling, using ~4.8 MB RSS and 0% idle CPU in validation.
- Added production-minded tooling: Secure Boot module signing, MOK enrollment flow, install/uninstall scripts, kernel Rust toolchain checks, and dev-containerized builds.
- Designed a small no_std-friendly Rust decode crate with testable firmware parsing logic separated from kernel integration.

## Whisrs Voice Dictation 
- [https://github.com/y0sif/whisrs/pull/50](https://github.com/y0sif/whisrs/pull/50)
- Whisrs is a Linux-native voice dictation software in Rust with support for multiple speech recognition providers including cloud and local.
- Pull request added support for realtime dictation for OpenAI-compatible endpoints, namely [Lemonade](https://lemonade-server.ai/docs/api/openai/). 
- Before this PR, the app supported realtime for OpenAI cloud dictation, or batch transcription (process the whole recording when recording stops) for OpenAI-compatible, or realtime with Whisrs-hosted whisper.cpp ([CPU-only](https://github.com/y0sif/whisrs/issues/48)).
- Pull request refactored OpenAI realtime transcription to a shared component that OpenAI-native and OpenAI-compatible can use.
- Added over 100 unit tests. 
- End result: realtime, fully-local, fully-private, GPU-accelerated voice transcription for Linux in Rust.
- Merged and released in [v0.1.19](https://github.com/y0sif/whisrs/releases/tag/v0.1.19).

## TaskSchedulerEngine (2011 through 2026)

- [https://github.com/pettijohn/TaskSchedulerEngine](https://github.com/pettijohn/TaskSchedulerEngine)
- Built a lightweight C#/.NET scheduling engine with cron-like rules, second-level precision, timezone support, async callbacks, graceful shutdown, and retry behavior.
- Designed a fluent scheduling API plus cron parsing, giving consumers an ergonomic way to define recurring or one-shot tasks without heavyweight scheduler infrastructure.
- Implemented a high-performance rule evaluator that compiles schedules into bit masks for fast per-second matching with minimal allocations.
- Architected a thread-safe evaluation pump that dispatches matching tasks asynchronously, tracks running callbacks, isolates failures, and handles missed-second catch-up behavior.
- Modernized the project for .NET 8, 9, and 10 with cross-targeted automated tests covering parsing, concurrency, retries, shutdown, and scheduler edge cases.

## Portfolio Drawdown Monte Carlo 

- [https://pettijohn.github.io/PortfolioDrawdownMonteCarlo/](https://pettijohn.github.io/PortfolioDrawdownMonteCarlo/) and [source code](https://github.com/pettijohn/PortfolioDrawdownMonteCarlo)
- Algorithm computes probability that a given portfolio shape will last through retirement, when retiree is in drawdown phase and not earning income. 
- Kept skills sharp, writing the algorithm in C#, Rust, Go, and TypeScript, plus a web basic UI. All but TypeScript used parallel programming on this CPU-bound algorithm. 
- Wrote code by hand in 2022. 
- In 2026, AI-assisted to run all in WASM in the browser, including parallel multi-threaded WebWorkers. 

## Microsoft Kiota (2024)

- Kiota generates strongly-typed API clients from OpenAPI specs in multiple  languages. 
- Fixed an inheritance bug in generated C# classes where some generated classes were "squashed" (removed the inheritance and flattened properties) while others inherited. [PR 5123](https://github.com/microsoft/kiota/pull/5123), fixing bug [5041](https://github.com/microsoft/kiota/issues/5014).