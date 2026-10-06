### Yi Hou (厚熠)

Second-year AI undergraduate at UCAS. I build language-model systems from scratch and report what the measurements say.

**[llm-from-scratch](https://github.com/Helios-YQH/llm-from-scratch)** — the full LLM stack in one monorepo: BPE → Transformer → Triton kernels → DDP / ZeRO-1 / FSDP → a Common Crawl pipeline → SFT / DPO / GRPO. Four projects, five technical reports — the GRPO study is now an [arXiv preprint](https://arxiv.org/abs/2610.04928).

Selected findings:

- 5.7× attention speedup at 64K context — hand-written Triton FlashAttention-2, and fp32 64K contexts run where naive attention OOMs
- −43% training memory from a from-scratch FSDP, cross-checked against PyTorch's
- GRPO at 1B: the prompt outweighs the estimator, and a 10%-flipped verifier costs RL almost nothing where best-of-32 selection keeps only 57% of its gain — [arXiv:2610.04928](https://arxiv.org/abs/2610.04928)
- AlpacaEval: the judge outweighs the model — the same three models span 3.8–9.4% or 26–33% win rate depending on who judges them

Also: [diffusion-from-scratch](https://github.com/Helios-YQH/diffusion-from-scratch) · [jittor-competition-point-cloud](https://github.com/Helios-YQH/jittor-competition-point-cloud) (top 100 of 3,668) · [lab-report](https://github.com/Helios-YQH/lab-report)

[helios-yqh.github.io](https://helios-yqh.github.io) · houyi25@mails.ucas.ac.cn
