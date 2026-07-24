# Sources Sections Design

**Date:** 2026-07-24  
**Repo:** Soluchann/Sources  
**Status:** Approved

## Goal

Keep the existing FMHY-style category index and add curated personal sections for UI tools, AI tools, and study material.

## Constraints

- Preserve all existing FMHY sections and links unchanged.
- Match FMHY markdown style: `#` headings with emoji, short bold blurb, `***` separators.
- Keep `README.md` and `fmhy.md` in sync (identical content).
- Place new sections after **Miscellaneous** and before **Changelog**.

## Sections

### UI tools

Emoji/title: `🎨 UI tools` (heading links to Canvas UI).  
Blurb: Canvas / WebGL UI libraries and components.

Entries:

- Canvas UI — https://canvasui.dev/
- HeroUI — https://github.com/heroui-inc/heroui
- ASCII Effect (Componentry) — https://componentry.dev/docs/components/ascii-effect

### AI tools

Emoji/title: `✨ AI tools` (plain heading; avoids clash with existing `🤖 Artificial Intelligence`).  
Blurb: Local agents, AI canvases, and related tools.

Entries:

- Penecho — https://github.com/penecho/penecho
- Atomic Agent — https://github.com/AtomicBot-ai/atomic-agent

### Study material

Emoji/title: `📖 Study material`.  
Blurb: Articles, threads, and deep dives worth reading.

Top-level entries:

- PyTorch Internals — https://blog.ezyang.com/2019/05/pytorch-internals/
- Alacritic Super thread — https://x.com/alacritic_super/status/2079548977532571792?s=46

Nested group `### LLM Cache Management`:

- KV Cache (Hugging Face) — https://huggingface.co/docs/transformers/en/kv_cache
- Paged Attention from First Principles — https://hamzaelshafie.bearblog.dev/paged-attention-from-first-principles-a-view-inside-vllm/
- Automatic Prefix Caching (vLLM) — https://docs.vllm.ai/en/latest/features/automatic_prefix_caching/
- Continuous Batching (Anyscale) — https://www.anyscale.com/blog/continuous-batching-llm-inference
- Looking Back at Speculative Decoding — https://research.google/blog/looking-back-at-speculative-decoding/
- KV Cache Quantization (Hugging Face) — https://huggingface.co/blog/kv-cache-quantization
- FlashInfer — https://arxiv.org/abs/2501.01005
- Zipage — https://arxiv.org/abs/2603.08743
- IceCache — https://arxiv.org/abs/2604.10539

## Out of scope

- Restructuring or replacing FMHY sections
- Building a site/app; markdown-only updates
- Deduplicating `README.md` / `fmhy.md` into a single source of truth
