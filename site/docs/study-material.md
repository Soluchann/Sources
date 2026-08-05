***
***
**[◄◄ Back to Wiki Index](/)**
***
***

# ► Reading

* [PyTorch Internals](https://blog.ezyang.com/2019/05/pytorch-internals/) - Long-form guide to how PyTorch works under the hood
* [Alacritic Super thread](https://x.com/alacritic_super/status/2079548977532571792?s=46) - AI / systems thread to explore
* [LLM Inference Handbook (Modular)](https://handbook.modular.com/) - Glossary, guidebook, and reference for production LLM inference
* [Outperforming cuBLAS on B200](https://www.paulwillchan.com/articles/outperforming-cublas-b200) - Blackwell matmul kernel optimizations vs cuBLAS
* [Quantizing to NF4 with AVX-512](https://www.cudahandbook.com/blog/quantizing-to-nf4-with-avx-512) - Fast NF4 quantization using AVX-512 (CUDA Handbook)
* [Graph Engineering (Andrej Karpathy)](https://drive.google.com/file/d/1-GOg0kxcp8tx1BMUECMj2yJq6JYGmfhb/view) - Graph engineering notes / material
* [Knowledge Graph Course](https://github.com/npubird/KnowledgeGraphCourse) - Southeast University graduate course on knowledge graphs
* [How to Scale Your Model](https://jax-ml.github.io/scaling-book/) - Systems view of LLMs on TPUs (Google DeepMind)
* [How to Think About GPUs](https://jax-ml.github.io/scaling-book/gpus/) - GPU systems chapter from the scaling book
* [Waterloo Intern thread](https://x.com/waterloo_intern/status/2081762065392541951?s=46) - X thread to explore
* [ML Systems Notes](https://github.com/JINO-ROHIT/ml-systems-notes) - Personal notes collection for ML systems
* [AI Engineering Book (Chip Huyen)](https://github.com/chiphuyen/aie-book) - Resources and supporting materials for AI Engineering
* [Seeing Theory](https://seeing-theory.brown.edu/#firstPage) - Visual introduction to probability and statistics
* [GPU Glossary (Modal)](https://modal.com/gpu-glossary) - Glossary of GPU architecture and CUDA concepts
* [tcgen05](https://github.com/sf-tensor/tcgen05) - Bit-level software model of Blackwell Tensor Core MMA arithmetic
* [Mixture-of-Kittens (Cursor)](https://cursor.com/blog/mixture-of-kittens) - Open-source MoE training megakernel for NVL72s

***

# ► LLM Cache Management

* [KV Cache (Hugging Face)](https://huggingface.co/docs/transformers/en/kv_cache) - Transformers KV cache strategies
* [Paged Attention from First Principles](https://hamzaelshafie.bearblog.dev/paged-attention-from-first-principles-a-view-inside-vllm/) - How PagedAttention works inside vLLM
* [Automatic Prefix Caching (vLLM)](https://docs.vllm.ai/en/latest/features/automatic_prefix_caching/) - Reuse KV cache across shared prompt prefixes
* [Continuous Batching (Anyscale)](https://www.anyscale.com/blog/continuous-batching-llm-inference) - Iteration-level batching for higher throughput
* [Looking Back at Speculative Decoding](https://research.google/blog/looking-back-at-speculative-decoding/) - Google Research on speculative decoding
* [KV Cache Quantization (Hugging Face)](https://huggingface.co/blog/kv-cache-quantization) - Compress KV cache for longer generations
* [FlashInfer](https://arxiv.org/abs/2501.01005) - Attention engine paper
* [Zipage](https://arxiv.org/abs/2603.08743) - Compressed PagedAttention paper
* [IceCache](https://arxiv.org/abs/2604.10539) - Memory-efficient KV cache paper
