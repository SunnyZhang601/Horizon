---
layout: default
title: "Horizon Summary: 2026-10-12 (ZH)"
date: 2026-10-12
lang: zh
---

> 从 33 条内容中筛选出 8 条重要资讯。

---

**科技新闻**
1. [Terence Tao 的 Math 2.0 幻灯片与 AI 数学讨论](#item-tech-news-1) ⭐️ 8.0/10
2. [Passkeys 被指为陷阱：平台锁定与可移植性之争](#item-tech-news-2) ⭐️ 7.0/10
3. [开源项目将 AI 文本检测器压缩至 97 MB 实现浏览器端运行](#item-tech-news-3) ⭐️ 7.0/10
4. [切片 Wasserstein 嵌入 + 自建 HNSW 做 4.8 万幅画作配色检索](#item-tech-news-4) ⭐️ 7.0/10
5. [丘成桐牵头成立数学与 AI 实验室联盟](#item-tech-news-5) ⭐️ 7.0/10

**科技博客**
1. [软件工程师没资格对 AI 做卢德派](#item-tech-blog-1) ⭐️ 5.0/10

**财经新闻**
1. [外资年内净撤出韩国股市约 1310 亿美元](#item-finance-news-1) ⭐️ 7.0/10
2. [中欧就混动与电动汽车贸易达成共识，中方配额不低于其他进口来源地](#item-finance-news-2) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Terence Tao 的 Math 2.0 幻灯片与 AI 数学讨论](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) ⭐️ 8.0/10

Terence Tao 的演讲幻灯片《Math 2.0》在 Hacker News 上引发讨论，主题是 AI 在数学中日益增长的作用。据分析摘要，相关讨论有 421 条评论，焦点包括 AI 驱动的发现、研究文化以及领域专长。由于源内容未提供，这里只能确认幻灯片主题与讨论概况，无法核实其中的具体数学主张或突破。

hackernews · Anon84 · 10月11日 13:16 · [社区讨论](https://news.ycombinator.com/item?id=50043026)

**「背景」** 这些幻灯片属于陶哲轩（Terence Tao）围绕“AI 与数学”的系列发言：他在 2026 年 7 月 24 日国际数学家大会（ICM 2026）的公开演讲中讨论了数学界应如何应对已能执行研究级数学任务的 AI 工具，并在 8 月 18 日将其整理为 arXiv 论文。2026 年 10 月 10 日，他在博客中把此前的数学实践称为“Math 1.0”，把过度侧重用 AI 自动求解未决问题的现状视为过渡阶段，并提出以 AI 工具同时维系数学共同体与数学理解的“Math 2.0”构想，本次 Caltech 演讲正是在这一框架下展开。

**「社区讨论」** 评论者对 Tao 关于癌症医学的类比提出异议：dekhn 认为该部分信息不足，并称其询问的多数医生或研究者不会因为 AI 设计的药物机制未被理解而拒绝使用；squidmaster 则认为 Tao 超出了本行，并以全身麻醉机制同样未完全明确为例。另有评论者提到 AI 系统解决了长期未解的问题、导致已提交的资助申请需要重写并带来“失去一个领域”的感受，thomasahle 则把 Tao 的观点解释为纯数学应维护高质量的理论“代码库”，而当前数学 AI 还不会是好的贡献者。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://teorth.github.io/tao-web/slides/age-of-ai-icm-2026.pdf">Mathematics in the age of AI - Public lecture, International ...</a></li>
<li><a href="https://terrytao.wordpress.com/2026/10/10/math-2-0/">Math 2.0 | What&#x27;s new</a></li>
<li><a href="https://arxiv.org/pdf/2608.16753">MATHEMATICS IN THE AGE OF AI - arXiv.org</a></li>

</ul>
</details>

**标签**: `#AI for mathematics`, `#Terence Tao`, `#mathematical research`, `#AI in science`, `#research culture`

---

<a id="item-tech-news-2"></a>
### [Passkeys 被指为陷阱：平台锁定与可移植性之争](https://nonfunctional.substack.com/p/passkeys-are-a-trap-do-not-use-them) ⭐️ 7.0/10

一篇题为“Passkeys are a trap”的批评文章认为，passkeys 在当前实现中会造成平台锁定和可移植性问题，并可能通过强制采用、备份限制、证明（attestation）和设备白名单加剧这一问题。该文是观点分析，并非新功能发布或安全事件；其核心主张是用户可能难以跨平台迁移或备份凭据，且部分服务可能强制使用硬件 passkey。文章没有提供可独立验证的漏洞或测量数据，相关技术细节主要来自 Hacker News 评论中的讨论。

hackernews · laurex · 10月11日 21:59 · [社区讨论](https://news.ycombinator.com/item?id=50048312)

**「背景」** Passkey 是一种与用户账户及特定网站或应用绑定的数字凭证，用户无需输入用户名、密码，也无需提供额外的认证因子即可完成登录（tool-2-3）。与之相关的 attestation（认证声明）机制用于注册环节：厂商的依赖方实现指南专门讨论如何在注册时利用 passkey attestation，这类证明通常存放在认证器的 TPM 中（tool-2-1）。这正是原文评论区围绕设备白名单、硬件限制与平台锁定展开争论的技术前提。

**「影响」** 评论者指出，若平台按设备名称或制造商白名单强制使用硬件 passkey，用户可能无法在设备间迁移或备份凭据，甚至需要携带多台设备；同时，attestation 只能在注册时要求，登录时无法追溯补加，开发者若在注册阶段强制证明会影响兼容性。

**「社区讨论」** 评论中，bramhaag 称部分平台维护设备制造商白名单，例如 OpenAI 强制使用硬件 passkey 并似乎按设备上报名称判断，他担心未来需携带多台不同厂商的设备；agwa 则指出 attestation 只能在注册时要求，登录时无法追溯要求，并质疑 Netflix 和 Twitter 是否真在注册时请求 attestation。bmitch3020 表示不愿启用 passkey，因为希望凭据可移植、可备份并自主控制强度；另有评论提到原文末尾附言承认 passkey 的域绑定特性可抵御中间人攻击。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developers.yubico.com/Passkeys/Passkey_relying_party_implementation_guidance/Attestation/">Attestation</a></li>
<li><a href="https://developers.google.com/identity/passkeys">Passkeys | Google for Developers</a></li>

</ul>
</details>

**标签**: `#passkeys`, `#authentication`, `#security`, `#platform lock-in`, `#WebAuthn`

---

<a id="item-tech-news-3"></a>
### [开源项目将 AI 文本检测器压缩至 97 MB 实现浏览器端运行](https://www.reddit.com/r/MachineLearning/comments/1x3vqip/compressed_a_roberta_aitext_detector_from_500_mb/) ⭐️ 7.0/10

Reddit 用户 /u/Alternative\_Detail31 发布了开源项目 tinydetect，把两个现成的开源检测器改造成完全在浏览器端运行：文本检测器基于 fakespot-ai/roberta-base-ai-text-detection-v1（Apache-2.0），从 fp32 的约 500 MB 压缩到约 97 MB；图像检测器基于 Community Forensics（commfor-model-384，MIT）的量化 ViT，约 26 MB。作者没有训练新模型，称工作集中在微调、压缩与浏览器运行时上：文本模型用 WiSE-FT 在原始权重与轻量微调权重之间插值，词嵌入矩阵被移出 ONNX 图并以 int4 存储（约 19 MB，另加 2 MB fp16 逐行 scale），在 JS 中反量化后送入约 75 MB 的混合精度量化 transformer 主体；分词器和 Fakespot 的 clean\_text 预处理也在 JS 中重写。运行时使用 ONNX Runtime Web 1.30，有 GPU 适配器时走 WebGPU 构建，否则用多线程 WASM，并由 service worker 注入 COOP/COEP 头以便在 GitHub Pages 上启用多线程 WASM。作者报告在其笔记本上约 100 token 的文本检查耗时约 60 ms、图像约 200 ms，同时提醒高分不能证明作者身份，短文本、改写、重度编辑、截图、裁剪以及更新的生成器都会降低准确率，首次加载的下载量也很大。

reddit · r/MachineLearning · /u/Alternative\_Detail31 · 10月12日 07:44

**「背景」** 该项目的两个基座模型此前均已公开发布：文本检测器为 fakespot-ai/roberta-base-ai-text-detection-v1（Apache-2.0），图像检测器为 OwensLab 的 Community Forensics commfor-model-384（MIT 许可，CVPR 2025，另有 224 输入的版本）。这些 fp32 权重体积约 500 MB，通常需要服务端推理，而 ONNX Runtime Web 1.30 能在浏览器内以 WebGPU 或线程化 WASM 执行 ONNX 图，这正是本次把已有检测器搬到客户端运行的技术前提。

**「影响」** 对希望本地处理敏感文本或图片的开发者而言，该项目提供了一个可自托管的浏览器端方案，输入无需上传；但部署时页面必须具备 COOP/COEP 响应头才能使用多线程 WASM（仓库用 service worker 在 GitHub Pages 上实现），WebGPU 路径则依赖访问者的 GPU 适配器，首次加载约 97 MB 文本模型加运行时对移动端仍是明显负担。作者本人也把准确率限制列为已知问题，因此结果不适合作为判定作者身份的单一依据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://huggingface.co/fakespot-ai/roberta-base-ai-text-detection-v1">fakespot - ai / roberta - base - ai - text - detection - v 1 · Hugging Face</a></li>
<li><a href="https://huggingface.co/OwensLab/commfor-model-384">OwensLab/commfor- model - 384 · Hugging Face</a></li>
<li><a href="https://github.com/JeongsooP/Community-Forensics">GitHub - JeongsooP/ Community - Forensics : Project page: https...</a></li>

</ul>
</details>

**标签**: `#model compression`, `#ONNX Runtime Web`, `#client-side ML`, `#AI-text detection`, `#quantization`

---

<a id="item-tech-news-4"></a>
### [切片 Wasserstein 嵌入 + 自建 HNSW 做 4.8 万幅画作配色检索](https://www.reddit.com/r/MachineLearning/comments/1x39uu6/sliced_wasserstein_embeddings_hnsw_for/) ⭐️ 7.0/10

一个个人开源项目 Palette Atlas 报告称，它用切片 Wasserstein（sliced Wasserstein）嵌入加自建 HNSW 索引，在 48,695 幅公有领域画作上实现了快速的配色方案近似检索。每幅画被简化为 128 个等权颜色，此时自然距离是 Earth Mover&\#x27;s Distance，但精确计算每对约需 6 ms，无法支撑近邻搜索；作者的做法是把 OKLab 颜色投影到 Fibonacci 半球的 8 个方向、排序后按 16 个分位数取均值，两向量间的 L1 距离即为各方向一维 W1 的平均值，是真实 W1 的下界。在 240 条查询上，该 8×16 L1 表示的精确 top-10 重叠率为 78%、top-10 平均仅远 1.8%，优于软颜色直方图（Hellinger，45%/13.5%）和平均色（3%/161%）。自建 HNSW（M=16、efConstruction=200）在 ef=32 时 recall@10 为 1.000、耗时 0.25 ms，而暴力搜索为 14 ms——这些都是作者自报的基准结果，属未同行评审的副项目。

reddit · r/MachineLearning · /u/Potential-Barber8658 · 10月11日 14:39

**「背景」** 调色板搜索的自然度量是 Earth Mover&\#x27;s Distance（EMD），但精确计算一对分布约需 6 ms，难以直接用于 48,695 幅画作的暴力最近邻搜索。HNSW 是一种基于分层图的近似最近邻索引，常用于高维向量检索；2025 年 ICML 的口头报告论文（Munyampirwa 等）曾质疑这种分层结构是否必要，而此项工作的嵌入内在维度约为 11，作者据此认为层级仍然有用（参见该论文关于何时无益的讨论）。

**「影响」** 对需要在调色板或图像集合上做交互式相似性检索的开发者来说，这一组合提供了可复用的取舍：作者报告在 ef=32 时以 0.25 ms 达到 recall@10 为 1.000，而精确路线每次查询约 14 ms，代价是嵌入只是真实 W1 的下界，top-10 与精确 EMD 的重叠为 78%。作者同时给出两点适用性提示——用 8 个 k-means 地标替换顶层随机节点后搜索代价基本不变（平均 2,558 次对 2,556 次距离计算），而该向量的内在维度约为 11，HNSW 的层级结构仍能带来收益（参见其引用的 Munyampirwa 等 2025 年工作）；迁移到自己的数据前应按实际召回要求重新验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://icml.cc/virtual/2025/48994">ICML Oral 2: Down with the Hierarchy : The ‘H’ in HNSW Stands for...</a></li>
<li><a href="https://www.emergentmind.com/topics/hierarchical-navigable-small-world-hnsw">Hierarchical Navigable Small World ( HNSW )</a></li>

</ul>
</details>

**标签**: `#Wasserstein distance`, `#HNSW`, `#image retrieval`, `#color palettes`, `#nearest-neighbor search`

---

<a id="item-tech-news-5"></a>
### [丘成桐牵头成立数学与 AI 实验室联盟](https://www.beijing.gov.cn/fuwu/lqfw/gggs/202610/t20261012_4897748.html) ⭐️ 7.0/10

菲尔兹奖得主、清华大学讲席教授丘成桐牵头联合多家机构，于 10 月 11 日在清华大学成立丘成桐数学与人工智能实验室联盟，由丘成桐任主席，汇集超过 1000 名科学家。联盟的目标是自主开发中国数学专用大模型，并建设 AI 辅助数学研究的基础设施，同时向量子计算、生命科学、金融经济等交叉领域拓展。丘成桐在成立时称，AI 对数学的冲击“像海啸来了”，应主动冲浪而非回避。目前公开信息仅为成立公告，未披露具体技术方案、研究成果、资金安排或第三方验证。

telegram · zaihuapd · 10月12日 03:00

**「背景」** 丘成桐是菲尔兹奖得主，现任清华大学讲席教授。此次成立的丘成桐数学与人工智能实验室联盟于 10 月 11 日在清华大学举行成立仪式，由丘成桐担任主席，联合多家机构并汇集超过 1000 名科学家，目标包括自主开发中国数学专用大模型和建设 AI 辅助数学研究的基础设施。

**「影响」** 对考虑加入的数学与 AI 研究者来说，现阶段可确认的只是联盟由丘成桐任主席、汇集超过 1000 名科学家，公告未披露资金规模、模型发布时间或技术路线，因此暂时无法据此安排算力、数据或工具链的迁移决策。与此同时，公开的数学专用模型已经存在——例如 Qwen2.5-Math 系列可用思维链和工具集成推理求解中英文数学题——联盟提出的“中国数学专用大模型”需要在能力或数据上给出可验证的差异，才能成为研究者实际替换现有工具的理由。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/QwenLM/Qwen2.5-Math">GitHub - QwenLM/Qwen2.5-Math: A series of math-specific large ...</a></li>

</ul>
</details>

**标签**: `#AI for mathematics`, `#large language models`, `#research alliance`, `#China AI`, `#Tsinghua University`

---

## 科技博客

<a id="item-tech-blog-1"></a>
### [软件工程师没资格对 AI 做卢德派](https://seangoedecke.com/software-engineers-dont-get-to-be-luddites-about-ai/) ⭐️ 5.0/10

rss · Sean Goedecke · 10月12日 00:00

**「背景」** 作者肖恩·戈德克（Sean Goedecke）观察到，许多软件工程师对 AI 自动化自己的技能感到愤怒；但他认为，这种愤怒很难成立，因为软件工程一直以来的价值恰恰来自自动化他人的工作。

**「方案」** 作者的核心论据是：从商业软件诞生起，软件工程就在取代人类劳动。VisiCalc 的开发者曾担心电子表格让簿记员失业；文中列出的被自动化行业包括录像带租赁店、商业名录与百科全书、排字公司、旅行社、唱片店、打字池、数据录入和交易大厅跑腿。因此工程师不应一边靠自动化谋生，一边宣称软件工程是不可自动化的神圣艺术。作者借用卢德派历史：卢德派是被动力织机等取代的纺织工人，而软件工程师更像制造这些机器的铁匠和机械师；但机械师约五十年后也因工艺改进被非熟练劳工（“非法人”）取代，其抗争没有暴力，四个月后因缺钱复工，还被《泰晤士报》斥为伪善，称其呼喊不过是手织工反对不可抗拒规律的老调。作者还区分了做软件工程的体验——调试 CSS、运行时错误、优雅表达问题或解谜——与软件工程的本质：用更快更便宜的机器劳动替代人力，也就是让人失业。他承认技术乐观主义当下不受欢迎，也不确定争论哪方正确，但认为工程师无论宣称什么信念，始终站在技术与自动化一边；每个开源提交都是技术进步机器的一部分。闭眼只关注谜题可以理解，但在自动化浪潮席卷本行业时公开反对进步是不体面的：既然参与过其他工作的毁灭或转型，公平起见也应接受自己的被毁灭或转型。文章主要依赖历史类比与道德一致性论证，而非技术数据或实证结果。

**「启示」** 作者因此主张，软件工程师没有立场扮演卢德派：其职业本身就是自动化他人劳动，所以更应承认自己也可能被自动化，并接受技术进步带来的毁灭与重建，而不是否认 AI 的能力或拒绝面对行业变迁。

**标签**: `#AI and employment`, `#software engineering labor`, `#automation history`, `#technology ethics`, `#Luddism`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [外资年内净撤出韩国股市约 1310 亿美元](https://m.gelonghui.com/live/2705107) ⭐️ 7.0/10

外国投资者今年已从韩国股市净撤出约 1310 亿美元（约合 8767 亿元人民币）；韩国综合指数（KOSPI）在上半年领涨后于下半年下跌约 22%，市场成交额较 5 月底峰值下降 70%。

telegram · zaihuapd · 10月11日 12:13

**「背景」** 韩国股市上半年曾是全球表现最好的主要市场之一，但行情高度依赖三星电子和 SK 海力士两家存储芯片巨头；三星外资持股比例已降至 46.38%，为 2008 年金融危机以来近 18 年最低。

**标签**: `#Korean stocks`, `#foreign outflows`, `#Samsung Electronics`, `#memory chips`, `#market concentration`

---

<a id="item-finance-news-2"></a>
### [中欧就混动与电动汽车贸易达成共识，中方配额不低于其他进口来源地](https://www.mofcom.gov.cn/xwfb/sjfzrfb/art/2026/art_4d502e1d49fd4480b39a6cfd0d752038.html) ⭐️ 7.0/10

中国商务部表示，中欧在贸易投资磋商机制下就混动汽车和电动汽车贸易达成多项共识，其中混动汽车安排以 2025 年为基准向上，中方配额不低于欧方其他进口来源地；电动汽车方面，欧方将继续推进企业价格承诺及其他复审程序。商务部未公布具体配额规模、实施时间等细节，并称中方保留在世贸组织框架下争端解决等权利。

telegram · zaihuapd · 10月12日 06:19

**「背景」** 2024 年 10 月，欧盟对自中国进口的纯电动汽车加征最高 35.3%的反补贴税，叠加 10%基础税率后最高达 45.3%，随后中国车企将出口重心转向当时未被加税的插混车型；2025 年欧盟自华进口新车超过 100 万辆、对华出口仅 16 万辆，汽车贸易失衡被欧方反复提及。

**「影响」** 对向欧洲出口混动和电动汽车的中国车企而言，配额“不低于其他进口来源地”意味着在准入数量上不被差别对待；但欧方继续保留价格承诺与复审程序，出口仍可能需按最低进口价格销售，此前大众汽车（安徽）的 CUPRA Tavascan 纯电车型即以此方式免于 20.7%的反补贴税。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.auto-cn.com/views-13309">auto-cn.com/views-13309</a></li>
<li><a href="https://post.smzdm.com/p/anv9okk0/">post.smzdm.com/p/anv9okk0</a></li>
<li><a href="https://www.chinaautosupplier.com/show_article-87647.html">chinaautosupplier.com/show_article-87647.html</a></li>

</ul>
</details>

**标签**: `#中欧贸易`, `#电动汽车`, `#混动汽车`, `#贸易政策`, `#商务部`

---