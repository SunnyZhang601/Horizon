---
layout: default
title: "Horizon Summary: 2026-10-17 (EN)"
date: 2026-10-17
lang: en
---

> From 69 items, 8 important content pieces were selected

---

**Technology News**
1. [Claude traces NIST elliptic-curve seeds to lrand48 RNG outputs](#item-tech-news-1) ⭐️ 8.0/10
2. [Big Fish: exploiting a 37-year-old OpenBSD kernel bug](#item-tech-news-2) ⭐️ 8.0/10
3. [ORL claims 2,788 tokens/s diffusion LLM decoding on one RTX 5090](#item-tech-news-3) ⭐️ 8.0/10
4. [StepFun releases Step 5 Preview agent flagship model](#item-tech-news-4) ⭐️ 8.0/10
5. [NVIDIA Details 2.8-Trillion-Token Indic Pretraining With Open Data Pipeline](#item-tech-news-5) ⭐️ 7.0/10
6. [Kernel Rust proposal targets safe self-referential structures via pin\_init](#item-tech-news-6) ⭐️ 6.0/10
7. [Linux NFS server changes outlined at Linux Plumbers Conference](#item-tech-news-7) ⭐️ 6.0/10

**Financial News**
1. [China Proposes Export Controls on 40 AI, Biotech and Solar Technologies](#item-finance-news-1) ⭐️ 8.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Claude traces NIST elliptic-curve seeds to lrand48 RNG outputs](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 8.0/10

An Anthropic research post reports that Claude traced the origins of the NIST P-192, P-224, P-256, P-384, and P-521 elliptic-curve seeds to outputs of the C library&\#x27;s lrand48 random-number generator, seeded with Unix timestamps. The report says none of those seeds came from a hash algorithm. One binary seed, B-163, remains unexplained. Commenters stressed that the finding identifies the generation method but does not prove the curves were not deliberately selected, because discarded candidates from the generation process cannot be inspected.

hackernews · ahlCVA · Oct 16, 18:55 · [Discussion](https://news.ycombinator.com/item?id=50122800)

**「Background」** The seeds behind NIST&\#x27;s standard elliptic curves have long been a focus of cryptographic suspicion because they were meant to show the curves were generated verifiably, yet nobody had established how the seed numbers themselves were produced. Anthropic&\#x27;s report says its analysis matched five NIST prime-curve seeds—and five ANSI X9.62 seeds—to outputs of the C library&\#x27;s lrand48 generator, with a recovered 48-bit generator state regenerating the entire 160-bit seed.

**「Impact」** The result does not demonstrate a break or weakness in the NIST P-curves, so users do not have a compatibility or migration action from this finding alone; the unresolved trust question is whether the seed-generation process allowed deliberate selection.

**「Community discussion」** Commenters broadly treated the finding as resolving the generation method, but fidotron cautioned that it says nothing about how the curves were selected, especially since candidates generated and discarded over months cannot be inspected. teddyh suggested the unexplained B-163 seed may have been generated the same way but mistyped before publication, which would prevent a match.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>
<li><a href="https://dzen.ru/a/atJ62LttX1YBcpwi">Claude восстановила происхождение пяти кривых ECDSA ... | Дзен</a></li>

</ul>
</details>

**Tags**: `#cryptography`, `#elliptic curves`, `#AI research`, `#NIST standards`, `#cybersecurity`

---

<a id="item-tech-news-2"></a>
### [Big Fish: exploiting a 37-year-old OpenBSD kernel bug](https://calif.io/research/big-fish) ⭐️ 8.0/10

A research write-up published at calif.io, &quot;Big Fish,&quot; demonstrates exploitation of a kernel bug that the author says went undetected in OpenBSD for 37 years. Commenters on the item add that the same code was rewritten in NetBSD in August 1999, where the flaw was reportedly fixed by accident, leaving OpenBSD affected. The surrounding debate is about detection method rather than impact: whether code review should have caught it, and whether fuzzing or static analysis could realistically find this class of bug.

hackernews · rs\_rs\_rs\_rs\_rs · Oct 16, 14:44 · [Discussion](https://news.ycombinator.com/item?id=50118977)

**「Background」** The write-up traces the faulty kernel field back roughly 37 years to original BSD source code, so the &quot;37-year-old&quot; framing describes the age of the inherited code path rather than a modern OpenBSD kernel that has existed that long unchanged. The bug is a privilege-escalation issue: Calif reports gaining root on OpenBSD through it, and notes that it publishes offensive research while generally keeping its defensive work — remediation help, patch generation, and cryptographic improvements for open source projects — out of the spotlight.

**「Impact」** Because the published proof-of-concept chains a roughly 37-year-old integer overflow with a separate kernel flaw to gain root on OpenBSD 7.9, the defenses many administrators count on — KARL kernel-address randomization and the SMAP and SMEP hardware protections — do not stop this path. The exploit is a local privilege escalation, so the immediate exposure is to hosts where an attacker already holds an unprivileged account or code execution; the flaws have since been patched, making an update the practical mitigation rather than treating KARL, SMAP, and SMEP as sufficient.

**「Community Discussion」** One commenter praised the write-up&\#x27;s graphics as a riff on OpenBSD release artwork, while another noted the flaw was accidentally fixed in NetBSD during an August 1999 rewrite of that code. A third commenter argued that a bug surviving 37 years in a heavily audited codebase shows how hard some kernel bugs are to catch by review alone, and asked whether fuzzing or static analysis could realistically have found it or whether a human reasoning about the exploit primitive was required — a question the supplied comments leave unresolved.

<details><summary>References</summary>
<ul>
<li><a href="https://calif.io/research/big-fish">Big Fish : Exploiting a 37 - Year - Old Kernel Bug in OpenBSD | Calif</a></li>
<li><a href="https://dzen.ru/a/atJi8f5wA2igUvxy">Calif получила root в OpenBSD через 37 -летнюю ошибку ядра | Дзен</a></li>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://thehackernews.com/2026/10/researchers-demonstrate-openbsd-root.html">Researchers Demonstrate OpenBSD Root Exploit Chaining 37-Year ...</a></li>
<li><a href="https://thedailytechfeed.com/37-year-old-kernel-bug-in-openbsd-finally-patched-after-root-exploit-poc/">37-Year-Old Kernel Bug in OpenBSD Finally Patched After Root ...</a></li>

</ul>
</details>

**Tags**: `#OpenBSD`, `#kernel security`, `#vulnerability research`, `#exploit development`, `#operating systems`

---

<a id="item-tech-news-3"></a>
### [ORL claims 2,788 tokens/s diffusion LLM decoding on one RTX 5090](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

A Reddit research post introduces ORL \(On-Policy Residual Learning\) and a companion inference engine, dlmrt, for speeding up diffusion language model decoding, claiming 2,788 tokens/s for LLaDA-2.1-mini + ORL in NVFP4 on a single RTX 5090 and 7,708 tokens/s for DiffusionGemma 26B MoE + ORL in NVFP4 on 8× B200. The authors also report up to 6.9× higher end-to-end throughput on their QwenDLM-4B model, and 1.74× faster than DFlash speculative decoding at matched accuracy in a single-request H100 comparison. These are self-reported figures from the post, measured at batch size 1 \(single-request decoding\) and described as peak results on specific benchmarks rather than averages across arbitrary prompts. Models, training code, evaluation pipeline, and the dlmrt engine are released openly, with checkpoints published on Hugging Face.

reddit · r/MachineLearning · /u/arty\_photography · Oct 16, 20:03

**「Background」** Diffusion language models \(dLLMs\) generate text by iteratively denoising a sequence, refining many token positions in parallel across multiple forward passes, unlike autoregressive models that emit one token per pass. Their practical cost therefore hinges on how many tokens the model can finalize per forward pass, and ORL&\#x27;s premise is that the residual context carried between denoising steps is inherently on-policy — so training on model-induced residual trajectories, rather than stale offline residuals, is what allows more tokens to be committed per pass without degrading output quality.

**「Impact」** Because the LLaDA-2.1-mini ORL NVFP4 checkpoint is positioned to run on an RTX 5090 via dlmrt, readers with consumer Blackwell hardware can attempt to reproduce the single-request latency claim themselves. The engine&\#x27;s reported 1.2–1.6× advantage over SGLang/vLLM and the 1.74× comparison against DFlash were measured only in single-H100 setups, so behavior on other GPUs, with other models, or under concurrent batching is untested in the supplied account.

<details><summary>References</summary>
<ul>
<li><a href="https://arxivb.org/abs/2610.20687">On-Policy Residual Learning for Diffusion Language Models</a></li>

</ul>
</details>

**Tags**: `#diffusion language models`, `#LLM inference`, `#speculative decoding`, `#open source`, `#GPU performance`

---

<a id="item-tech-news-4"></a>
### [StepFun releases Step 5 Preview agent flagship model](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 8.0/10

StepFun released Step 5 Preview on Hugging Face, a flagship sparse mixture-of-experts model targeting agentic work. It has 600 billion total parameters with 27 billion active, supports up to 1 million tokens of context, and accepts text, image, and video input. The model can be deployed through an OpenAI-compatible API using vLLM or SGLang under the StepFun Model License 1.0. StepFun claims leading performance in software engineering, long-horizon agent execution, and professional knowledge tasks, especially finance, but those claims are unverified for this preview release.

telegram · zaihuapd · Oct 16, 06:36

**「Background」** Sparse mixture-of-experts \(MoE\) models keep a large total parameter count while routing each token through only a small subset of experts, so Step 5 Preview&\#x27;s 600B total and 27B active parameters describe two different quantities: stored model capacity versus the compute used per token. StepFun&\#x27;s model card lists this architecture alongside a context window of up to 1M tokens, which is the basis for the deployment trade-off the release is built around.

**「Impact」** Developers evaluating agent models can deploy Step 5 Preview through OpenAI-compatible vLLM or SGLang endpoints, and StepFun claims its per-task cost is one-eighth that of Claude Opus 5 — a vendor figure that teams should validate against their own workloads before migrating. Reported results give it 67.7% on the DeepSWE v1.1 software-engineering benchmark, slightly above Kimi K3 and GLM-5.3, though coverage notes that coding-agent competition is not settled by single-turn benchmark scores.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/stepfun-ai/Step-5-Preview">stepfun -ai/ Step - 5 - Preview · Hugging Face</a></li>
<li><a href="https://www.eesel.ai/blog/stepfun-step-5">StepFun Step 5 Preview : specs, pricing, benchmarks, and... | eesel AI</a></li>
<li><a href="https://blog.margrop.net/post/step-5-preview-sparse-moe-agentic-model/">600B 参数仅激活 27B，单任务成本狂砍 8 倍！ 阶 跃 星 辰 Step ...</a></li>
<li><a href="https://m.21jingji.com/article/20260921/herald/742325e7deb08d056e5801bcae9c9974.html">“单任务成本仅为Claude Opus 5的1/8”， 阶 跃 星 辰 Step 5 Preview ...</a></li>

</ul>
</details>

**Tags**: `#large language models`, `#mixture-of-experts`, `#AI agents`, `#multimodal models`, `#StepFun`

---

<a id="item-tech-news-5"></a>
### [NVIDIA Details 2.8-Trillion-Token Indic Pretraining With Open Data Pipeline](https://huggingface.co/blog/nvidia/scaling-indic-pretraining) ⭐️ 7.0/10

NVIDIA published a Hugging Face blog post describing a large-scale Indic-language pretraining effort built on 2.8 trillion tokens, paired with an open data generation pipeline. The open pipeline is the component most relevant to multilingual and data-centric LLM research, since it is presented as a reusable way to generate pretraining data rather than only a finished model. The supplied material contains no source content, model card, license terms, or independent measurement, so the token count and the extent of the pipeline&\#x27;s openness remain vendor claims as described in the blog.

rss · Hugging Face Blog · Oct 16, 01:44

**「Background」** The corpus, named Nemotron-pretraining-Indic-v1, is a joint effort between NVIDIA, IIT Madras&\#x27;s AI4Bharat lab and Bodhan AI, and spans 22 Indian languages — all in native script, with romanized text for twelve of them. Reporting around the announcement describes the roughly 2.8 trillion-token corpus as releasing soon alongside the open, GPU-accelerated data generation pipeline used to build it, rather than as an already-downloadable dataset.

**「Impact」** Developers building Indian-language models can work from the released Nemotron-pretraining-Indic-v1 corpus of about 2.8 trillion tokens spanning 22 scheduled languages, and can use the accompanying open, GPU-accelerated pipeline to generate additional training data instead of being limited to a fixed dataset. The practical requirement for that extension work is access to GPU capacity described in the pipeline, since the generation step, not just the published tokens, is what is being opened.

<details><summary>References</summary>
<ul>
<li><a href="https://daily.dev/posts/scaling-indic-pretraining-2-8-trillion-tokens-and-an-open-data-generation-pipeline-gngeiqcjb">Scaling Indic Pretraining: 2.8 Trillion Tokens and an Open ...</a></li>
<li><a href="https://www.unite.ai/nvidia-unveils-2-8t-token-indic-pretraining-corpus-and-open-pipeline/">NVIDIA Unveils 2.8T-Token Indic Pretraining Corpus and Open ...</a></li>
<li><a href="https://www.explainx.ai/blog/nvidia-indic-pretraining-2-8-trillion-tokens-open-pipeline-2026">Nemotron Indic Pretraining: 2.8T Tokens, 22 Languages ...</a></li>
<li><a href="https://www.printingpressai.com/article/generative-ai/scaling-indic-pretraining-2-8-trillion-tokens-and-an-open-data-generation-pipeli">Scaling Indic Pretraining: 2.8 Trillion Tokens and an Open ...</a></li>

</ul>
</details>

**Tags**: `#AI`, `#LLM pretraining`, `#multilingual NLP`, `#open data`, `#Indic languages`

---

<a id="item-tech-news-6"></a>
### [Kernel Rust proposal targets safe self-referential structures via pin\_init](https://lwn.net/Articles/1099224/) ⭐️ 6.0/10

At Kangrejos 2026, Gary Guo presented a technique for building self-referential data structures in kernel Rust without unsafe code, based on the kernel&\#x27;s pin\_init crate, which is used to create immovable data structures for C interoperability. Guo claimed the approach could eliminate most unsafe code related to lifetimes in the Nova GPU driver and, eventually, other Rust components. The available source is a short LWN teaser with no mechanism, implementation detail, or measured results, so this is a proposed approach rather than a demonstrated or merged capability.

rss · LWN.net · Oct 16, 18:30

**「Background」** The kernel&\#x27;s pin\_init crate exists to initialize pinned data structures safely: annotating a struct with \#\[pin\_data\] and using the pin\_init\! macro lets it be constructed in place, which matters because Rust&\#x27;s pinning guarantees a value stays at the same memory address from the time it is pinned until it is dropped \(tool-2-1, tool-2-2\). Self-referential structs — those holding a pointer back into themselves — are the simplest kind of address-sensitive type, and they are the reason such a no-move guarantee is needed \(tool-2-2\). pin\_init is already used on the Rust side for kernel sync structures that wrap self-referential C structs \(tool-2-2\).

**「Impact」** If the pin\_init-based technique holds up, Nova driver developers could remove much of the unsafe code tied to lifetimes — code that the driver&\#x27;s own guidelines say should be avoided or isolated behind a safe API, which would shrink the surface needing manual safety review. The talk describes a proposed approach rather than a measured or merged result, so any reduction in Nova&\#x27;s unsafe code depends on the changes being adopted.

<details><summary>References</summary>
<ul>
<li><a href="https://rust.docs.kernel.org/pin_init/">pin_init - Rust</a></li>
<li><a href="https://doc.rust-lang.org/std/pin/?example-self-referential-struct">std::pin - Rust pin_init - Rust - Docs.rs kernel::init - Rust linux/rust/kernel/init.rs at master · torvalds/linux · GitHub init.rs - source - The Linux Kernel Archives rust: pin-init: create self references safely - lwn.net</a></li>
<li><a href="https://rust-for-linux.com/nova-gpu-driver">Nova GPU Driver - Rust for Linux</a></li>
<li><a href="https://github.com/torvalds/linux/blob/master/Documentation/gpu/nova/guidelines.rst">linux/Documentation/gpu/nova/guidelines.rst at master ...</a></li>

</ul>
</details>

**Tags**: `#Rust`, `#Linux kernel`, `#Rust for Linux`, `#memory safety`, `#GPU drivers`

---

<a id="item-tech-news-7"></a>
### [Linux NFS server changes outlined at Linux Plumbers Conference](https://lwn.net/Articles/1098611/) ⭐️ 6.0/10

At the 2026 Linux Plumbers Conference, NFS developer Jeff Layton presented an overview of recent enhancements to the Linux NFS server implementation and indicated what is planned for the near future. The talk framed these changes as part of the protocol&\#x27;s continued evolution, which requires implementations to keep pace. The available summary of the session does not specify individual features, versions, or release timelines, so concrete details of the recent and forthcoming work are not yet established here.

rss · LWN.net · Oct 16, 14:26

**「Background」** NFS is a long-standing network filesystem protocol on Unix-like systems, and Linux implements both the client and server in the kernel, so its capabilities change incrementally with each kernel release. One concrete recent step reported by Phoronix: during the Linux 6.14 merge window, the NFS client gained support for direct I/O \(O\_DIRECT\) with LOCALIO. That kind of incremental kernel-side enhancement is what Layton&\#x27;s Plumbers talk surveys.

<details><summary>References</summary>
<ul>
<li><a href="https://www.phoronix.com/news/Linux-6.14-NFS">Linux 6.14 NFS Adds Direct I/O With LOCALIO, Attribute... - Phoronix</a></li>

</ul>
</details>

**Tags**: `#Linux`, `#NFS`, `#filesystems`, `#networking`, `#open source`

---

## Financial News

<a id="item-finance-news-1"></a>
### [China Proposes Export Controls on 40 AI, Biotech and Solar Technologies](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 8.0/10

China&\#x27;s Ministry of Commerce released a draft revision of its Catalogue of Technologies Prohibited or Restricted from Export for public comment, covering 40 technologies across artificial intelligence, biomedicine and solar power. The proposal spans 23 AI technologies \(large models, agents, computing clusters and information processing — excluding technologies already in the public domain via open source or published papers\), 5 biomedicine technologies \(cell and gene therapy, small nucleic acid drugs and pathogens, with licensing deals that do not transfer ownership eligible for expedited automatic approval\), and 12 solar technologies \(polysilicon, wafer and cell manufacturing, including key equipment\), according to the ministry; the draft is not yet in force, and the source headline&\#x27;s reference to &\#x27;temporary registration&\#x27; differs from the text&\#x27;s description of a proposed revision.

telegram · zaihuapd · Oct 16, 09:12

**「Background」** China&\#x27;s Catalogue of Technologies Prohibited or Restricted from Export is the official list setting which technologies need government permission — or are barred outright — before they can be transferred abroad, and revisions are published for public comment before they take effect. This round is still a consultation draft covering 40 proposed technologies, and the Ministry of Commerce has publicly explained its thinking behind the proposed artificial-intelligence additions.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.sina.com.cn/roll/2026-10-16/doc-inivmazf7040150.shtml">finance.sina.com.cn/roll/ 2026 -10-16/doc-inivmazf7040150.shtml</a></li>

</ul>
</details>

**Tags**: `#出口管制`, `#中国贸易政策`, `#人工智能`, `#生物医药`, `#光伏`

---