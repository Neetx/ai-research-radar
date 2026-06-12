# Library — worth studying

Curated shelf for an AI researcher / AI-systems engineer / daily AI practitioner:
projects, papers and concepts worth knowing, picked during scans. Unlike the
trend ledger, a single strong artifact qualifies — but only opened, primary
sources enter. Newest first; pruned weekly.

- 2026-06-12 — [vLLM `turboquant` module](https://docs.vllm.ai/en/latest/api/vllm/model_executor/layers/quantization/turboquant) (docs/code) — KV-cache vector quantization inside a mainstream serving engine; read next to the TurboQuant paper to see the research→production distance
- 2026-06-12 — [RecursiveMAS](https://github.com/RecursiveMAS/RecursiveMAS) (code) — reference implementation of latent-space multi-agent computation, with checkpoints over Qwen/Llama/Gemma that make it reproducible on modest hardware
- 2026-06-12 — [Cache-to-Cache (C2C)](https://arxiv.org/abs/2510.03215) (paper, ICLR'26) — the cleanest formulation of direct KV-cache communication between different LLMs
- 2026-06-12 — [ExLlamaV3 / EXL3](https://github.com/turboderp-org/exllamav3) (code) — production trellis-coded quantization (QTIP-derived) on consumer GPUs; the format to study to understand where weight quantization is heading
- 2026-06-12 — [bitnet.cpp](https://github.com/microsoft/BitNet) (code) — the official ternary-LLM inference stack; the practical entry point to 1-bit models on CPU
- 2026-06-12 — [Design Patterns for Securing LLM Agents](https://arxiv.org/abs/2506.08837) (paper) — the reference catalogue of injection-resistant agent architectures; required reading before building any tool-using agent
- 2026-06-12 — [Claude Code Agent Teams](https://code.claude.com/docs/en/agent-teams) (docs) — first mainstream built-in multi-agent orchestrator; the shared-task-list + mailbox architecture is a pattern worth studying regardless of vendor
