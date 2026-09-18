<div align="center">
  <img src="https://dwim.sh/hero.png" width="200" alt="dwim logo: a small robot sitting cross-legged, eyes closed, at peace">

# dwim

**A coding agent that runs on your own GPU.**

The agent, the model, and the engine that runs it, in one Rust program:
no API key, no server, and nothing leaves your machine.

[GitHub](https://github.com/dwim-sh/dwim) · [Model: Bonsai 2 27B](https://huggingface.co/prism-ml/Ternary-Bonsai-2-27B-gguf) · [Website](https://dwim.sh/)

</div>

## Getting started

```console
cargo install --git https://github.com/dwim-sh/dwim
dwim
```

The model is downloaded (about 6 GB) on first use. `dwim "what changed in the
last commit?"` answers one thing and exits.

- **A real coding agent.** A shell where the model runs commands, reads their
  output, and keeps going until the task is done. It follows your project's
  `AGENTS.md`.
- **A 27B model in 6 GB.** Bonsai 2 27B, PrismML's ternary version of
  Qwen3.8-27B: every weight is -1, 0, or 1, so it fits on a laptop GPU.
- **Its own inference engine.** No llama.cpp, no CUDA. Metal on macOS, Vulkan
  everywhere else, and a CPU reference the GPU kernels are tested against.

MIT licensed · [github.com/dwim-sh/dwim](https://github.com/dwim-sh/dwim)
