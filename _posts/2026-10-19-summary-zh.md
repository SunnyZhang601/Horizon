---
layout: default
title: "Horizon Summary: 2026-10-19 (ZH)"
date: 2026-10-19
lang: zh
---

> 从 92 条内容中筛选出 25 条重要资讯。

---

**科技新闻**
1. [Linux 7.3 内核发布：18765 个非合并提交创纪录](#item-tech-news-1) ⭐️ 9.0/10
2. [vLLM v0.32.0 发布：通用解析器与低精度 KV 缓存](#item-tech-news-2) ⭐️ 7.0/10
3. [HybridAgent：潜空间推理、文本行动](#item-tech-news-3) ⭐️ 7.0/10
4. [RepRapMicron：开源微米级 3D 打印项目 wiki](#item-tech-news-4) ⭐️ 7.0/10
5. [DeepSeek 推出搜索与抓取 API，每千次成功请求 0.75 美元](#item-tech-news-5) ⭐️ 7.0/10
6. [开源亚微米三维运动平台 MicroManipulator 获关注](#item-tech-news-6) ⭐️ 7.0/10
7. [动画讲解 Parser Combinators](#item-tech-news-7) ⭐️ 7.0/10
8. [F-22 飞行员在模拟空战中演示指挥 YFQ-44A 无人僚机](#item-tech-news-8) ⭐️ 7.0/10
9. [Anthropic 向 METR 开放“类员工”内部访问权限](#item-tech-news-9) ⭐️ 7.0/10
10. [TempoPFN：用合成数据预训练线性 RNN 实现零样本时间序列预测](#item-tech-news-10) ⭐️ 7.0/10
11. [SemiAnalysis：英伟达 vLLM 优化使 Kimi K3 提速 1.68 倍](#item-tech-news-11) ⭐️ 7.0/10
12. [Google 开源 Harness² 递归智能体优化框架](#item-tech-news-12) ⭐️ 7.0/10
13. [Anthropic 游说法案：AI 致 50 死或 10 亿美元损失才可叫停](#item-tech-news-13) ⭐️ 7.0/10
14. [软件的价值不只在代码，更在人的判断与品味](#item-tech-news-14) ⭐️ 6.0/10
15. [把 Wi-Fi 网卡变成 SDR：未公开 I/Q 采样能力扩散](#item-tech-news-15) ⭐️ 6.0/10
16. [浙大提出具身智能体长程记忆基准](#item-tech-news-16) ⭐️ 6.0/10
17. [官方 DLSS 5 被提取：非支持游戏最高提速 90%](#item-tech-news-17) ⭐️ 6.0/10
18. [MIT 研发软性三维形状传感皮肤，误差低于半厘米](#item-tech-news-18) ⭐️ 6.0/10
19. [SemiAnalysis：300 多项数据中心禁令仅拖慢三个美国项目](#item-tech-news-19) ⭐️ 6.0/10
20. [FOI 开源 WiFireNet：用 Wi-Fi 信号识别隐藏手枪](#item-tech-news-20) ⭐️ 6.0/10
21. [大疆发布首款换电机场 Dock 4，未获美国 FCC 认证](#item-tech-news-21) ⭐️ 6.0/10

**科技博客**
1. [Intel 8087 浮点加减的微码实现](#item-tech-blog-1) ⭐️ 9.0/10

**财经新闻**
1. [英央行副行长警告：对冲基金杠杆化持债或放大债市冲击](#item-finance-news-1) ⭐️ 7.0/10
2. [特朗普以放宽制裁换俄罗斯柴油：普京获政治收益，乌克兰承压](#item-finance-news-2) ⭐️ 7.0/10
3. [美国 AI 基建热潮现裂痕：至少 47 个大型数据中心项目受阻](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Linux 7.3 内核发布：18765 个非合并提交创纪录](https://lwn.net/Articles/1101143/) ⭐️ 9.0/10

Linus Torvalds 按预期发布了 Linux 7.3 内核。本次发布在提交量和开发者数量上都创下纪录：共纳入 18,765 个非合并提交，来自 3,021 名开发者，其中 807 人是首次参与内核开发的贡献者。主要变更包括 binfmt\_misc 的扩展、面向大型系统的分组调度改进、对所有操作都返回失败的新 failfs 文件系统、fchroot\(\) 系统调用、BPF 程序的全局 per-CPU 数据、sched\_ext 子调度器特性的完成、虚拟机的 working-set 跟踪、ntfs3 的备用数据流支持，以及一批 SMB 服务器改进。Torvalds 同时宣布 7.4 的合并窗口于次日开启，但他正值年度家庭休假，合并工作当天下午才开始，因此他预计自己的作息在一段时间内会不太规律。

rss · LWN.net · 10月18日 23:45

**「发布节奏背景」** Linux 内核按合并窗口推进版本开发：新特性先在合并窗口进入主线，再经过若干候选版本测试，最终发布稳定版。7.3 发布后，7.4 的合并窗口随即开启；Torvalds 表示，由于正值家庭休假，他接下来一段时间的合并安排会与平常不同。

**「影响」** 希望使用 sched\_ext 完整功能、fchroot\(\) 或 failfs 等的开发者和发行版维护者，需要以 7.3 或其后续稳定版本为基线；由于 Torvalds 休假，7.4 合并窗口的初期节奏会与常规不同，新特性进入主线的时机也可能随之偏移。

**标签**: `#Linux kernel`, `#open source`, `#operating systems`, `#release engineering`

---

<a id="item-tech-news-2"></a>
### [vLLM v0.32.0 发布：通用解析器与低精度 KV 缓存](https://github.com/vllm-project/vllm/releases/tag/v0.32.0) ⭐️ 7.0/10

vLLM 发布 v0.32.0，包含 814 个提交、363 名贡献者。此版本新增 \`hf\` 工具调用与推理解析器，可直接读取 checkpoint 的 \`response\_template\`，并扩展 NVFP4/FP8 低精度 KV 缓存：NVFP4 覆盖 SM8x、SM12x 和 SM90，GLM-5.x 在 SM100 上默认使用 FP8 KV 缓存。按发布说明，GLM-5.x 的 FP8 KV 默认配置在每个 rank 上将 KV 内存减半，基准中吞吐提高 2.3–5.5%，但首 token 时间增加 7–11%；ROCm 还新增约两倍于 FP8 密度的 4-bit \`ultraquant\_4bit\` KV 缓存。该版本有破坏性变更：不再支持 Python 3.10，默认限制 CORS 来源，升级 \`transformers\`/\`tokenizers\` 依赖，并移除 cascade attention 等旧路径。

github · khluu · 10月18日 06:50

**「背景」** vLLM 是开源的大模型推理与服务引擎，以 OpenAI 兼容的 HTTP 接口对外提供模型能力；它此前已通过 \`--tool-call-parser\`、\`--reasoning-parser\` 之类的启动参数，把模型原始输出拆分成工具调用与推理内容，但这些解析器通常是按模型家族逐个实现的。KV cache 是推理时缓存历史 token 的注意力键值、避免重复计算的核心结构，其精度直接决定显存占用：把 KV cache 从 BF16 降到 FP8 或 4 位，用更少显存换取更长的上下文或更大的并发批次，代价通常是首 token 延迟（TTFT）与精度上的取舍。因此本次发布涉及的通用 \`hf\` 解析器与多种 GPU 架构上的低精度 KV cache，都是在既有机制上扩展适用范围，而非从零引入的新能力。

**「影响」** 部署者升级前需检查 Python 3.10、CORS 默认值、\`transformers\`/\`tokenizers\` 版本约束，以及 \`max\_tokens\` 不再从上下文窗口预留等行为变化；使用 GLM-5.x 的团队可在 SM100 上获得更低 KV 内存占用，但应权衡 7–11% 的首 token 延迟代价。对于自带 \`response\_template\` 的模型，\`--tool-call-parser hf\` 和 \`--reasoning-parser hf\` 可免去模型专用解析器。

**标签**: `#LLM inference`, `#vLLM`, `#KV cache quantization`, `#GPU kernels`, `#structured outputs`

---

<a id="item-tech-news-3"></a>
### [HybridAgent：潜空间推理、文本行动](https://arxiv.org/abs/2610.18861) ⭐️ 7.0/10

togethercomputer 的 HybridAgent 项目通过论文与开源发布提出一种 LLM 代理：代理在潜空间中完成推理，再通过文本执行动作。代码发布在 GitHub 的 togethercomputer/HybridAgent，模型和数据放在 Hugging Face 集合中，评估部分位于 arXiv 论文第 5 节。来源没有提供具体基准分数，因此目前能确认的是方法与发布物，而不是已公开验证的性能优势。

hackernews · allinonai · 10月18日 20:48 · [社区讨论](https://news.ycombinator.com/item?id=50145337)

**「背景」** 现有工具型 LLM 智能体通常把中间推理写成文本，再据此发起工具调用；隐空间推理则把中间步骤留在连续表示中，HybridAgent 试图把两者衔接起来。论文提出的 HybridLink 用于连接隐空间表示与文本动作，并通过 HybridSFT 和 HybridRL 后训练教模型何时在隐空间思考、何时输出文本动作；作者在 Qwen3-Base 模型上实例化了这一流程。

**「影响」** 对想试用的开发者，代码、模型和数据的发布降低了复现门槛；但若沿用现有推理栈，需要先验证框架兼容性——有评论报告一个 14B 模型的 8-bit 量化版本在 llama.cpp 中反复输出同一段内容，尚不清楚是模型问题还是推理框架适配问题。

**「社区讨论」** 评论中，amluto 建议在文本模式下也同时传入潜空间向量和 token 嵌入，让模型边生成文本边进行潜空间推理；incognito124 则追问这与 Astra 的循环 Transformer 有何本质区别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2610.18861v1">Hybrid Reasoning Agents - arXiv.org</a></li>
<li><a href="https://www.explainx.ai/blog/hybridagent-together-stanford-latent-reasoning-text-tools-10-4-percent-3x-cheaper-code-2026">HybridAgent: Latent Reasoning Agents, 3x Cheaper, Code Out ...</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#latent reasoning`, `#hybrid reasoning`, `#open-source AI`, `#arXiv`

---

<a id="item-tech-news-4"></a>
### [RepRapMicron：开源微米级 3D 打印项目 wiki](https://github.com/VikOlliver/RepRapMicron/wiki) ⭐️ 7.0/10

Hacker News 上被讨论的是 RepRapMicron 的 GitHub wiki，该页面指向一个面向微米级 3D 打印的开源项目。提供的材料没有包含打印分辨率、材料体系、速度、成本或可复现实验结果，因此尚不能确认它已实现可用的微米级制造。对关注开源微纳加工和芯片原型制作的人而言，这一方向具有潜在相关性，但项目当前状态仍不明确。

hackernews · RobotToaster · 10月18日 13:48 · [社区讨论](https://news.ycombinator.com/item?id=50141076)

**「背景」** RepRap 项目原本旨在开发低成本、可打印自身大部分零件的开源 3D 打印机，其设计以自由软件许可证发布。RepRapMicron 把这一开源思路延伸到微米尺度：项目页面称目标可制造小至 1 微米甚至更细的结构，早期原型预期在 10 毫米工作范围内实现优于 3 微米的可重复定位，特征尺寸约为 10–20 微米。

**「社区讨论」** Hacker News 评论者把 RepRapMicron 与工业革命时期精密制造工具的突破相类比，期待廉价、可持续的芯片设计打印能改变硬件开发；也有人质疑极端微型化自复制的实际意义。上述均为评论者观点，未提供项目性能或可行性证据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RepRap">RepRap - Wikipedia</a></li>
<li><a href="https://reprap.org/wiki/RepRapMicron">RepRapMicron - RepRap GitHub - VikOlliver/RepRapMicron: μRepRap - A 3D printer ... RepRap Micron: Open-Source Printer Produces a 0.65-Millimeter ... Introducing RepRapMicron: The Open Source 3D Printer ... RepRapMicron Micron Scale 3D Printer by vik - Thingiverse RepRapMicron: Exploring Micro-Manufacturing via Precision ... RepRap - Wikipedia</a></li>

</ul>
</details>

**标签**: `#RepRapMicron`, `#micron-scale 3D printing`, `#open-source hardware`, `#microfabrication`, `#DIY semiconductors`

---

<a id="item-tech-news-5"></a>
### [DeepSeek 推出搜索与抓取 API，每千次成功请求 0.75 美元](https://api-docs.deepseek.com/guides/search/) ⭐️ 7.0/10

DeepSeek 推出了搜索与抓取 API，面向需要网页检索的 AI agent 和 RAG 构建者。其文档标价为每 1000 次成功请求 0.75 美元，计费口径只针对成功请求。现有材料未提供独立测得的检索质量或延迟数据。

hackernews · fagnerbrack · 10月18日 06:50 · [社区讨论](https://news.ycombinator.com/item?id=50138531)

**「背景」** 此前，DeepSeek 已将 Search 和 Fetch 作为服务端工具接入 DeepSeek Harness、Claude Code 和 Codex；这些调用目前免费，按请求计费将从北京时间 2026 年 11 月 1 日 00:00 开始。此次开放让开发者可以直接调用这两个端点，而不必只通过上述工具间接使用。

**「对 RAG 与 Agent 开发者的成本影响」** 对构建 RAG 或 AI agent 的团队来说，按「每 1000 次成功请求 0.75 美元」计费意味着失败查询不产生费用，预算比按调用次数计费更可预测；作为价格参照，Brave 的公开定价页面显示其分层区间可覆盖到每 1000 次查询 30 美元。接入前需要向文档确认「成功请求」的判定口径，以及搜索与抓取是否共用同一计费单位，否则实际账单可能高于按标题推算的水平。

**「社区讨论」** 有评论质疑托管搜索 API 的实际用途，并称自建 SearXNG 工具对个人使用更省钱；也有人推测，随着 agent 驱动搜索普及，搜索 API 可能因 SEO 和结果排序竞争而出现负价格。另有评论在比较时列出 Brave Search API 为 5 美元、Kagi API 为 12 美元。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://startupfortune.com/deepseek-opens-its-search-and-fetch-apis-at-075-per-1000-calls/">DeepSeek Opens Its Search and Fetch APIs at $0.75 per 1,000 ...</a></li>
<li><a href="https://api-docs.deepseek.com/guides/search/">Search &amp; Fetch | DeepSeek API Docs</a></li>
<li><a href="https://costbench.com/software/ai-search-apis/brave-search-api/">Brave Search API Pricing 2026: Free-$30 per 1K queries</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#search API`, `#DeepSeek`, `#web retrieval`, `#pricing`

---

<a id="item-tech-news-6"></a>
### [开源亚微米三维运动平台 MicroManipulator 获关注](https://github.com/0x23/MicroManipulatorStepper) ⭐️ 7.0/10

GitHub 上出现了一个名为 Open MicroManipulator（MicroManipulatorStepper）的开源 DIY 亚微米级三维运动控制平台，目标是用于精密仪器和嵌入式运动控制。该项目在 Hacker News 上引发讨论，评论者把它与 RepRap Micron 等同类方案比较，并提到压电粘滑驱动可实现更高分辨率但成本约 1,000 美元。现有材料未给出具体行程、重复定位精度、控制器配置或套件供应情况，因此“亚微米”目前是项目定位，尚无独立测量结果。

hackernews · \_Microft · 10月18日 11:16 · [社区讨论](https://news.ycombinator.com/item?id=50140001)

**「背景」** 亚微米级三维定位常用昂贵的压电位移台；MicroManipulatorStepper 改用步进电机驱动，试图以开源、低成本方案实现精密运动控制。项目说明把光学对准、电子元件探测和显微观察列为目标用途。

**「影响」** 对于需要精密定位但预算有限、且愿意自行搭建的开发者和小型实验室，这个项目的开源属性意味着可以按需修改机械、驱动和控制部分；代价是精度、重复性和长期稳定性需要自行校准验证，不能直接等同于商用计量设备。

**「社区讨论」** 评论者把该项目与 RepRap Micron 相提并论，并指出压电粘滑执行器可达到潜在的亚纳米分辨率，但成本约 1,000 美元；也有人表示正在把非电动的手动版本加以改装，准备用于点衍射干涉仪。另一位评论者称刚用周末时间搭建了该项目，讨论集中在可复现性和具体应用，而不是单一的精度结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/omarshebl/micromanipulatorstepper">GitHub - omarshebl/micromanipulatorstepper: A sub-micrometer ...</a></li>
<li><a href="https://agihunt.info/en/p/1a14f0cd53e08a16381740e909e">Open MicroManipulator: an open-source… · AGI Hunt</a></li>

</ul>
</details>

**标签**: `#open-source hardware`, `#precision positioning`, `#motion control`, `#DIY instrumentation`, `#embedded systems`

---

<a id="item-tech-news-7"></a>
### [动画讲解 Parser Combinators](https://t3.at/blog/2026-10-17-parser-combinators/) ⭐️ 7.0/10

一篇题为《Parser Combinators》的动画博文用可视化方式讲解解析器组合子的工作方式，面向希望理解解析与语言设计的开发者；这是一篇概念教程，而非版本发布或经独立测量的性能报告。Hacker News 的讨论将其与正则表达式、解析器生成器以及 \`nom\` 等实际库相比较，并延伸到 monadic parser combinators。评论者还提到，组合子方案常需额外编写映射与解包代码，并且“返回值加剩余输入”的直观设计若依赖字符串切片，可能带来性能开销，但这些是经验性说法，而非统一基准。

hackernews · schindlabua · 10月18日 08:19 · [社区讨论](https://news.ycombinator.com/item?id=50139067)

**「背景概念」** 解析器组合子是一种高阶函数：它接收若干解析器作为输入，返回一个新的解析器，因此复杂语法的解析器可以由小块逐步拼装，并沿用递归下降的方式构造，也便于分别测试各个部件。Graham Hutton 的《Monadic Parser Combinators》常被当作把组合子与 monad 结合起来的入门文献，这篇博文正是对这一概念的教学式讲解，而非新版本发布或具体事件。

**「影响」** 对考虑采用解析器组合子的开发者，讨论指出的实际取舍是：它便于逐步组合和理解语法，但相比从独立语法文件生成解析器的工具，往往需要更多映射与解包代码；如果实现返回“值+剩余输入”，还应评估字符串切片的成本。以上是评论者报告的经验，不是基准测试结论。

**「社区讨论」** 评论者认可动画让概念更直观，但 ArneCode 认为组合子解析器因大量映射和解包代码而比语法文件驱动的生成器更难读；sovrin 则报告，返回“提取值+剩余输入”的设计在性能上不理想，问题可能出在字符串切片。BoppreH 还推荐 Python 内置却缺少官方文档的 \`re.Scanner\`，作为单个正则太重、完整解析器又太重时的分词选择。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Parser_combinator">Parser combinator - Wikipedia</a></li>
<li><a href="https://arialdomartini.github.io/monadic-parser-combinators">Monadic Parser Combinators in F#</a></li>
<li><a href="https://people.cs.nott.ac.uk/pszgmh/monparsing.pdf">Monadic Parser Combinators</a></li>

</ul>
</details>

**标签**: `#parser combinators`, `#parsing`, `#programming languages`, `#functional programming`, `#technical writing`

---

<a id="item-tech-news-8"></a>
### [F-22 飞行员在模拟空战中演示指挥 YFQ-44A 无人僚机](https://www.tomshardware.com/tech-industry/drones/f-22-raptor-pilot-successfully-demonstrates-command-of-wingman-fighter-drone-in-simulated-combat-anduril-yfq-44a-fury-test-advances-usafs-program-to-integrate-uncrewed-aircraft-into-fighter-squadrons) ⭐️ 7.0/10

美国空军在一场模拟空战中完成机载测试：一名 F-22“猛禽”飞行员向安杜里尔 YFQ-44A“狂怒”无人机下达战术指令，后者将指令解析为一系列任务和飞行动作。该测试属于协同作战飞机（CCA）项目，目标是把无人僚机编入战斗机中队，让飞行员以指挥方式使用无人机，而不是手动操纵。报道指出，这离作战部署仍有距离：项目还需界定无人机的战术自主性边界、安全飞行控制与武器授权，并验证其在电子干扰和通信中断下的表现，以及维护、弹药和前沿基地保障。

rss · Tom&\#x27;s Hardware · 10月18日 15:02

**「背景」** 美国空军的“协同作战飞机”（CCA）项目旨在让无人战机与有人战斗机编队协同执行任务，Anduril 的 YFQ-44A Fury 是该项目的候选机型之一。据 The Aviationist 报道，此次演示是 F-22A 首次在空中战术控制演示中操控一架 YFQ-44A，两架飞机当时均处于飞行状态。

**「后续影响」** 对 CCA 项目及承包商而言，接下来的测试重点将从“能否接收指令”转向自主性边界、通信降级和武器授权等可认证问题；这些结果决定无人僚机能否进入有人战斗机中队的日常作战与后勤流程。

<details><summary>参考链接</summary>
<ul>
<li>F-22 Controls Collaborative Combat Aircraft In Flight For The First Time</li>

</ul>
</details>

**标签**: `#autonomous-drones`, `#collaborative-combat-aircraft`, `#military-ai`, `#robotics`, `#human-machine-teaming`

---

<a id="item-tech-news-9"></a>
### [Anthropic 向 METR 开放“类员工”内部访问权限](https://arstechnica.com/ai/2026/10/anthropic-gives-outside-ai-watchdog-employee-like-access/) ⭐️ 7.0/10

Anthropic 已让非营利评估机构 METR 的团队嵌入其办公室，并授予该团队访问其硬件和内部系统的“类员工”权限，用于评估模型风险。这是对 9 月由 CEO 达里奥·阿莫代伊提出、并得到萨姆·奥尔特曼和埃隆·马斯克支持的“在领先实验室嵌入外部审计员”承诺的首次实施；OpenAI 尚未公布相关计划。Anthropic 表示，随着模型能力增强，它们需要更强保障和更困难的风险评估，但公司无法公开所有安全相关信息。

rss · Ars Technica · 10月18日 16:25

**「背景」** METR 是一家与 OpenAI、Anthropic、谷歌和 Meta 等主要实验室均有合作的非营利评估机构，其工作是在模型能力变得更强时对其风险进行独立测试。今年 9 月，Anthropic 首席执行官 Dario Amodei 提议在领先实验室内部常驻外部审计员，OpenAI 的 Sam Altman 和 SpaceX 的 Elon Musk 都公开支持这一构想；此次给予 METR 的访问权限是该承诺的首次具体落实。Anthropic 将这种安排类比为银行业监管中向大型银行派驻现场检查员的制度。

**「实际影响」** 对 METR 而言，这意味着评估可以基于 Anthropic 的非公开系统和硬件，而不只是公开材料；但 Anthropic 以相关信息可能帮助恶意行为者或竞争对手为由，表示不会公开所有相关内容。批评者认为这类安排可能产生利益冲突，并主张需要更强的政府监管；Anthropic 则将其比作向大型银行派驻检查员的银行监管模式。

**标签**: `#AI safety`, `#AI governance`, `#Anthropic`, `#third-party evaluation`, `#METR`

---

<a id="item-tech-news-10"></a>
### [TempoPFN：用合成数据预训练线性 RNN 实现零样本时间序列预测](https://www.reddit.com/r/MachineLearning/comments/1x97v19/tempopfn_synthetic_pretraining_of_linear_rnns_for/) ⭐️ 7.0/10

一个被 NeurIPS 2026 接收的研究项目 TempoPFN 发布了一套合成时间序列生成器与数据增强库，用于训练时间序列基础模型；该研究自身采用的模型是基于 DeltaProduct 的线性 RNN。作者同时开源了代码（GitHub 仓库 automl/TempoPFN），并在 Hugging Face 的 AutoML-org 组织下发布了预训练权重。帖子称，这套合成数据此前已被用于 Toto-2 和 TS-ICL。帖子只给出 arXiv 编号 2510.25502 和作者名单（Vladyslav Moroshan、Julien Siems、Arber Zela、Timur Carstensen、Frank Hutter），并未列出具体基准结果或数据规模，因此其零样本预测效果目前仍属作者主张，尚待独立验证。

reddit · r/MachineLearning · /u/Yossarian\_1234 · 10月18日 16:43

**「背景：DeltaProduct 线性 RNN」** TempoPFN 所采用的 DeltaProduct 是一种线性循环神经网络架构，由同一 AutoML 团队（Frank Hutter 等）于 2025 年 2 月提出。据其论文与代码库说明，DeltaProduct 在状态追踪和语言建模任务上优于 DeltaNet，并显著改善了长度外推能力，其设计目标是在状态转移的表达能力与计算效率之间取得平衡。TempoPFN 正是以这一架构作为时间序列基础模型的骨干。

**「影响」** 对构建时间序列基础模型的开发者而言，可直接复用这套生成器与预训练权重来训练或评估模型，不必自建合成数据管线；但帖子未说明生成器的推理成本、权重许可证或与 Toto-2、TS-ICL 的兼容细节，实际采用前需要查阅仓库和论文确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2502.10297">[2502.10297] DeltaProduct: Improving State-Tracking in Linear ...</a></li>
<li><a href="https://www.emergentmind.com/topics/deltaproduct">DeltaProduct: Expressive &amp; Efficient Linear RNN</a></li>
<li><a href="https://github.com/automl/DeltaProduct">GitHub - automl/DeltaProduct: DeltaProduct is a new linear ...</a></li>

</ul>
</details>

**标签**: `#time series forecasting`, `#foundation models`, `#synthetic data`, `#linear RNNs`, `#NeurIPS`

---

<a id="item-tech-news-11"></a>
### [SemiAnalysis：英伟达 vLLM 优化使 Kimi K3 提速 1.68 倍](https://x.com/SemiAnalysis_/status/2111627094878790023) ⭐️ 7.0/10

SemiAnalysis 在 X 上称，英伟达通过一项上游 vLLM 优化，在 2.8 万亿参数的 Kimi K3 模型上达到每用户每秒 423 个 token，并在相同硬件上实现 1.68 倍加速。该帖称，这项优化由英伟达 CentML 的 Benjamin 使用 Cute DSL 编写解码专用内核，并通过 Megakernel 融合实现；英伟达同时还在为 vLLM 开发对 DeepSeek v4.1 等模型的适配。现有信息来自简短转帖，未提供基准测试方法、硬件配置或可复现细节，因此 423 tokens/s 和 1.68 倍仍是 SemiAnalysis 转述的指标。

telegram · zaihuapd · 10月18日 08:20

**「背景」** vLLM 是常用的大模型推理与服务框架，解码阶段按 token 逐步生成，专用内核与算子融合会直接影响单用户吞吐。Kimi K3 的参数量为 2.8 万亿，因此这类底层内核优化对其推理服务尤为关键。

**「影响」** 如果该优化进入用户实际部署的 vLLM 版本，运行 Kimi K3 的服务方可能获得更高的单用户解码吞吐；但转帖未说明适用的 GPU 型号、vLLM 版本或代码合并状态，采用前需要自行复核。

**标签**: `#vLLM`, `#NVIDIA`, `#LLM inference`, `#kernel optimization`, `#Cute DSL`

---

<a id="item-tech-news-12"></a>
### [Google 开源 Harness² 递归智能体优化框架](https://github.com/google-research/harness2) ⭐️ 7.0/10

Google Research 已在 GitHub 开源 Harness²，这是一个通过两层递归来优化 LLM 智能体、并且无需调整模型权重的框架。项目方称，该框架支持并行与顺序两种递归模式，在 WorkBuddy-Bench 等基准测试上最高提升 11.5 分，并已集成多款基准测试。代码以 Apache 2.0 协议发布；上述基准提升来自项目自述，在给定的材料中没有独立复现或验证结果。

telegram · zaihuapd · 10月18日 11:24

**「背景」** 在 LLM 智能体中，harness 指模型之外的提示、工具调用和流程代码等脚手架；Harness² 的出发点是保持模型权重不变，通过递归改写这层脚手架来适应设计时未见过的新任务。其论文称，该框架连接任务级递归与另一层递归，任务级递归使用对比式 Propose-Probe-Compose 步骤，在没有标准答案验证器的情况下引导对 harness 的修改。

**「对开发者的直接影响」** 对智能体开发者来说，可以在 Apache 2.0 许可下集成该框架，并用并行或顺序递归配置测试现有的冻结模型；但最高 11.5 分的提升是项目方在 WorkBuddy-Bench 等基准上公布的结果，尚未见独立复现，选型前应在自身任务上验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/google-research/harness2">google-research/harness2 - GitHub</a></li>
<li><a href="https://arxiv.org/abs/2610.14224">[2610.14224] Harness^2: Recursive Agent Harnessing for an ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/18/google-harness2-recursive-agent-harnessing-framework/">Google Open-Sources Harness 2 , a Recursive Agent... - MarkTechPost</a></li>
<li><a href="https://github.com/google-research/harness2">GitHub - google - research / harness 2 · GitHub</a></li>

</ul>
</details>

**标签**: `#LLM agents`, `#recursive optimization`, `#agent frameworks`, `#open source`, `#Google Research`

---

<a id="item-tech-news-13"></a>
### [Anthropic 游说法案：AI 致 50 死或 10 亿美元损失才可叫停](https://www.tomshardware.com/tech-industry/artificial-intelligence/anthropics-proposed-ai-safety-bill-only-kicks-in-if-50-deaths-or-usd1-billion-in-damages-are-on-the-line-proposal-would-effectively-make-the-commerce-department-the-only-agency-capable-of-stopping-an-ai-model) ⭐️ 7.0/10

Anthropic 正游说一项 AI 安全法案，拟规定只有当模型可能造成超过 10 亿美元损失，或导致超过 50 人死亡或受伤时，政府才可阻止其发布。据 Tom&\#x27;s Hardware 援引 Politico 报道，该提案要求由美国商务部注册的独立第三方定期评估实验室和模型，并在发现生物武器、AI 网络攻击或失控风险后 72 小时内报告；是否停止发布须由商务部提交哥伦比亚特区联邦法院，由法官裁定。除商务部外，其他美国机构不得下令叫停模型。Anthropic 称该提案源自其 6 月起推动的 Advanced AI Framework，目前仍是待国会审议的提案，而非已生效法律。

telegram · zaihuapd · 10月18日 12:40

**「背景」** 这项法案目前只是 Anthropic 的游说提案，尚未成为生效法律。Anthropic 表示，其内容来自公司自 6 月起向联邦和州议员推介的《Advanced AI Framework》；Politico 率先报道了该提案。

**「实际影响」** 若该提案成为法律，AI 实验室和第三方评估机构将面对一套集中化的合规流程：评估须由商务部注册机构进行，特定风险须在 72 小时内上报，而其他联邦机构无法单独叫停模型发布，最终决定权落到哥伦比亚特区联邦法官手中。

**「社区讨论」** Tom&\#x27;s Hardware 评论区对提案多持怀疑态度。有读者认为，让商务部介入更像监管俘获，可能被用来限制外国开放权重模型；也有人质疑“50 人或 10 亿美元”的门槛由谁认定、在开发完成前如何判断，以及美国法律对境外数据中心和开发者是否有效。

<details><summary>参考链接</summary>
<ul>
<li>Anthropic quietly pitches its own AI safety bill to lawmakers - POLITICO</li>

</ul>
</details>

**标签**: `#AI safety regulation`, `#Anthropic`, `#AI policy`, `#risk thresholds`, `#U.S. legislation`

---

<a id="item-tech-news-14"></a>
### [软件的价值不只在代码，更在人的判断与品味](https://karrisaarinen.com/posts/someone-behind-the-software/) ⭐️ 6.0/10

这是一篇讨论软件价值的文章，核心论点是软件的价值来自人的判断、品味以及决定构建什么，而不只是代码或架构。文章放在 AI 辅助编程日益普及的背景下，提醒读者关注产品意图和人的选择。它没有发布新产品、版本或可独立验证的技术结果。

hackernews · tosh · 10月18日 16:32 · [社区讨论](https://news.ycombinator.com/item?id=50142573)

**「背景」** 作者卡尔里·萨里宁（Karri Saarinen）是 Linear 的联合创始人兼 CEO，这篇随笔发表在他的个人网站，并在 Hacker News 上引发讨论。它是一篇产品构建者的观点文章，讨论的是软件背后人的判断与品味，并非产品发布或技术论文。

**「评论讨论」** 评论者 jwr 认同这一观点，称在 AI 已能写出更好代码、并逐步逼近架构能力的情况下，SaaS 的价值在于决定做什么和不做什么、定义产品愿景。allenu 补充说 AI 没有价值观、意图和品味；ajrouvoet 提到 Dorothy Sayers《The Mind of the Maker》中创意分为想法、实现和互动的框架；jakub\_g 则观察到产品常不断叠加能力，却缺少统一视角。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://karrisaarinen.com/">Karri Saarinen</a></li>
<li><a href="https://daily.dev/posts/someone-behind-the-software-saqawwlwf">Someone Behind the Software - daily.dev</a></li>

</ul>
</details>

**标签**: `#AI-assisted development`, `#software engineering culture`, `#human factors`, `#product design`

---

<a id="item-tech-news-15"></a>
### [把 Wi-Fi 网卡变成 SDR：未公开 I/Q 采样能力扩散](https://hackaday.com/2026/10/18/turning-a-wi-fi-adapter-into-an-sdr/) ⭐️ 6.0/10

Hackaday 于 10 月 18 日发文，介绍如何将一块 Wi-Fi 网卡当作软件定义无线电（SDR）使用，文中配有一张 GQRX 瀑布图截图。该做法建立在约两周前在 ESP32 芯片中发现的未公开 I/Q 采样功能之上；文章称，此后在其他无线芯片中也陆续发现了类似能力。需要说明的是，所提供的原文只是被截断的开头，没有给出网卡型号、采样率、可调谐频率范围，也未说明所需的固件或主机软件，因此目前无法确认该方案适用于哪些硬件，也无法确认实际接收效果；相关能力也尚未见到独立测量验证。

rss · Hackaday · 10月18日 08:00

**「背景」** 此前公开的 ESP-SDR 项目利用了 ESP32 中一个未公开的原始 I/Q 采样功能：固件绕过芯片的 Wi‑Fi/蓝牙固定功能调制解调器，从接收链路抓取基带样本，再经 USB 或 UART 传给电脑，使普通 ESP32 板可作为仅接收的软件定义无线电使用，而无需额外 SDR 硬件。该项目的说明还指出，这些样本可用于查看频谱并研究普通 Wi‑Fi 数据包之外的信号。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://espargos.net/espsdr/">ESPARGOS - ESP-SDR: Raw IQ Capture with Espressif&#x27;s ESP32 Chips</a></li>
<li><a href="https://github.com/ESPARGOS/esp-sdr">GitHub - ESPARGOS/esp-sdr: ESP-SDR uses the undocumented raw ...</a></li>
<li><a href="https://blog.adafruit.com/2026/09/30/esp-sdr-uses-undocumented-raw-i-q-capture-of-esp32-to-make-software-defined-radios/">ESP-SDR uses undocumented raw I/Q capture of ESP32 to make ...</a></li>

</ul>
</details>

**标签**: `#SDR`, `#Wi-Fi`, `#ESP32`, `#wireless hardware`, `#hardware hacking`

---

<a id="item-tech-news-16"></a>
### [浙大提出具身智能体长程记忆基准](https://mp.weixin.qq.com/s?__biz=MzI3MTA0MTk1MA==&amp;mid=2652735627&amp;idx=3&amp;sn=2195898b4588173b111e6ffc13732156) ⭐️ 6.0/10

浙江大学研究团队提出一个面向具身智能体的长程记忆评测基准，主题是“看见不等于记住”，即检验智能体在长程任务中能否持续保留并调用此前的观察与经验，而不只是当帧感知。目前公开信息只有标题与摘要，未披露任务设计、基准规模、评价指标、实验数据，也没有第三方复现或采用记录，因此它与已有具身智能评测基准相比有多大增量尚不清楚。

rss · 新智元 · 10月18日 05:00

**「长程具身任务为何需要记忆基准」** 具身智能体执行长程任务时，必须在多个步骤之间保留并更新环境状态，例如物体被移动或遮挡后仍能回忆其位置；单帧视觉感知无法覆盖这一能力，因此需要专门的评测基准把“记忆”拆成可测量的子项。arXiv 在 2026 年 9 月收录的相关工作（如 EMem-Bench）已把细粒度视觉记忆、动态世界状态追踪以及通过交互记录世界状态列为评测目标，反映出该方向正从概念讨论转向建立可复现的测试协议。

**「对具身智能体评测的影响」** 对具身智能体的研究者与开发者而言，该基准一旦公开，将提供一个专门考察长程记忆的评测入口；但现有公开信息未披露任务规模、评价指标或基线结果，因此尚无法判断它能否真正区分“看见”与“记住”。同期同类评测显示，部分可观测、世界状态被覆盖以及长期记忆难以转化为具体动作，仍是这类基准反复暴露的问题（WorldLines，2026 年 8 月），所以新基准的实用价值取决于它是否覆盖这些失效模式。

<details><summary>参考链接</summary>
<ul>
<li>Benchmarking Embodied Memory for Long-Horizon Embodied Tasks - arXiv</li>
<li>EmbodiedMemory-Bench: Benchmarking Embodied Memory ...</li>
<li>FindingDory: A Benchmark to EvaluateMemory in Embodied Agents</li>
<li>WorldLines: Benchmarking and Modeling Long-Horizon Stateful ...</li>

</ul>
</details>

**标签**: `#embodied AI`, `#robotics`, `#memory`, `#benchmark`, `#machine learning`

---

<a id="item-tech-news-17"></a>
### [官方 DLSS 5 被提取：非支持游戏最高提速 90%](https://www.tomshardware.com/pc-components/gpus/modders-used-the-official-dlss-5-release-on-unsupported-games-and-are-seeing-up-to-90-percent-better-performance-than-the-leaked-dlss-5-nvidia-says-new-nr-model-uses-20-percent-less-vram-and-processes-neural-workloads-up-to-2x-faster) ⭐️ 6.0/10

模组制作者已从《NBA 2K27》提取版本 310.9.16.0 的官方 DLSS 5 神经渲染构建，并借助 RenoDX 或 OptiScaler 将其注入未获官方支持的游戏。社区测试称，在《巫师 3》原生 DLSS 5 路径下，新 NR 模型比旧模型最高快 90%，但报道另一处给出的最高增幅为 40%，两者都是模组制作者的结果，而非 Nvidia 官方基准。Nvidia 表示新模型体积缩小 24%，4K 下显存占用减少 20%，处理神经渲染负载最高快 2 倍；新 DLL 同时保留旧模型 Preset A 和新模型 Preset B。

rss · Tom&\#x27;s Hardware · 10月18日 12:45

**「背景」** DLSS 5 的 Neural Rendering 依赖计算和显存开销较大的 AI 模型，因此英伟达在新模型中优先缩小体积、降低 4K 下的显存占用。此前泄露版和早期发布版已在模改社区流传，玩家通过 RenoDX 或 OptiScaler 将 DLSS DLL 注入未获官方支持的游戏，本次新旧模型对比正是在这一基础上进行。

**「影响」** 对想在不被官方支持的显卡上试用 DLSS 5 的玩家，社区已修改运行时以支持 RTX 20 系列，但这依赖非官方注入和修改，兼容性与稳定性没有 Nvidia 保障；报道称 Nvidia 目前计划面向 RTX 40 系列发布 DLSS 5，尚无 RTX 30/20 系列获得官方支持的报道。

**标签**: `#DLSS`, `#Nvidia`, `#GPU`, `#neural rendering`, `#gaming`

---

<a id="item-tech-news-18"></a>
### [MIT 研发软性三维形状传感皮肤，误差低于半厘米](https://www.tomshardware.com/virtual-reality/mit-engineers-build-soft-3d-shape-sensing-skin-for-gaming-and-vr-tracks-3d-movement-and-touch-with-sub-half-centimeter-error) ⭐️ 6.0/10

MIT 研究人员演示了一种可穿戴的柔性光学波导传感片，能重建自身三维形状并感知按压，面向游戏、VR 和物理治疗等场景。论文《Toward fully soft and multifunctional shape sensing via optical waveguide arrays》给出的实物测试中，16×16×0.5 厘米硅胶片内嵌两层共 14 根、每根 160 毫米长的波导，贴合三种已知形状模具时的表面重建均方根误差分别为 0.37、0.28 和 0.45 厘米。模拟中，14 根波导最多断开 3 根时误差仍低于 0.3 厘米，断开 5 根后升至约 1 厘米或更高，显示出一定损伤容限。当前光纤粗约 1 毫米，传感面虽为全软但电子件仍在薄片边缘，MATLAB 重建约每秒 3 次，离衣物级可穿戴和低延迟交互仍有距离。

rss · Tom&\#x27;s Hardware · 10月18日 12:25

**「背景」** 这类形状传感依赖光纤弯曲时的漏光量变化：传统光纤由透明芯和包层构成，弯曲会使到达末端的光减少，因此测量光输出即可推算弯曲程度。MIT 的改动是用柔性橡胶芯替代玻璃芯，并采用黑色染色包层、刻意粗糙化光纤一侧，让向不同方向弯曲产生不同光损，从而获得方向信息。

**「影响」** 对 VR 和游戏开发者而言，这仍是实验室原型：关节处的拉伸会让形状算法失准，团队在腕、肘演示中改用更简单的缩放方法；力感知也没有校准出具体力度，且与形状模式分开运行。若要用于智能衣物，还需先把约 1 毫米粗的波导缩到数十微米、增加波导数量并换用更快求解器。

**标签**: `#soft robotics`, `#shape sensing`, `#optical fiber sensors`, `#wearable hardware`, `#VR/AR`

---

<a id="item-tech-news-19"></a>
### [SemiAnalysis：300 多项数据中心禁令仅拖慢三个美国项目](https://www.tomshardware.com/tech-industry/data-centers/300-plus-local-data-center-bans-have-only-delayed-just-three-us-projects-bans-much-more-bark-than-bite-only-2-3-gigawatts-of-data-centers-are-held-up-versus-38-gigawatts-expected-online-in-2027) ⭐️ 6.0/10

SemiAnalysis 的项目逐项审计显示，美国 300 多项地方数据中心建设暂停令目前可能只导致三个项目延期，约 2.3 GW 容量受阻；相比之下，其预测 2027 年美国将有 38 GW 数据中心 IT 容量上线。该机构称，过去 12 个月这一预测“几乎没有变化”，因为已生效的暂停令覆盖约 20 GW，但其中仅约 1.5 GW 延期，纽约州的暂停令另增加 0.8 GW。报告同时指出，2.3 GW 的数字未计入得克萨斯州环境质量委员会（TCEQ）的许可暂停，后者可能持续到 ERCOT 于 12 月中旬完成审查。

rss · Tom&\#x27;s Hardware · 10月18日 11:45

**「背景：地方暂停令的适用范围」** 地方数据中心暂停令通常是对新申请设置的临时法律冻结，并不撤销已获批准的项目；已开工、已完全许可或不在辖区内的项目因此不受约束。SemiAnalysis 的审计正是按地块、许可、生效时间和用途逐项比对，只有这些条件同时命中，暂停令才可能改变项目交付时间。

**「德州许可冻结扩大工期风险」** 德州州长 Abbott 已于 9 月 21 日指示 TCEQ 暂停审批数据中心许可，直至 ERCOT 完成电网审计；Bracewell 指出，该暂停连离网和表后项目也覆盖，并预计持续到 2026 年 12 月中旬。对开发商而言，即使项目不进入 ERCOT 并网队列，也需把许可冻结及 10 月 19 日的 TCEQ 合规报告节点计入工期；SemiAnalysis 的 2.3 GW 延误统计未包含这一暂停，因此实际受阻容量可能高于其估算。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://gov.texas.gov/news/post/governor-abbott-directs-tceq-to-halt-data-center-permits">Governor Abbott Directs TCEQ To Halt Data Center Permits</a></li>
<li><a href="https://www.bracewell.com/resources/governor-abbott-orders-tceq-to-pause-all-permit-issuance-for-data-center-projects/">Governor Abbott Orders TCEQ to Pause All Permit Issuance for ...</a></li>
<li><a href="https://www.troutman.com/insights/governor-abbott-directs-tceq-to-halt-all-data-center-permits-pending-ercot-twdb-audits/">Governor Abbott Directs TCEQ to Halt All Data Center Permits ...</a></li>

</ul>
</details>

**标签**: `#data centers`, `#AI infrastructure`, `#local policy`, `#capacity forecast`, `#power constraints`

---

<a id="item-tech-news-20"></a>
### [FOI 开源 WiFireNet：用 Wi-Fi 信号识别隐藏手枪](https://www.tomshardware.com/tech-industry/artificial-intelligence/researchers-train-ai-to-detect-concealed-handguns-using-wi-fi-signals-open-source-wifirenet-achieves-precision-detection-on-older-802-11a-standard-by-analyzing-how-weapons-distort-wireless-signals) ⭐️ 6.0/10

瑞典国防研究局（FOI）的研究人员公开了 WiFireNet：一个利用 Wi-Fi 信道状态信息（CSI）识别隐藏手枪的开源 AI 原型，相关论文于 10 月 13 日发布在 arXiv。该系统由 Wi-Fi 发射端、接收端和深度学习模型组成，在最多 4 人移动的小型室内受控试验中，平均手枪检测精确率为 72.5%；若要求定位武器在携带者身上的具体位置，精确率降至 53.8%。它基于修改过的 1999 年 IEEE 802.11a 标准做概念验证，在未见过或未测试的室内布局中表现不佳，团队计划后续改用 Wi-Fi 7 和 Wi-Fi 8 获取更高分辨率 CSI。代码、模型和 WiFire Dataset 数据均已开源。

rss · Tom&\#x27;s Hardware · 10月18日 11:00

**「背景」** Wi-Fi 信道状态信息（CSI）记录信号遇到人体或物体后如何反射、穿透和衰减，是 Wi-Fi 感知在不依赖摄像头的情况下推断目标属性的原始数据。安全研究者此前已展示，普通 Wi-Fi 路由器可利用这类信号以 99.5% 的准确率识别人体，而 WiFireNet 将同一类 CSI 输入用于识别隐蔽手枪；其代码和模型已在 GitHub 公开。

**「实际影响」** 对试图部署这类系统的机构而言，当前结果只适用于已知布局、受控室内的概念验证，不能当作真实场景的检测精度；其无法指出武器在人体上的位置，也限制了安检处置。开源代码、模型和数据集则为其他研究者提供了可复现的基线，用于测试更新 Wi-Fi 标准下的 CSI。与此同时，报道提到批评者认为 Wi-Fi 感知的普及和监管框架缺失会带来隐私风险，部署前需要面对这一合规问题。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2610.18736">Concealed Handgun Detection using WiFi Signals - arXiv.org</a></li>
<li><a href="https://github.com/persson-erik/WiFireNet">WiFireNet: Concealed Handgun Detection using WiFi Signals</a></li>

</ul>
</details>

**标签**: `#Wi-Fi sensing`, `#AI security`, `#channel state information`, `#open-source research`, `#wireless hardware`

---

<a id="item-tech-news-21"></a>
### [大疆发布首款换电机场 Dock 4，未获美国 FCC 认证](https://www.tomshardware.com/tech-industry/drones/djis-first-battery-swapping-dock-gets-drones-recharged-and-back-in-the-air-in-under-45-seconds-but-dock-4-has-no-fcc-clearance-for-u-s-sale) ⭐️ 6.0/10

大疆宣布推出其首款换电式无人机机场 Dock 4，称自动换电耗时 25 秒，从降落到再次起飞可在 45 秒内完成，而常规充电约需 30 分钟。该机场可同时为两块 925 克、260 Wh、额定 400 次循环的电池包充电，每块从 15% 充至 95% 约需 27 分钟；装载至少两块电池时，即使市电中断也能继续换电，但备用电力不会给电池包充电。Dock 4 只能搭配 Matrice 5TD 无人机和 DJI O4 Ground Station 使用，中国合作伙伴已开始接受 Dock 4、Matrice 5TD 和 O4 Ground Station 套装订单，硬件价格为 167,999 元（约 2.5 万美元）。大疆规格表未列出 FCC 数据，报道指出这使该产品未获 FCC 授权、不能在美国销售，除非美国相关部门认定其不构成安全风险；大疆今年早些时候已起诉 FCC。

rss · Tom&\#x27;s Hardware · 10月18日 10:30

**「背景」** Dock 4 是 DJI 首款采用自动换电的机库；其前代 Dock 3 搭配的 Matrice 4TD 在热成像分辨率、长焦和激光测距等指标上均低于新的 Matrice 5TD。美国销售受限则源于 FCC 去年 12 月将外国制造的无人机及关键部件列入 Covered List，新机型须经美国国防部或国土安全部认定不构成安全风险才能获得授权，DJI 今年已就此起诉 FCC。

**「影响」** 对应急响应等需要连续作业的机构而言，这套能力要求按整套新硬件采购：Dock 4 只能配 Matrice 5TD 和 O4 Ground Station，现有的 Dock 3 与 Matrice 4TD 组合不能直接沿用；市电中断时虽可继续换电，但备用电池不负责给电池包充电，持续外勤仍需单独规划电力补给。

**标签**: `#drones`, `#robotics`, `#hardware`, `#batteries`, `#regulatory`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [Intel 8087 浮点加减的微码实现](http://www.righto.com/2026/10/8087-addition-subtraction-microcode.html) ⭐️ 9.0/10

rss · righto.com \(Ken Shirriff\) · 10月18日 16:14

**「背景」** 1980 年推出的 Intel 8087 让 IBM PC 等系统的浮点运算比 8086 软件模拟快近两个数量级；Ken Shirriff 通过开盖显微成像和微码反汇编，追问其加减法究竟如何落到硅片电路与微码上。

**「方案」** 8087 内部以 80 位“临时实数”保存数值，寄存器堆带有 zero、valid、special、empty 标签；数据通路的核心是 69 位整数加法器、可任意移位的移位器、前导零计数器和指数转换器。加减法微码先把两个操作数送入 tmpA 和 tmpB，比较指数并右移较小者对齐，再用整数加/减完成尾数运算；由于符号组合，加法指令可能触发无符号减法，反之亦然，因此硬件用符号异或判断实际路径。随后微码根据进位或前导零进行左/右规格化，用两位 expAdj 和 tmpB 的指数字段记录指数修正，并在 32/64/80 位精度间调整、处理 guard/round/sticky 舍入。零结果还要区分+0 和-0，公共微码用大量条件分支处理无穷、NaN、非规格化数、伪零等特例，并可能触发异常或返回特殊值。

**「启示」** 作者由此说明，看似基础的浮点加减其实是算法、微码控制流与专用硅电路紧密配合的产物；8087 对特殊值的处理也塑造了后来的 IEEE-754 标准，尽管其中部分特例因代价过高而被舍弃。

**标签**: `#Intel 8087`, `#floating point`, `#microcode`, `#reverse engineering`, `#computer architecture`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [英央行副行长警告：对冲基金杠杆化持债或放大债市冲击](https://www.cnbc.com/2026/10/18/hedge-funds-bond-market-turmoil.html) ⭐️ 7.0/10

英国央行副行长 Sarah Breeden 周四警告，对冲基金在政府债券市场占比上升且更多使用杠杆，使局部市场动荡演变为更广泛金融冲击的可能性高于以往。美国金融研究办公室 8 月 19 日的数据显示，截至 2025 年底，对冲基金持有规模 30 万亿美元的美国国债市场中的 7%，创纪录高位。

rss · CNBC Top News · 10月18日 06:13

**「背景」** 国际货币基金组织（IMF）周二发布的《全球金融稳定报告》也警告，对冲基金通过基差交易——买入美国国债现券、卖空对应期货以赚取价差——等策略加杠杆并扎堆交易，可能在市场承压时放大冲击。

**「影响」** IMF 指出，若债市压力外溢，向高杠杆基金提供融资和交易服务的银行主经纪业务是可能受影响的渠道之一。

**标签**: `#hedge funds`, `#bond market`, `#financial stability`, `#leverage`, `#Treasury market`

---

<a id="item-finance-news-2"></a>
### [特朗普以放宽制裁换俄罗斯柴油：普京获政治收益，乌克兰承压](https://www.cnbc.com/2026/10/17/trump-diesel-russia-ukraine-war.html) ⭐️ 7.0/10

美国总统特朗普与俄罗斯总统普京达成安排，美国豁免部分对俄关键制裁，以换取俄方向全球市场供应 480 万公吨柴油，豁免期至 2027 年 4 月。CNBC 引述专家估算，这一数量仅约相当于美国 10 天的柴油需求，对全球油价和俄财政的直接提振都有限，更大收益在政治层面。

rss · CNBC Top News · 10月18日 07:22

**「背景」** 美国国会此前通过了一揽子对俄制裁方案，特朗普于周五签署行政令，豁免了其中关键条款，以换取俄罗斯向全球市场供应柴油；据标普全球报道，这项豁免（包括允许柴油输美）有效期至 2027 年 4 月 7 日。

**「影响」** 对乌克兰及其欧洲盟友而言，这一豁免可能削弱西方制裁的可信度，并加大基辅在冬季战事中对美国军援和情报支持的依赖风险。

<details><summary>参考链接</summary>
<ul>
<li>Trump doubles down after waiving new Russia sanctions, calling it a ...</li>
<li>NYMEX ULSD crack weakens after Trump announces additional diesel ...</li>

</ul>
</details>

**标签**: `#Russia sanctions`, `#diesel markets`, `#Ukraine war`, `#US energy policy`, `#geopolitical risk`

---

<a id="item-finance-news-3"></a>
### [美国 AI 基建热潮现裂痕：至少 47 个大型数据中心项目受阻](https://www.ft.com/content/9ea5a37d-15c9-4d5b-94d6-719048c9cd3c?syn-25a6b1a6=1) ⭐️ 7.0/10

美国 AI 基础设施热潮出现裂痕：2026 年以来至少 47 个大型数据中心项目被推迟、撤回或叫停，分析机构估计规划项目中仅约 35%具有较高可行性。2025 至 2032 年美国 AI 基建支出预计超过 10 万亿美元，但融资成本上升、审批受阻和公众反对正在拖慢项目落地。

telegram · zaihuapd · 10月18日 08:52

**「背景」** CoreWeave 是一家在美国和欧洲运营 AI 数据中心、出租英伟达 GPU 算力的云服务商；2025 年 9 月英伟达与其签署 63 亿美元云计算容量订单，并约定在 2032 年 4 月前购买其未售出的算力容量（tool-1-2、tool-1-3）。这类合约让英伟达的芯片收入与数据中心租用需求直接挂钩，因此 CoreWeave 股价大跌被市场视为 AI 基建扩张降温的信号。

**「影响」** 融资压力已传导至相关企业：英伟达支持的云服务商 CoreWeave 周五跌超 11%，费城半导体指数连续第 8 个交易日下跌，追平 2006 年以来最长连跌纪录。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://money.usnews.com/investing/news/articles/2025-09-15/coreweave-nvidia-sign-new-6-3-billion-deal-for-cloud-computing-capacity">CoreWeave , Nvidia Sign $6.3 Billion Cloud Computing Capacity Order</a></li>
<li><a href="https://www.reuters.com/business/coreweave-nvidia-sign-63-billion-cloud-computing-capacity-order-2025-09-15/">reuters.com/business/ coreweave - nvidia -sign-63-billion- cloud ...</a></li>

</ul>
</details>

**标签**: `#AI infrastructure`, `#data centers`, `#financing costs`, `#semiconductor stocks`, `#CoreWeave`

---