---
layout: default
title: "Horizon Summary: 2026-10-13 (ZH)"
date: 2026-10-13
lang: zh
---

> 从 46 条内容中筛选出 14 条重要资讯。

---

**科技新闻**
1. [黑客远程触发欧洲超市冷柜除霜，Danfoss 控制器受关注](#item-tech-news-1) ⭐️ 8.0/10
2. [开源项目把 WiFi 7 路由器改造成 320 Msps SDR 接收机](#item-tech-news-2) ⭐️ 8.0/10
3. [Meta 发布 Muse Wonder 模型，社区实测与隐私问题引讨论](#item-tech-news-3) ⭐️ 8.0/10
4. [Python 3.15 发布：PEP 810 惰性导入与采样分析器](#item-tech-news-4) ⭐️ 8.0/10
5. [learnc：调优现有 C 代码常量，JPEG 体积减 9.1%](#item-tech-news-5) ⭐️ 8.0/10
6. [用 C 构建现代 Web 应用并靠 chroot/pledge 降权](#item-tech-news-6) ⭐️ 7.0/10
7. [Codex CLI 被指默认安装常驻自更新后台守护进程](#item-tech-news-7) ⭐️ 7.0/10
8. [LineageOS 24.0 发布，代码库重基于 Android 17](#item-tech-news-8) ⭐️ 7.0/10
9. [Looped Diffusion Transformer：每个去噪步骤内循环运行共享模块](#item-tech-news-9) ⭐️ 7.0/10
10. [Anthropic：防蒸馏措施初步减少 90% 至 99% 提取数据](#item-tech-news-10) ⭐️ 7.0/10

**财经新闻**
1. [克利夫兰联储主席哈马克称可能需要维持限制性政策以压低通胀](#item-finance-news-1) ⭐️ 8.0/10
2. [新能源汽车出口退税率 2027 年 4 月起由 13%降至 9%](#item-finance-news-2) ⭐️ 8.0/10
3. [中国商务部：中欧就混动与电动汽车贸易达成多项共识](#item-finance-news-3) ⭐️ 7.0/10
4. [税务处罚新裁量基准 11 月施行，社保欠缴最高罚 3 倍](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [黑客远程触发欧洲超市冷柜除霜，Danfoss 控制器受关注](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

据报道，欧洲多家超市的冷柜遭网络攻击，被远程触发自动除霜，配送和店内价格也受到影响；法国连锁 Intermarché 据称有 150 家门店被针对。相关 Claroty 研究此前披露了联网 Danfoss 制冷控制器中的漏洞，但本次攻击是否利用这些漏洞、攻击者身份及确切影响范围尚未得到官方确认。事件凸显老旧联网制冷控制器与 OT 安全风险，具体技术细节和调查结论仍待公布。

hackernews · Zeekaas · 10月12日 12:16 · [社区讨论](https://news.ycombinator.com/item?id=50055304)

**「背景」** Claroty 的 Team82 研究团队在 2026 年 8 月披露，Danfoss AK-SM 800A 制冷控制器平台的嵌入式网页管理界面存在多个漏洞（CVE-2025-41450、CVE-2025-41451、CVE-2025-41520），Danfoss 随后在新固件版本中进行了修复。据 The Stack 报道，此次欧洲超市制冷事件中被利用的是否正是这批漏洞，在报道时仍存在争议。

**「对门店与顾客的实际影响」** 对受影响的超市门店而言，直接后果是联网制冷控制器被远程切入除霜模式，同时配送与门店定价系统受扰，恢复正常需要现场人工干预和抢修，期间货品损耗与营业中断风险上升。另据报道，针对 Intermarché 的这起攻击还波及约 30 万名客户，数据来自其 Drive 自提业务历史记录（tool-3-1），相关客户应警惕后续钓鱼与欺诈；也有分析认为此类事件暴露了零售业过时软件、弱访问控制和第三方风险等共性问题（tool-3-2）。

**「社区讨论」** HN 评论中，有人指出疑似涉事设备是 Danfoss SM800（2021 年停止支持）和 SC355（2016 年停止支持）等 15–20 年老控制器，并称轮班维护场景缺乏安全审查与更换预算；也有人以医院订阅制设备为例，反驳“冷柜为何要联网”的简单质疑。另有评论猜测本次事件与 2026 年 8 月美军基地冷柜异常有关，但未提供证据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claroty.com/team82/research/freeze-the-controller-defrost-the-food-uncovering-vulnerabilities-in-danfoss-refrigeration-controllers">Freeze the Controller, Defrost the Food: Uncovering ...</a></li>
<li><a href="https://www.thestack.technology/french-supermarkets-hacked-danfoss-vulnerabilities-blamed/">French supermarkets hacked: Danfoss vulnerabilities blamed</a></li>
<li><a href="https://www.connexionfrance.com/news/intermarche-cyberattack-affects-nearly-300000-customers/806317">Intermarché cyberattack 2026 : Nearly 300,000 customers&#x27; data stolen...</a></li>
<li><a href="https://insights.made-in-china.com/How-the-Intermarch-Cyberattack-Exposed-Critical-Flaws-in-U-S-Retail-Cybersecurity_STXAwugOfxIF.html">How the Intermarché Cyberattack Exposed Critical Flaws in...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#OT security`, `#embedded systems`, `#industrial control systems`, `#Danfoss`

---

<a id="item-tech-news-2"></a>
### [开源项目把 WiFi 7 路由器改造成 320 Msps SDR 接收机](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

开源项目 h0m3us3r/w1700k-sdr 展示了如何将一款 WiFi 7 路由器改造成采样率达 320 Msps 的软件定义无线电（SDR）接收机，目标用户是希望在廉价通用硬件上获得高采样率接收能力的射频与嵌入式开发者。项目以公开仓库形式发布，其采样率、5 GHz 频段接收等能力目前来自项目作者与社区评论者的描述，尚无独立测量或第三方验证。该方案定位为接收端用途，改造对象是消费级 WiFi 7 路由器硬件。

hackernews · djfergus · 10月12日 12:41 · [社区讨论](https://news.ycombinator.com/item?id=50055593)

**「背景」** Wi-Fi 7 路由器里的射频芯片本就工作在很宽的频段上，但厂商固件通常只输出 Wi-Fi 帧，不向用户暴露原始 IQ 采样，因此以往在这一频段做宽带接收一般要靠专用 SDR 硬件。该项目的做法是针对 Gemtek W1700K 所用的联发科 MT7996 射频芯片，以逐寄存器逆向得到的自定义固件替换原厂固件，从而在开机后即把射频前端作为接收机使用；采样数据由 Airoha AN7581 SoC 经 10 GbE 以零拷贝 UDP 送出，Linux 主机端负责显示实时频谱与瀑布图，覆盖 2.4、5 和 6 GHz 频段，并支持任意本振调谐。

**「移植与兼容性」** 对想复用该方案的开发者而言，评论者指出若目标设备采用相同芯片组，这套接收链路有希望移植到板上自带 PCIe/M.2 的 Banana Pi BPI-R4（官方规格为 MediaTek MT7988A / Filogic 880 四核 Cortex-A73 平台）；不过“同芯片组即可用”只是社区基于硬件的推断，仓库本身与独立测试都未给出验证，动手前仍需自行确认射频前端、接口与驱动支持。

**「社区讨论」** 评论者 yonatan8070 提到同一开发者此前还用 ESP32 Wi-Fi 微控制器做过 SDR（eSpDR），并希望此类改造能扩展到更多常见 Wi-Fi 网卡，让普通笔记本也能低成本当作 SDR 使用；thebeardisred 认为由于芯片组相同，该方案很可能也适用于自带 PCIe 的 Banana Pi R4。aftbit 则表示没想到有更便宜的方式获得 5 GHz、320 Msps 的接收能力——这些都属社区个人判断与经验推测，并非已验证结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://daily.dev/posts/turn-a-wifi-7-router-into-a-320msps-software-defined-radio-receiver-38irzaw8t">Turn a WiFi 7 Router into a 320Msps Software Defined...</a></li>
<li><a href="https://zeli.app/story/50055593">Wi-Fi 7 router turned into a 320 Msps · 56 HN comments | Zeli</a></li>
<li><a href="https://banana-pi.org/en/bananapi-router/155.html">Banana Pi BPI- R 4 Wifi 7 Router board with MTK MT 7988 A design...</a></li>
<li><a href="https://www.androidpimp.com/embedded/banana-pi-bpi-r4-pro/">Banana Pi BPI- R 4 Pro Review: The Best WiFi 7 OpenWrt Router?</a></li>

</ul>
</details>

**标签**: `#software-defined radio`, `#WiFi 7`, `#hardware hacking`, `#open source`, `#RF signal processing`

---

<a id="item-tech-news-3"></a>
### [Meta 发布 Muse Wonder 模型，社区实测与隐私问题引讨论](https://research.meta.ai/blog/muse-wonder) ⭐️ 8.0/10

Meta 于 2026 年 10 月 12 日在其研究博客（research.meta.ai）发布名为 Muse Wonder 的 AI 模型。由于本次提供的来源正文为空，公告中的模型规格、版本号、开放范围与基准成绩均无法由来源核实，以下关于性能与登录体验的说法均来自 Hacker News 评论。该发布在 Hacker News 上获得约 550 分、303 条评论，讨论集中在与 Opus 5.5 的横向实测以及对 Meta 账号登录流程的隐私担忧。

hackernews · meetpateltech · 10月12日 16:48 · [社区讨论](https://news.ycombinator.com/item?id=50059115)

**「背景」** 按 Meta 官方新闻稿的说法，它已在 2026 年 9 月推出名为 Muse 的个人 AI 代理，定位为能代为执行任务的助手（tool-2-2）。第三方模型聚合页则显示，同属 Meta 的多模态推理模型 Muse Spark 1.3 已通过 OpenRouter 提供 API，定价为每百万输入 token 1.25 美元、输出 4.25 美元，上下文窗口约 100 万 token（tool-2-3）。本次讨论中的评论者还以 8 月的 Muse Spark 1.2 和 9 月的 Muse 1.3 作为对照，把 Muse Wonder 放在 Meta 这一产品线的版本序列中比较。

**「对开发者的实际影响」** 打算试用 Muse Code 的开发者需要留意：有用户在评论中报告，用 Meta 账号登录后在自己的登录授权里看到无关开发者的资料与邮箱，且无法进入账号设置停用账号；这是个人报告而非已确认的漏洞，但在核实前不宜贸然使用主账号。Meta 的账号说明指出，可以选择为 Muse 使用独立账号，这样 Muse 的交互与数据不会与其他 Meta 产品共享，希望隔离数据的人应优先采用该选项。此外，实测者称 Muse Wonder 在图像转 HTML 任务上明显弱于 Opus 5.5、更接近 Sonnet 或 Haiku 水平，因此在视觉到代码的工作流中应先用自己的用例验证，而不是只依据公布的基准分数。

**「社区讨论」** 实测方面，评论者 jjcm 用图像转 HTML 任务比较后称 Muse Wonder 明显弱于 Opus 5.5、更接近 Sonnet 或 Haiku，并对其公布的基准数字感到意外；simonw 用同一套 SVG「鹈鹕」测试把它与 8 月的 Muse Spark 1.2 和 9 月的 Muse 1.3 做了并排对比。另有评论者 pmuse 报告，通过 dev.meta.ai 的 Muse Code 站点登录自己仅用于 Quest 的 Meta 账号时，登录授权中出现了无关开发者的资料与邮箱，且无法进入账号设置注销账号；atleastoptimal 则主张前沿模型由 3–4 家公司并行开发，比一家独大更可取。这些均为评论者个人报告与观点，未获来源或独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse : The World’s First Personal AI Agent Built for Everyone</a></li>
<li><a href="https://openrouter.ai/meta/muse-spark-1.3">Muse Spark 1.3 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://muse.ai/privacy">Muse Privacy Policy</a></li>

</ul>
</details>

**标签**: `#Meta AI`, `#LLM release`, `#model benchmarking`, `#AI privacy`, `#Hacker News`

---

<a id="item-tech-news-4"></a>
### [Python 3.15 发布：PEP 810 惰性导入与采样分析器](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 8.0/10

Python 3.15 已发布，Simon Willison 的博客梳理了主要变化：新增 PEP 810 显式惰性导入（lazy import），允许模块在符号首次使用时才加载；PEP 798 让列表、集合和字典推导式支持 \* 和 \*\* 解包；标准库加入采样分析器 profiling.sampling（Tachyon），原 cProfile 更名为 profiling.tracing。Simon Willison 表示，作为需要兼容所有受支持 Python 版本的开发者，现在可以告别 3.10 并开始使用 3.11 的特性。性能方面，Miguel Grinberg 基于 3.15.0rc3 的测试发现整体与 3.14 接近，仅实验性 JIT 在 Fibonacci 测试中带来约 1.2 倍提升，这是其首次观察到有意义的 JIT 性能增幅。

rss · Simon Willison · 10月12日 18:15

**「背景」** PEP 810 的显式惰性导入解决的是一处长期存在的痛点：在此之前，命令行工具和插件作者只能靠手写延迟导入（把 import 挪进函数内部等）来避免安装重型依赖后拖慢每次调用的启动时间（tool-2-1）。同样，3.15 新增的采样分析器 profiling.sampling 之前属于 py-spy 这类标准库之外的第三方工具领域，如今被并入标准库（tool-2-2）。作者自述维护需兼容所有仍受支持 Python 版本的开源软件，这正是他在 3.10 退出支持后转向 3.11 特性的原因。

**「影响」** 对库作者而言，可以直接停止为 Python 3.10 做兼容，并开始使用 3.11 的语言特性；对插件式 CLI 工具而言，惰性导入可以把 sentence\_transformers 等重依赖的导入推迟到真正使用时，避免每次调用多出数秒启动时间。仍在 Python 3.10 上的用户若需要继续获得新版本支持，需升级到 3.11 或更高版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://peps.python.org/pep-0810/">PEP 810 – Explicit lazy imports | peps.python.org</a></li>
<li><a href="https://docs.python.org/3/whatsnew/3.15.html">What’s new in Python 3.15 — Python 3.15.0 documentation</a></li>

</ul>
</details>

**标签**: `#Python`, `#Python 3.15`, `#PEP 810`, `#lazy imports`, `#programming languages`

---

<a id="item-tech-news-5"></a>
### [learnc：调优现有 C 代码常量，JPEG 体积减 9.1%](https://www.reddit.com/r/MachineLearning/comments/1x4dlbm/learnc_fit_the_constants_in_existing_c_code_to/) ⭐️ 8.0/10

learnc 是一个 MIT 许可的工具，它针对用户用 C 编写的评分函数，调优未修改 C 代码文件中的具名常量，并把新值写回同一文件。按作者给出的留出数据结果，在 stb\_image\_write.h 的 128 个 JPEG 量化表条目上用 12 张 Kodak 图像调优、另 12 张测试，取得了等 SSIM 下 9.1% 的 BD-rate 改善，并称在 libjpeg 中用 scikit-image 独立复核；作为对照，mozjpeg 的表为 2.7%。在 Google WebRTC VAD 上，对 vad\_core.c 中所有常量用 LibriParty dev 调优后，LibriParty eval 的 F1 从 0.810 升至 0.859。作者同时说明，JPEG 在低于 1 bpp 时没有增益，且该工具适合数十到数百个常量，不适合大型权重集。

reddit · r/MachineLearning · /u/keep\_up\_sharma · 10月12日 20:51

**「背景」** JPEG 的量化表直接决定压缩率与画质的权衡，而标准 Annex K 表源自早期图像集，因此编码器常自带针对特定指标重新调优的预设表——例如 mozjpeg 就提供面向 MS-SSIM 等目标的自定义量化表。Guetzli 走得更远，用闭环优化器同时调整全局量化表与每个 DCT 块的系数。learnc 处理的是同类问题，但它把可调对象限定为现有 C 代码中已命名的常量，并由用户自己编写的 C 评分函数来驱动搜索。

**「影响」** 对需要在 C 代码里调参的开发者来说，这意味着可以只写评分函数就让工具搜索现有具名常量，而无需改写算法或移植到其他框架；但若目标是低码率 JPEG 或大规模权重集，当前结果不支持把它当作通用替代方案。由于工具会原地覆盖源文件，使用前应依赖版本控制或备份。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/imagemin/imagemin-mozjpeg">GitHub - imagemin/imagemin- mozjpeg : Imagemin plugin for mozjpeg</a></li>
<li><a href="https://arxiv.org/pdf/1703.04421">Guetzli: Perceptually Guided JPEG Encoder</a></li>

</ul>
</details>

**标签**: `#C`, `#program optimization`, `#JPEG`, `#WebRTC VAD`, `#open-source tooling`

---

<a id="item-tech-news-6"></a>
### [用 C 构建现代 Web 应用并靠 chroot/pledge 降权](https://prophitt.me/writing/a-modern-web-app-in-c) ⭐️ 7.0/10

一篇在 Hacker News 上引发讨论的博客文章介绍了如何用 C 语言构建现代 Web 应用：由 nginx 等 Web 服务器在每次请求时调用后端二进制，并用 OpenBSD pledge、chroot 等手段丢弃权限，这几点得到评论者的确认。文章同时涉及部署模型与替代 Web 架构的比较。由于本条目未附原文内容，文中没有给出具体版本号、基准数据或独立测量结果，相关说法属于作者与评论者的经验性论述。

hackernews · prophittcorey · 10月12日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50058528)

**「背景」** 这篇博文记录的是作者 Corey Prophitt 用 BCHS 技术栈交付商业网页产品 marketyour.games 的实践（tool-1-1）。该做法与 1994 年前后的 CGI 模式在根本上相同：把 C 程序放进 cgi-bin 目录，由 Apache 按请求 fork 执行；文章将自身描述为“三十多年后”仍用同一套底层技术构建商业产品（tool-1-2）。

**「影响」** 对考虑这一路线的开发者来说，请求由 Web 服务器逐次启动二进制的模式意味着进程内无法保留状态，评论者 brainless 因此更倾向使用常驻且自带状态的 Rust 加 SQLite 后端，而不是让 nginx 每次请求都调用程序；采用该架构前需要先确定状态存放与备份方案。

**「社区讨论」** 评论中 ramses0 认为文章内容“100% 属实且论证充分”，尤其认可用 pledge/chroot 丢弃权限的做法，并补充 busybox 内置 CGI 支持、rclone 可提供 WebDAV 服务；brainless 则质疑每次请求由 nginx 调用二进制的模型，偏好带状态的常驻后端，而 assimpleaspossi 回忆二十多年前用 C 加 FastCGI 构建的餐厅订餐系统长期运行良好。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://zeli.app/story/50058528">A Modern Web App in C · 153 HN comments | Zeli</a></li>
<li><a href="https://upstract.com/x/ff7e87d60c67529f">A Modern Web App in C - upstract.com</a></li>

</ul>
</details>

**标签**: `#C`, `#web applications`, `#systems programming`, `#deployment`, `#privilege separation`

---

<a id="item-tech-news-7"></a>
### [Codex CLI 被指默认安装常驻自更新后台守护进程](https://github.com/openai/codex/issues/48195) ⭐️ 7.0/10

Hacker News 上关于 OpenAI Codex CLI 的讨论指出，该命令行工具默认会安装一个常驻后台、可自我更新的守护进程，用户对此提出磁盘占用与权限方面的抱怨。发帖人称目前没有正式的关闭文档，但该功能位于一个尚未默认关闭的特性开关后，可在 ~/.codex/config.toml 中设置 \[features\] daemon\_auto\_start = false 来禁用；启动时它还会在 ~/.codex 下写入 pid、lock 等文件。另有用户报告守护进程累计占用约 12 GB 磁盘空间，并称自动更新会随机破坏文件权限，例如把 .git 变为只读从而阻塞任务。以上均为该讨论串中的用户报告，而非 OpenAI 的官方说明或独立验证结果。

hackernews · whimblepop · 10月12日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=50060694)

**「背景」** 外部报道显示，Codex CLI 从 v0.157.0（2026 年 9 月）起把守护进程的自动启动设为稳定默认行为，此前该进程只在显式调用 \`codex exec-server\` 时启动，要恢复按会话运行的旧行为需在 \`~/.codex/config.toml\` 中关闭自动启动\[tool-2-1\]\[tool-2-3\]。讨论帖中给出的开关写法是 \`\[features\]\` 下的 \`daemon\_auto\_start = false\`，与外部报道记录的 \`daemon\` 配置项命名不完全一致，说明该配置键本身也在变动\[tool-2-1\]。

**「影响」** 对通过 npm（\`npm install -g @openai/codex\`）安装 Codex CLI 的开发者而言，直接后果是安装后默认会出现一个自动更新的常驻后台进程，而发帖者称目前没有正式文档化的关闭方式，只能改 \`~/.codex/config.toml\` 里的 feature flag \`daemon\_auto\_start = false\`，或删除并锁定 \`~/.codex\` 下的 pid、lock 等文件。评论区用户还报告了具体故障：旧版本残留据称占用约 12 GB 磁盘，自动更新时还会破坏文件权限、把 \`.git\` 变成只读并使任务中断——这些均为用户个人报告，未经独立核实。

**「社区讨论」** 评论者提供了若干绕过手段：除修改配置开关外，还可以把 ~/.codex 下守护进程写入的文件删除后改用指向 /dev/null 的符号链接，并用 chattr +i 之类的方式标记为不可写；也有人认为通过 NPM 安装的 CLI 出现这类行为虽可理解，但仍然令人警惕。另有用户称自动更新会随机把 .git 变成只读，使其难以信任 Codex 完成任何任务，并转而使用极简的 bash 型框架 hax，认为这类“过度工程化”的工具带来更多麻烦。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://codex.danielvaughan.com/2026/09/25/codex-cli-daemon-auto-start-stable-default-v0157/">Daemon Auto-Start Is Now the Stable Default in Codex CLI v0 ...</a></li>
<li><a href="https://elsolitario.org/en/2026/10/12/codex-cli-daemon-auto-start-opt-in-en/">Codex CLI Daemon: Why Users Want It Opt-In - elsolitario.org</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai/ codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**标签**: `#Codex CLI`, `#background daemon`, `#AI coding agents`, `#developer tooling`, `#privacy/security`

---

<a id="item-tech-news-8"></a>
### [LineageOS 24.0 发布，代码库重基于 Android 17](https://lwn.net/Articles/1099950/) ⭐️ 7.0/10

LineageOS 项目发布了 LineageOS 24.0，把这套开源 Android 发行版的全部改动与功能重新基于 Android 17（该版本于 2026 年 6 月发布）。项目在公告中称，由于此前几个版本已经适应了 Google 的大规模重构，这次 rebase 比预期更快，发布也比往年更早。公告同时提到，2026 年 12 月 24 日 LineageOS 将迎来项目成立十周年。上述内容均来自项目官方公告，公告未说明具体机型的可用版本与支持情况。

rss · LWN.net · 10月12日 13:13

**「背景」** LineageOS 是一个面向移动设备的开源 Android 发行版，其每个大版本都会把自身积累的修改与功能重新基于当年 Android 的代码库，因此适配速度取决于上游改动的幅度。据该项目说明，Android 17 于 2026 年 6 月发布，首个版本主要包含迭代式改进和部分界面与交互调整；而 LineageOS 将在 2026 年 12 月 24 日迎来项目成立十周年。

**「影响与升级注意」** 对仍在使用官方 Linux 4.4 与 4.9 内核设备支持的用户来说，这次升级并不覆盖他们的机型：按项目的安全支持政策，这些设备继续停留在 LineageOS 22.2，无法直接获得 24.0 的改动。同时，24.0 引入了浏览器端刷机工具等新流程，说明刷写方式本身也有变化，升级前需按新版本说明确认所持机型与刷机路径。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.androidsage.com/2026/10/12/lineageos-24-released-based-on-android-17-in-browser-webusb-flashing-canvas-photo-editor-and-kernel-overhauls/">LineageOS 24 Released: Android 17 Features &amp; WebUSB</a></li>
<li><a href="https://easternherald.com/2026/10/12/lineageos-24-android-17-browser-flashing/">LineageOS 24 Adds Android 17 and Browser Flashing Tools</a></li>

</ul>
</details>

**标签**: `#LineageOS`, `#Android`, `#open source`, `#mobile OS`, `#custom ROM`

---

<a id="item-tech-news-9"></a>
### [Looped Diffusion Transformer：每个去噪步骤内循环运行共享模块](https://www.reddit.com/r/MachineLearning/comments/1x49d61/looped_diffusion_transformer_the_same_blocks_run/) ⭐️ 7.0/10

arXiv 预印本 2609.40305（9 月 30 日）提出 Looped Diffusion Transformer：不扩大文本到图像 DiT 的参数量，而是在每个去噪步骤内让同一组 Transformer 块重复运行多次，并用每轮深监督与自调制注意力解决朴素循环不稳定的问题。作者宣称，一个 260M 参数的循环模型在多个基准上击败了参数量为其 6.5 倍的模型，且推理计算量少 4.9 倍；在固定推理预算下，增加循环深度比增加去噪步数更有效。B/16 代码与权重以 MIT 许可发布，权重托管在 Hugging Face 的 sensenova 下。一位 Reddit 用户在 M5 Pro 上用 PyTorch MPS fp32、100 步 Euler、CFG 6.0 做了仅涉及五个提示词的小规模复现：模型在深度 4 训练，但 README 称其他深度无需重训即可使用；该用户发现深度 3 和 4 的生成结果非常接近，深度可在采样时选择，深度 1 每张图约 23–24 秒，深度 4 约 43–47 秒。

reddit · r/MachineLearning · /u/Fit-Ant2238 · 10月12日 18:13

**「背景」** Looped-DiT 的骨干是 MiniT2I——一个基于 MMDiT 的像素空间去噪器，作者选用它是因为其训练流程简单，能在受控条件下研究循环深度（tool-2-2）。这一架构的基本思路是在每个去噪步内部反复复用同一部分 Transformer 块，而不是增加独立参数或更多的扩散评估次数（tool-2-3）。论文提出的改进是在中间各次循环上施加深度监督，并配合自调制注意力，以稳定循环中的特征更新（tool-2-1）。

**「对开发者的实际影响」** 由于 Looped-DiT 的 PyTorch 实现、B/16 代码与权重以 MIT 许可公开（权重托管在 Hugging Face 的 sensenova 名下），开发者可以在采样阶段直接调整循环深度来按图换取算力与画质，无需重新训练或更换模型；但该独立复现表明收益主要在深度 3 之前出现、深度 3 与 4 的结果非常接近，而 M5 Pro 上单张图耗时从深度 1 的约 23–24 秒增至深度 4 的 43–47 秒，因此继续加深循环更可能只是增加计算量而非明显改善输出。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40305">[ 2609 . 40305 ] Looped Diffusion Transformer</a></li>
<li><a href="https://arxiv.org/html/2609.40305">Looped Diffusion Transformer</a></li>
<li><a href="https://www.alphaxiv.org/abs/2609.40305">Looped Diffusion Transformer | alphaXiv</a></li>
<li><a href="https://github.com/OpenSenseNova/Looped-DiT">GitHub - OpenSenseNova/Looped-DiT: PyTorch implementation of ...</a></li>

</ul>
</details>

**标签**: `#diffusion models`, `#transformer architecture`, `#efficient inference`, `#text-to-image`, `#model replication`

---

<a id="item-tech-news-10"></a>
### [Anthropic：防蒸馏措施初步减少 90% 至 99% 提取数据](https://www.anthropic.com/research/distillation-defenses) ⭐️ 7.0/10

Anthropic 10 月 12 日表示，初步证据显示其新部署的防蒸馏措施使针对 Claude 能力的模型蒸馏攻击中被提取的数据减少约 90% 至 99%。公司称已封禁数万个相关账号，部分账号在发起攻击后不到两小时即被封，并采取限制推理内容跨会话、模型和账号流转、部署双阶段分类器以及持续修补绕过手法等措施。Anthropic 称误报率低于 0.1%，但部分开发者需要更新集成，且被拦截的请求仍可能计费。这些数据为 Anthropic 单方面公布的初步结果，尚未见独立验证。

telegram · zaihuapd · 10月13日 01:25

**「背景：模型蒸馏攻击」** 模型蒸馏通常指用能力更强的模型输出作为训练数据，来训练或微调另一个模型，从而以较低成本复制部分能力。Anthropic 所指的蒸馏攻击，是外部通过 Claude API 大规模抽取模型输出，再用于训练竞争模型；这类行为依赖跨会话、跨模型或跨账号的持续调用。此次防护中的推理内容流转限制和双阶段分类器，就是为识别并阻断这种批量提取模式而设计。

**「开发者影响」** 使用 Claude API 的开发者若依赖编辑历史对话上下文，或跨会话、跨模型、跨账号传递模型的推理内容，需要按新防护措施调整集成方式。Anthropic 称误报率低于 0.1%，但被分类器拦截的请求仍可能计费，因此集成方需为少数正常请求被拦截并照常产生费用的情况做准备。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/distillation-defenses">Strengthening our defenses against distillation attacks</a></li>
<li><a href="https://www.explainx.ai/blog/anthropic-distillation-defenses-preserved-thinking-classifier-90-99-percent-2026">Anthropic Distillation Defenses: 90-99% Less Data Stolen ...</a></li>

</ul>
</details>

**标签**: `#AI security`, `#model distillation`, `#Anthropic`, `#Claude API`, `#model extraction`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [克利夫兰联储主席哈马克称可能需要维持限制性政策以压低通胀](https://www.cnbc.com/2026/10/12/beth-hammack-fed-inflation-policy.html) ⭐️ 8.0/10

克利夫兰联储主席哈马克周一表示，可能需要维持限制性货币政策，即用较高利率给经济降温，才能让通胀及时回到 2%的目标，并暗示可能进一步加息。美国 8 月个人消费支出（PCE）价格指数同比上涨 3.4%，核心 PCE 同比上涨 3.0%，均高于美联储 2%的目标。

rss · CNBC Finance · 10月13日 02:58

**「背景」** 哈马克是美联储政策制定委员会的投票成员；美联储上月进行了三年来的首次加息，9 月会议纪要显示官员们可能再次加息，但未明确时间。

**标签**: `#Federal Reserve`, `#Monetary policy`, `#Inflation`, `#Interest rates`, `#Central bank communication`

---

<a id="item-finance-news-2"></a>
### [新能源汽车出口退税率 2027 年 4 月起由 13%降至 9%](https://www.news.cn/20261012/9709731f470b42f9a84825c2e4eb914b/c.html) ⭐️ 8.0/10

财政部、税务总局 10 月 12 日发布公告，自 2027 年 4 月 1 日起将新能源汽车增值税出口退税率由 13%下调至 9%，并取消电子烟设备装置等产品的增值税出口退税；公告称对上述产品中征收消费税的产品，出口消费税政策不作调整。

telegram · zaihuapd · 10月12日 11:00

**「背景」** 出口退税是中国把出口商品在国内已缴纳的增值税退还给企业的政策工具，使产品能以更低成本进入海外市场；新能源汽车此前适用 13%的出口退税率，此次下调意味着自 2027 年 4 月 1 日起每出口一批车可退回的税款相应减少。

**「影响」** 退税减少 4 个百分点将直接抬高新能源汽车出口企业的成本，而 2026 年 7 月中国新能源汽车出口达 55.3 万辆、同比增长约 1.5 倍，并连续两个月占汽车出口总量一半以上，比亚迪、特斯拉中国等出口占比较高的车企受影响更明显。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.reuters.com/world/china-lower-vat-export-rebate-new-energy-vehicles-2026-10-12/">China to lower VAT export rebate on new energy vehicles</a></li>
<li><a href="https://cnevpost.com/2026/08/13/automakers-share-china-nev-exports-jul-2026/">Automakers &#x27; share of China NEV exports in July: BYD... - CnEVPost</a></li>
<li><a href="https://chinaevhome.com/2026/08/12/chinas-new-energy-vehicle-sales-share-tops-60-for-first-time-in-july/">China &#x27;s New Energy Vehicle Sales Share Tops 60... | ChinaEVHome</a></li>

</ul>
</details>

**标签**: `#China NEV exports`, `#export tax rebates`, `#fiscal policy`, `#automotive industry`, `#e-cigarettes`

---

<a id="item-finance-news-3"></a>
### [中国商务部：中欧就混动与电动汽车贸易达成多项共识](https://www.mofcom.gov.cn/xwfb/sjfzrfb/art/2026/art_4d502e1d49fd4480b39a6cfd0d752038.html) ⭐️ 7.0/10

中国商务部表示，中欧在贸易投资磋商机制下就混动汽车和电动汽车贸易达成多项共识。混动汽车安排将以 2025 年为基准向上调整，中方配额不低于欧方其他进口来源地，并保留世贸组织争端解决等权利；电动汽车方面，欧方将继续推进企业价格承诺及其他复审程序。

telegram · zaihuapd · 10月12日 06:19

**「背景」** 2026 年 1 月，欧盟与中国以“价格承诺”机制（出口商承诺遵守最低进口价格）取代了此前欧盟对中国电动汽车加征的反补贴关税，此次中欧在磋商机制下就混动和电动汽车达成的共识属于该框架下的后续进展。

**「影响」** 若相关安排执行，向欧盟出口混动汽车的中国企业将获得不低于其他进口来源地的配额待遇；具体配额数字尚未公布。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://informedclearly.com/en/trade-war/57721/eu-china-ev-price-floor-trade-2026">EU-China EV Price Floor: Redrawing Global Trade Rules in 2026</a></li>
<li><a href="https://informedclearly.com/en/trade-war/62505/eu-china-ev-price-floor-trade-deal-2026">EU-China EV Price Floor: 2026 Global Trade Truce Explained</a></li>

</ul>
</details>

**标签**: `#China-EU trade`, `#electric vehicles`, `#hybrid vehicles`, `#trade policy`, `#auto industry`

---

<a id="item-finance-news-4"></a>
### [税务处罚新裁量基准 11 月施行，社保欠缴最高罚 3 倍](https://fgk.chinatax.gov.cn/zcfgk/c100012/c5252754/content.html) ⭐️ 7.0/10

国家税务总局发布《全国税务行政处罚裁量基准（2026 年版）》，自 2026 年 11 月 1 日起施行，将用人单位逾期不缴或少缴社保费纳入处罚事项，按欠缴金额和占比分档，最高罚欠缴金额的 3 倍。公告称处罚前提是经责令限期缴纳后逾期仍不缴纳，且需补缴欠费并按日加收万分之五滞纳金；该基准不能单独作为处罚依据，施行前发生的违法行为原则上适用当时规定。

telegram · zaihuapd · 10月13日 02:45

**「背景」** 税务行政处罚裁量基准是税务机关统一各地处罚尺度的内部规则，本身不能单独作为处罚依据：对社保欠缴罚款，仍需以社会保险费等上位法规定为前提，并先经责令限期缴纳、逾期仍不缴纳这一环节。公告还明确，2026 年 11 月 1 日施行前发生的违法行为原则上适用当时的规定。

**标签**: `#税务处罚`, `#社保欠缴`, `#裁量基准`, `#企业合规`, `#中国政策`

---