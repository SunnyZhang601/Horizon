---
layout: default
title: "Horizon Summary: 2026-10-17 (ZH)"
date: 2026-10-17
lang: zh
---

> 从 69 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Claude 溯源 NIST 椭圆曲线种子：源自 lrand48 与 Unix 时间戳](#item-tech-news-1) ⭐️ 8.0/10
2. [Big Fish：OpenBSD 内核 37 年前漏洞的利用研究](#item-tech-news-2) ⭐️ 8.0/10
3. [ORL 加速扩散语言模型单请求推理，RTX 5090 达 2,788 tokens/s](#item-tech-news-3) ⭐️ 8.0/10
4. [阶跃星辰发布 Step 5 Preview 稀疏 MoE 智能体模型](#item-tech-news-4) ⭐️ 8.0/10
5. [NVIDIA Indic 预训练：2.8 万亿 token 与开放数据生成流程](#item-tech-news-5) ⭐️ 7.0/10
6. [内核 Rust：基于 pin\_init 的安全自引用数据结构提案](#item-tech-news-6) ⭐️ 6.0/10
7. [LWN：Linux NFS 服务器近期与未来改动](#item-tech-news-7) ⭐️ 6.0/10

**财经新闻**
1. [商务部拟修订技术出口目录，涉人工智能、生物医药、光伏 40 项技术](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Claude 溯源 NIST 椭圆曲线种子：源自 lrand48 与 Unix 时间戳](https://www.anthropic.com/research/ecdsa-curve-origins) ⭐️ 8.0/10

Anthropic 发布研究称，Claude 在不到半小时内追溯出 NIST P-192、P-224、P-256、P-384 和 P-521 五条椭圆曲线种子的来源：它们并非任何哈希算法的结果，而是 C 标准库 lrand48 随机数生成器以 Unix 时间戳为种子产生的输出。据社区评论转述，第五个二进制种子 B-163 不符合 Claude 已尝试的任何生成方式，目前仍无解释。需要说明的是，该条目本身基本只包含一个链接和社区讨论，上述结果来自 Anthropic 的报告与评论转述，未经独立验证。

hackernews · ahlCVA · 10月16日 18:55 · [社区讨论](https://news.ycombinator.com/item?id=50122800)

**「背景」** 椭圆曲线标准的参数会附带一个“种子”值，其用意是让曲线系数能够经公开算法从该种子复现，以表明参数是推导而来、而非人为挑选；但这些种子的来源长期无法被复现，因而成为悬置多年的争议话题，社区评论将其形容为围绕 NIST 曲线的多年“阴谋论”。被引述的分析给出的生成方式并非任何哈希算法，而是 C 库 lrand48\(\) 的 lrand48\(\) &gt;&gt; 23 输出，且每个恢复出的 48 位状态都能重建完整的 160 位种子（tool-2-1）。

**「实际影响」** 这一发现解决的是种子的“生成方式”问题，而非曲线“被选中”的问题：正如评论所指出的，生成过程中被丢弃的候选值无法被观察，理论上仍可通过遍历时间戳来搜索具有特定性质的曲线。因此对依赖这些曲线的实现者而言，兼容性不受影响，但 NIST 种子来源的可审计性、以及此前“种子被故意构造”的猜测，其证据基础发生了变化；B-163 未被解释也意味着溯源工作并不完整。

**「社区讨论」** HN 评论在肯定结果的同时强调其边界：fidotron 指出，这只能确认生成方法，无法说明曲线的选择过程，因为被丢弃的候选值不可见，仍原则上可能通过搜索时间戳来定向选曲线。teddyh 则对 B-163 提出更简单的解释——它或许本以同样方式生成，只是在发布途中被误敲了一位数字，因此按“数字正确”的假设无法求解。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/ecdsa-curve-origins">Claude reveals ECDSA curve origins \ Anthropic</a></li>

</ul>
</details>

**标签**: `#cryptography`, `#elliptic curves`, `#AI research`, `#NIST standards`, `#cybersecurity`

---

<a id="item-tech-news-2"></a>
### [Big Fish：OpenBSD 内核 37 年前漏洞的利用研究](https://calif.io/research/big-fish) ⭐️ 8.0/10

安全研究文章《Big Fish》（发布于 calif.io）公布了对 OpenBSD 内核中一个已存在约 37 年的漏洞的利用研究。目前可获得的材料仅有文章标题、简要说明与社区评论，缺少受影响代码路径、版本范围、利用前提以及是否已有修复等具体细节，因此该漏洞的实际影响范围无法确认。文章由此引出对代码审查局限的讨论：为何这类缺陷能在一个长期以人工审计著称的项目中存续如此之久。

hackernews · rs\_rs\_rs\_rs\_rs · 10月16日 14:44 · [社区讨论](https://news.ycombinator.com/item?id=50118977)

**「背景」** Calif 将漏洞相关字段的声明追溯到约 37 年前的原始 BSD 源码，说明“37 年”指的是这段继承代码的年龄，而非现代 OpenBSD 已存在这么久（tool-2-2）。评论区有人提到，NetBSD 在 1999 年 8 月重写该部分代码时无意中修复了同一问题，但这一说法未在提供的资料中得到独立确认。

**「影响」** 这是一枚本地权限提升漏洞：攻击者需要先在目标主机上获得代码执行能力，之后才能把普通用户权限提升为 root；据安全厂商 Calif 公布的概念验证，该利用链绕过了 OpenBSD 的 KARL 内核地址随机化以及 SMAP、SMEP 硬件保护，并可在 OpenBSD 7.9 上取得 root 权限。由于链中一环可追溯到约 37 年前的 BSD 原始代码，源自 BSD 的其他内核代码可能带有同类缺陷；据 thedailytechfeed 报道相关漏洞在 PoC 公布后已被修补，因此管理员应核对并安装最新安全补丁，而不能依赖 KARL 或 SMAP/SMEP 等缓解措施。

**「社区讨论」** 评论者 ozereray1 认为，一个漏洞能在以重度审计著称的代码库中存活 37 年，说明某些内核缺陷单靠人工审查很难发现，并追问模糊测试或静态分析是否能实际找出这类问题，还是必须由人从利用原语的角度去思考。评论者 phendrenad2 则指出，同类代码在 NetBSD 于 1999 年 8 月的一次重写中被意外修复。以上均为评论者个人说法，未在所提供的材料中得到独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://dzen.ru/a/atJi8f5wA2igUvxy">Calif получила root в OpenBSD через 37 -летнюю ошибку ядра | Дзен</a></li>
<li><a href="https://cybersecuritynews.com/37-year-old-kernel-openbsd-flaw/">37-Year-Old Kernel Flaw Exploited to Gain Root Access on ...</a></li>
<li><a href="https://thehackernews.com/2026/10/researchers-demonstrate-openbsd-root.html">Researchers Demonstrate OpenBSD Root Exploit Chaining 37-Year ...</a></li>
<li><a href="https://thedailytechfeed.com/37-year-old-kernel-bug-in-openbsd-finally-patched-after-root-exploit-poc/">37-Year-Old Kernel Bug in OpenBSD Finally Patched After Root ...</a></li>

</ul>
</details>

**标签**: `#OpenBSD`, `#kernel security`, `#vulnerability research`, `#exploit development`, `#operating systems`

---

<a id="item-tech-news-3"></a>
### [ORL 加速扩散语言模型单请求推理，RTX 5090 达 2,788 tokens/s](https://www.reddit.com/r/MachineLearning/comments/1x7qgr0/research_2788_tokenss_on_a_single_rtx_5090_with_a/) ⭐️ 8.0/10

Reddit r/MachineLearning 研究帖介绍了 ORL（On-Policy Residual Learning）与配套推理引擎 dlmrt，声称能在不牺牲生成质量的前提下大幅加快扩散语言模型（dLLM）的单请求解码。作者给出的峰值数据包括：LLaDA-2.1-mini + ORL 在单张 RTX 5090 上以 NVFP4 达到 2,788 tokens/s，DiffusionGemma 26B MoE + ORL 在 8×B200 上达到 7,708 tokens/s，QwenDLM-4B 端到端吞吐最高提升约 6.9× 且 HumanEval pass@1 从 82.9% 提升到 89.6%，单张 H100 上为 1,298 tokens/s，对比 DFlash 的 746 tokens/s 和 EAGLE3 的 405 tokens/s。作者已开源模型权重、训练代码、评测流程和推理引擎 dlmrt，并说明上述数字均为 batch size 1 的单请求峰值结果，不是并发请求的聚合吞吐，也不是任意提示的平均值。这些主张来自作者自述的帖子，尚未经独立验证。

reddit · r/MachineLearning · /u/arty\_photography · 10月16日 20:03

**「背景」** 与一次只生成一个 token 的自回归语言模型不同，扩散语言模型（dLLM）可以在一次前向传播中并行细化并确定多个 token，难点在于如何让它们用更少的去噪步数收敛。ORL 所强调的&quot;在线策略&quot;（on-policy）正源于此：残差上下文由模型自己在推理中产生，其分布会随训练过程变化，若在离线的、陈旧的残差上训练就会造成训练与推理的错配，因此需要直接在当前模型生成的残差轨迹上训练；相关论文与代码库也把这一算法与残差捕获、专用注意力核和负载均衡打包等系统设计协同考虑（tool-2-1、tool-2-2）。在自回归一侧，用于对比的低延迟方案则是投机解码，例如本文提到的 DFlash 与 EAGLE3。

**「影响」** 对希望在消费级 Blackwell 显卡上做本地单请求推理的开发者，作者提供了可试用的具体路径：用 dlmrt 加载 LLaDA-2.1-mini ORL 的 NVFP4 checkpoint，而 NVFP4 路径依赖 Blackwell 架构（包括 RTX 5090）。需要注意这是一次端到端系统对比——ORL 侧使用 dlmrt，投机解码基线使用 vLLM，复现时引擎差异会影响结果；作者也公开邀请社区复现并测试不同工作负载。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2610.20687v1">On-Policy Residual Learning for Diffusion Language Models</a></li>
<li><a href="https://github.com/Introspective-Diffusion/ORL/blob/main/">ORL: On-Policy Residual Learning for Diffusion Language Models</a></li>

</ul>
</details>

**标签**: `#diffusion language models`, `#LLM inference`, `#speculative decoding`, `#open source`, `#GPU performance`

---

<a id="item-tech-news-4"></a>
### [阶跃星辰发布 Step 5 Preview 稀疏 MoE 智能体模型](https://huggingface.co/stepfun-ai/Step-5-Preview) ⭐️ 8.0/10

阶跃星辰在 Hugging Face 发布旗舰模型 Step 5 Preview，定位为面向智能体工作负载的预览版本。该模型采用稀疏 MoE 架构，总参数 6000 亿、激活参数 270 亿，支持最高 100 万 token 上下文，并可接收文本、图像和视频输入。官方称其在软件工程、长周期智能体执行和专业知识任务（尤其金融场景）上表现领先，但这是预览阶段的厂商说法，尚无第三方评测验证。部署方面可通过 OpenAI 兼容 API 搭配 vLLM 或 SGLang，许可为 StepFun Model License 1.0。

telegram · zaihuapd · 10月16日 06:36

**「背景」** 稀疏 MoE（混合专家）架构的核心是把总参数量与激活参数量分开：模型的容量由全部专家决定，但每个 token 前向只激活其中一部分，因此推理开销更接近激活参数规模。Step 5 Preview 在 Hugging Face 上公布的规格即 6000 亿总参数、270 亿激活参数、最高 100 万 token 上下文，这一结构是理解其“大模型体量、较小推理成本”定位的前提。

**「对开发者的实际影响」** 对需要长上下文智能体能力的团队来说，Step 5 Preview 可通过 OpenAI 兼容 API 配合 vLLM 或 SGLang 部署，意味着现有以 OpenAI 接口为基准的推理与调用栈较容易改接；但它采用 StepFun Model License 1.0 而非标准开源许可，正式采用前需核对授权条款。第三方报道称该模型在 DeepSWE v1.1 软件工程测试中得分 67.7%，略高于 Kimi K3 与 GLM-5.3，且厂商给出“单任务成本为 Claude Opus 5 的 1/8”的说法——这些均为厂商或媒体数据，尚无独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/stepfun-ai/Step-5-Preview">stepfun -ai/ Step - 5 - Preview · Hugging Face</a></li>
<li><a href="https://blog.margrop.net/post/step-5-preview-sparse-moe-agentic-model/">600B 参数仅激活 27B，单任务成本狂砍 8 倍！ 阶 跃 星 辰 Step ...</a></li>
<li><a href="https://m.21jingji.com/article/20260921/herald/742325e7deb08d056e5801bcae9c9974.html">“单任务成本仅为Claude Opus 5的1/8”， 阶 跃 星 辰 Step 5 Preview ...</a></li>

</ul>
</details>

**标签**: `#large language models`, `#mixture-of-experts`, `#AI agents`, `#multimodal models`, `#StepFun`

---

<a id="item-tech-news-5"></a>
### [NVIDIA Indic 预训练：2.8 万亿 token 与开放数据生成流程](https://huggingface.co/blog/nvidia/scaling-indic-pretraining) ⭐️ 7.0/10

Hugging Face 博客发布文章，介绍 NVIDIA 在大规模 Indic 语言预训练方面的工作，称其使用了 2.8 万亿个 token，并提供了开放的数据生成流程。该工作面向多语言 NLP 与数据驱动的研究者，但博客未披露模型名称、参数规模或基准测试结果。由于目前仅有标题和摘要可供参考，这些数字属于发布方声明，尚待独立验证，也无法确认模型或数据是否已开放下载。

rss · Hugging Face Blog · 10月16日 01:44

**「背景」** 预训练语料的规模通常以 token 数量衡量，2.8 万亿 token 属于当前大模型基础训练所用的量级。围绕这一体量，NVIDIA 与 IIT Madras、其 AI4Bharat 实验室以及 Bodhan AI 联合推出了 Nemotron-pretraining-Indic-v1，覆盖 22 种印度语言，全部使用本土文字，其中 12 种语言还包含罗马化转写文本，并附带用于生成该语料的开放、GPU 加速数据管线。截至 2026 年 10 月中旬的报道，该语料被描述为“即将发布”，尚不能视为已完全开放下载。

**「对开发者与数据团队的影响」** 从事印度语言模型训练的开发者可以直接复用 Nemotron-pretraining-Indic-v1 这一约 2.8 万亿 token、覆盖 22 种印度附表语言的合成数据集，以及配套的开源 GPU 加速数据生成流水线，从而省去从零搭建多语言合成预训练数据管线的成本（tool-3-1、tool-3-3）。不过该数据集为合成生成，团队在正式训练前仍需针对自身语言配比与领域做质量校验，并确认流水线对算力和依赖环境的要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://daily.dev/posts/scaling-indic-pretraining-2-8-trillion-tokens-and-an-open-data-generation-pipeline-gngeiqcjb">Scaling Indic Pretraining: 2.8 Trillion Tokens and an Open ...</a></li>
<li><a href="https://www.unite.ai/nvidia-unveils-2-8t-token-indic-pretraining-corpus-and-open-pipeline/">NVIDIA Unveils 2.8T-Token Indic Pretraining Corpus and Open ...</a></li>
<li><a href="https://www.explainx.ai/blog/nvidia-indic-pretraining-2-8-trillion-tokens-open-pipeline-2026">Nemotron Indic Pretraining: 2.8T Tokens, 22 Languages ...</a></li>
<li><a href="https://www.printingpressai.com/article/generative-ai/scaling-indic-pretraining-2-8-trillion-tokens-and-an-open-data-generation-pipeli">Scaling Indic Pretraining: 2.8 Trillion Tokens and an Open ...</a></li>

</ul>
</details>

**标签**: `#AI`, `#LLM pretraining`, `#multilingual NLP`, `#open data`, `#Indic languages`

---

<a id="item-tech-news-6"></a>
### [内核 Rust：基于 pin\_init 的安全自引用数据结构提案](https://lwn.net/Articles/1099224/) ⭐️ 6.0/10

在 Kangrejos 2026 上，Gary Guo 介绍了一种基于内核 pin\_init crate 的方案，用于解决 Rust 自引用数据结构长期难以在不使用 unsafe 代码的情况下实现的问题（pin\_init 本身用于创建不可移动的数据结构，通常服务于与 C 的互操作）。据该演讲的说法，这一改动有望移除 Nova GPU 驱动中大部分与生命周期相关的 unsafe 代码，并最终适用于其他 Rust 组件。不过现有报道仅为简短摘要，未给出具体机制、代码示例或实测结果，因此上述效果目前属于演讲者的预期，而非已经验证的结论。

rss · LWN.net · 10月16日 18:30

**「背景」** Rust 长期难以安全表达自引用结构：这类结构持有指向自身数据的指针，而值一旦被移动，内部指针就会失效，\`Pin\` 的意义正是保证值从被钉住直到析构都停留在同一内存位置\[tool-2-2\]。内核的 \`pin\_init\` crate 在此之上提供不可移动数据结构的原地安全初始化，通过 \`\#\[pin\_data\]\`、\`\#\[pin\]\` 标记字段并用 \`pin\_init\!\` 构造，主要用于与 C 代码互操作\[tool-2-1\]\[tool-2-3\]。Nova 是 Rust for Linux 中的 GPU 驱动，其与生命周期相关的 unsafe 代码能否减少，取决于这套初始化机制能覆盖多少自引用场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://rust.docs.kernel.org/pin_init/">pin_init - Rust</a></li>
<li><a href="https://doc.rust-lang.org/std/pin/?example-self-referential-struct">std::pin - Rust pin_init - Rust - Docs.rs kernel::init - Rust linux/rust/kernel/init.rs at master · torvalds/linux · GitHub init.rs - source - The Linux Kernel Archives rust: pin-init: create self references safely - lwn.net</a></li>
<li><a href="https://docs.rs/pin-init/latest/pin_init/">pin_init - Rust - Docs.rs</a></li>

</ul>
</details>

**标签**: `#Rust`, `#Linux kernel`, `#Rust for Linux`, `#memory safety`, `#GPU drivers`

---

<a id="item-tech-news-7"></a>
### [LWN：Linux NFS 服务器近期与未来改动](https://lwn.net/Articles/1098611/) ⭐️ 6.0/10

LWN 报道称，在 2026 年 Linux Plumbers 大会上，NFS 开发者 Jeff Layton 介绍了 Linux 内核 NFS 服务器实现的近期改进，并透露了近期计划中的后续工作。该报道仅是该演讲的简要概述，未给出具体版本号、补丁名称、性能数据或合并时间表，也未说明这些改动是已经落地还是仍处于计划阶段。因此，目前可确认的只是一场关于进行中和计划中工作的会议演讲，而不是已发布功能或经过独立测量的结果。

rss · LWN.net · 10月16日 14:26

**「背景」** NFS 是 Unix 类系统上历史悠久的网络文件系统协议，协议本身仍在演进，Linux 内核的客户端与服务器实现必须持续跟进。近期的一个例子是 Linux 6.14 合并窗口中的 NFS 改动，其中客户端侧为 LOCALIO 启用了 O\_DIRECT 直接 I/O。2026 年 Linux Plumbers Conference 上 NFS 开发者 Jeff Layton 介绍的议题，正建立在这样的持续迭代之上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.phoronix.com/news/Linux-6.14-NFS">Linux 6.14 NFS Adds Direct I/O With LOCALIO, Attribute... - Phoronix</a></li>

</ul>
</details>

**标签**: `#Linux`, `#NFS`, `#filesystems`, `#networking`, `#open source`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [商务部拟修订技术出口目录，涉人工智能、生物医药、光伏 40 项技术](https://aqygzj.mofcom.gov.cn/flzc/gzjgfxwj/art/2026/art_c99f95ca0cd043829ac9991495fc283c.html) ⭐️ 8.0/10

商务部就修订《中国禁止出口限制出口技术目录》公开征求意见，拟对人工智能、生物医药、光伏三个领域共 40 项技术实施出口管理。其中人工智能 23 项（含大模型、智能体、算力集群）、生物医药 5 项（含细胞和基因治疗、小核酸药）、光伏 12 项（含多晶硅、硅片和电池制造及关键设备），该文件目前仍处征求意见阶段，尚未正式生效。

telegram · zaihuapd · 10月16日 09:12

**「背景」** 《中国禁止出口限制出口技术目录》是商务部管理技术出口的既有清单，列入其中的技术需按限制或禁止类别办理出口许可；此次修订以公开征求意见方式公布，尚未正式生效，商务部已就拟增列人工智能技术的考虑作出回应。

**「影响」** 若该征求意见稿最终生效，需要向境外转让或许可上述技术的中国机构——如大模型与算力集群、细胞和基因治疗、多晶硅及硅片制造等领域的企业——将须按出口管理程序申请许可；不过不涉及所有权转让的对外授权模式适用自动许可等便利措施，且已通过开源、发表论文进入公共领域的技术不在管理范围内。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.sina.com.cn/roll/2026-10-16/doc-inivmazf7040150.shtml">finance.sina.com.cn/roll/ 2026 -10-16/doc-inivmazf7040150.shtml</a></li>

</ul>
</details>

**标签**: `#出口管制`, `#中国贸易政策`, `#人工智能`, `#生物医药`, `#光伏`

---