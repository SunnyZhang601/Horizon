---
layout: default
title: "Horizon Summary: 2026-10-13 (ZH)"
date: 2026-10-13
lang: zh
---

> 从 54 条内容中筛选出 16 条重要资讯。

---

**科技新闻**
1. [Python 3.15 发布：显式惰性导入与 Tachyon 采样分析器](#item-tech-news-1) ⭐️ 9.0/10
2. [黑客远程触发欧洲超市冷柜除霜，Danfoss 旧控制器受关注](#item-tech-news-2) ⭐️ 8.0/10
3. [开源项目把 WiFi 7 路由器改造成 320 Msps SDR 接收机](#item-tech-news-3) ⭐️ 8.0/10
4. [用 C 构建现代 Web 应用的技术实践与讨论](#item-tech-news-4) ⭐️ 7.0/10
5. [OpenAI Codex CLI 默认安装持久自更新后台守护进程](#item-tech-news-5) ⭐️ 7.0/10
6. [Show HN：PS2 游戏静态重编译为 WebAssembly](#item-tech-news-6) ⭐️ 7.0/10
7. [LineageOS 24.0 发布，基于 Android 17 重构](#item-tech-news-7) ⭐️ 7.0/10
8. [learnc：自动调优 C 代码常量，JPEG 与 WebRTC VAD 指标提升](#item-tech-news-8) ⭐️ 7.0/10
9. [Intel Crescent Island 定名 D270：最高 480GB LPDDR5X，1.3 PFLOPS FP8](#item-tech-news-9) ⭐️ 7.0/10
10. [Qwen 发布 QwenGyre：超长智能体训练的弹性 RL 框架](#item-tech-news-10) ⭐️ 7.0/10
11. [OpenBMB 发布 MiniCPM-V 4.7 35B-A3B 端侧 MoE 多模态模型](#item-tech-news-11) ⭐️ 7.0/10
12. [Decision 3.0 开源多模态决策模型 0.6B 至 27B 发布](#item-tech-news-12) ⭐️ 7.0/10
13. [Meta 发布 Muse Wonder 模型，订阅价 20 美元起](#item-tech-news-13) ⭐️ 7.0/10

**财经新闻**
1. [美联储官员哈马克：或需进一步加息，以防通胀心理固化](#item-finance-news-1) ⭐️ 7.0/10
2. [重建后皇岗口岸开通 实施“一地两检”新通关模式](#item-finance-news-2) ⭐️ 7.0/10
3. [中国将新能源汽车出口退税率由 13%下调至 9%](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Python 3.15 发布：显式惰性导入与 Tachyon 采样分析器](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 9.0/10

Python 3.15 已发布，官方 What&\#x27;s New 指南由 3.14/3.15 发布经理 Hugo van Kemenade 整理，最受关注的新特性是 PEP 810 显式惰性导入，允许用 \`lazy import json\` 和 \`lazy from pathlib import Path\` 将模块导入推迟到首次使用符号时。该版本还引入 PEP 798 推导式解包语法，并把原有 tracing profiler 从 \`cProfile\` 更名为 \`profiling.tracing\`，同时新增名为 Tachyon 的采样分析器 \`profiling.sampling\`。性能方面，Miguel Grinberg 针对 3.15.0rc3 的测试发现整体与 3.14 大致相当，仅实验性 JIT 在 Fibonacci 测试中比标准 3.15 解释器快约 1.2 倍；以上为 Simon Willison 博文覆盖的内容，摘要未展示完整的变更清单。

rss · Simon Willison · 10月12日 18:15

**「背景」** Python 默认在遇到 import 语句时立即加载模块并执行其顶层代码；PEP 810 引入的显式 lazy import 将实际导入推迟到首次使用该符号时，以解决重型依赖带来的启动开销。新的推导式解包语法（PEP 798）是对 2015 年 Python 3.5 中 PEP 448 解包泛化的扩展。

**「影响」** 对插件生态和工具作者而言，PEP 810 的 \`lazy import\` 可直接消除因安装使用 \`sentence\_transformers\` 等重依赖插件而给每次 \`llm\` 命令增加数秒启动延迟的问题——Simon 的 LLM 工具此前只能在插件文档中建议手动惰性导入。同时，\`profiling.sampling\` 将采样分析能力带入标准库，已有 Python 3.15 进程可用 \`python -m profiling.sampling attach &lt;PID&gt;\` 采集样本，减少对 py-spy 等外部工具的依赖。

**标签**: `#Python`, `#Python 3.15`, `#PEP 810`, `#lazy imports`, `#open source releases`

---

<a id="item-tech-news-2"></a>
### [黑客远程触发欧洲超市冷柜除霜，Danfoss 旧控制器受关注](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

据报道，攻击者入侵了欧洲多国超市的联网制冷控制器，远程开启自动除霜，导致冷柜无法正常制冷。法国 Intermarché 等连锁超市受影响，报道称约 150 家门店被针对，商品配送和门店定价也受到干扰。Claroty Team82 曾披露 Danfoss 制冷控制器存在漏洞，而社区讨论提到涉事设备可能包括已终止支持的旧型号 SM800（2021 年 EOS）和 SC355（2016 年 EOS）。

hackernews · Zeekaas · 10月12日 12:16 · [社区讨论](https://news.ycombinator.com/item?id=50055304)

**「背景：Danfoss 控制器漏洞与补丁」** 此类事件的直接背景是 Danfoss 制冷控制器此前的安全研究：Claroty 的 Team82 于 2026 年 8 月发布研究，指出 Danfoss AK-SM 800A 制冷控制器平台的嵌入式 Web 管理界面存在多个漏洞，成功利用后可改变 Web 服务器处理请求的方式，并可能操纵与该设备交互的客户端，Danfoss 随后已在新固件版本中修复。据 Cybernews 报道，针对三款 Danfoss 控制器的补丁自 9 月 18 日起已可获取。

**「影响」** 对受影响的超市运营方而言，最直接的行动是排查并隔离制冷控制器的远程访问，限制其与互联网的连通；社区讨论提到，若涉及的是已终止支持的 Danfoss SM800（2021 年 EOS）或 SC355（2016 年 EOS），厂商补丁可能不可得，只能更换设备或加装网络分段等补偿性控制。

**「社区讨论」** 评论者围绕冷柜为何联网展开争论：renyicircle 引用 Danfoss 的宣传称远程诊断和跨门店能效对比可节省成本，alexpotato 则指出医院实验室的新设备也因订阅制而必须联网，9x39 认为旧控制器长期暴露是因为运营方缺乏安全审查和更换预算。bronco21016 还猜测此次攻击可能与 2026 年 8 月美军基地的类似事件是同一组织、受其启发或完全无关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claroty.com/team82/research/freeze-the-controller-defrost-the-food-uncovering-vulnerabilities-in-danfoss-refrigeration-controllers">Freeze the Controller, Defrost the Food: Uncovering ...</a></li>
<li><a href="https://cybernews.com/security/danfoss-refrigeration-hack-france-supermarkets/">Refrigeration Cyberattack Hits French Supermarkets | Cybernews</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#OT/ICS security`, `#IoT`, `#legacy systems`, `#refrigeration controllers`

---

<a id="item-tech-news-3"></a>
### [开源项目把 WiFi 7 路由器改造成 320 Msps SDR 接收机](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

GitHub 上出现了一个名为 w1700k-sdr 的开源项目，声称能把一台 WiFi 7 路由器改造成采样率 320 Msps 的软件定义无线电（SDR）接收机。该仓库由开发者 h0m3us3r 发布，经 Hacker News 提交后在硬件与 SDR 社区获得较高关注。需要说明的是，除项目仓库链接和社区讨论外，本次没有提供实现细节或独立测量数据，因此 320 Msps 属于项目方的宣称指标，尚未被第三方验证。评论者还提到该方案工作在约 5 GHz 频段。

hackernews · djfergus · 10月12日 12:41 · [社区讨论](https://news.ycombinator.com/item?id=50055593)

**「背景」** 软件定义无线电（SDR）把传统上由专用电路完成的滤波、解调等环节交给软件和主机 CPU，射频前端只负责把信号采样成数字流；因此采样率（Msps）直接决定单通道能同时覆盖的瞬时带宽，是衡量低成本 SDR 硬件能力的关键指标。该项目的开发者此前已用 ESP32 Wi‑Fi 微控制器实现过同类接收方案（eSpDR），这次是把同样的思路搬到 Wi‑Fi 7 路由器上，以开源仓库形式发布。

**「影响与兼容性」** 评论者 thebeardisred 指出，同款芯片组也用于 Banana Pi R4，而该板卡自带 PCIe 接口可接 NVMe，因此认为同一套方案很可能能在该硬件上复现；这属于基于芯片组相同做出的推断，并非已验证的结果。对想低成本获得高采样率接收能力的开发者而言，实际动手前需要先确认所用路由器或板卡的芯片组、射频前端与固件是否与项目匹配。

**「社区讨论」** yonatan8070 提到同一位开发者此前还用 ESP32 微控制器做过 SDR（eSpDR），并希望更多常见 WiFi 网卡能被这样利用，让普通笔记本以低成本充当 SDR；aftbit 则称自己不知道还有更便宜的 5 GHz、320 Msps 接收方案。mikewarot 从维修旧式服务监视器的经验出发，认为借助桌面 CNC、廉价 PCB 和常见元器件可以搭建类似设备；alightsoul 则提出问题，询问手机 FM 收音机需要签约授权是否与这些无线电越来越多地由软件定义有关。

**标签**: `#software-defined radio`, `#WiFi 7`, `#hardware hacking`, `#open source`, `#embedded systems`

---

<a id="item-tech-news-4"></a>
### [用 C 构建现代 Web 应用的技术实践与讨论](https://prophitt.me/writing/a-modern-web-app-in-c) ⭐️ 7.0/10

一篇技术文章介绍了如何用 C 语言构建现代 Web 应用，重点覆盖部署方式和安全实践。文章在 Hacker News 上引发讨论，话题集中在 CGI、FastCGI 以及用 chroot/pledge 等手段降低进程权限。由于原文内容不可用，文章中的具体实现、版本或性能数据无法核实。

hackernews · prophittcorey · 10月12日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50058528)

**「背景」** CGI 是让 Web 服务器通过 fork/exec 调用独立程序处理请求的旧接口（CGI/1.1 由 2004 年的 RFC 3875 定义），FastCGI 则避免了每个请求都新建进程的开销；用 C 写 Web 应用常落在 BCHS（BSD、C、httpd、SQLite）这类技术栈上，kcgi 就是其中最小化、可审计的 CGI/FastCGI 库。安全方面，OpenBSD 的 httpd 采用特权分离并运行在 chroot 内，各组件只 pledge 自身所需的系统调用，从而把可操作范围压缩到 chroot 内的文件访问、日志和网络通信。

**「影响」** 对考虑采用 C 或类似单二进制方案提供 Web 服务的开发者，讨论提醒需自行验证 CGI/FastCGI 下的并发编程与 .bss/.data 初始化问题，并确认 chroot/pledge 等权限隔离措施在目标平台上可用。

**「社区讨论」** 评论者补充了 BusyBox 内置 cgi-bin 支持，并有人分享早年用 C + FastCGI 运行餐厅点单系统的经历。也有评论者认为 Go 用 CGO\_ENABLED=0 可生成不依赖 libc 的单二进制并自带 HTTP/TLS 库，但坦言不喜欢在 C 中做并发编程。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://braindetox.kr/en/posts/modern_web_app_in_c_bchs_cgi_2026.html">Decisions Behind a Commercial Web App Built in C and CGI ...</a></li>
<li><a href="https://news.ycombinator.com/item?id=19549085">Secure CGI Applications in C on OpenBSD | Hacker News</a></li>
<li><a href="https://github.com/kristapsdz/kcgi">GitHub - kristapsdz/kcgi: minimal CGI and FastCGI library for ... AsiaBSDCon 2016: Secure CGI Applications in C Privilege Separation and Pledge - OpenBSD kcgi: securing CGI web applications - kristaps.bsd.lv Bob Beck beck@openbsd Pledge,</a></li>

</ul>
</details>

**标签**: `#C`, `#web development`, `#systems programming`, `#CGI/FastCGI`, `#security`

---

<a id="item-tech-news-5"></a>
### [OpenAI Codex CLI 默认安装持久自更新后台守护进程](https://github.com/openai/codex/issues/48195) ⭐️ 7.0/10

提交到 Hacker News 的一条 GitHub issue 称，OpenAI Codex CLI 默认会安装一个持久运行、可自我更新的后台守护进程，发帖人 whimblepop 表示目前没有文档化的关闭方式，但该功能位于一个 feature flag 之后，可在 ~/.codex/config.toml 中写入 \[features\] 并设置 daemon\_auto\_start = false 来关闭。评论者还报告了具体影响：旧版本不断堆积使磁盘占用达到约 12GB（icantevenhold 的实测说法），自动更新时可能随机破坏权限、令 .git 变成只读并因此中断任务（dllu 的报告）。这些均为用户个人报告，目前没有 OpenAI 的公开回应或官方文档确认，也没有独立验证。

hackernews · whimblepop · 10月12日 18:29 · [社区讨论](https://news.ycombinator.com/item?id=50060694)

**「背景」** Codex CLI 是 OpenAI 提供的本地编码 agent，可通过 npm 等包管理器全局安装（tool-2-2）。据第三方 Codex CLI 指南描述，其后台 app-server daemon 此前已具备可配置的更新计划、\`codex app-server daemon update\` 命令，以及 daemon 重启后的线程恢复能力（tool-2-1）。本次争议的焦点在于该 daemon 现在随 CLI 默认安装并自行启动与更新，而社区反映缺乏文档化的关闭方式。

**「影响」** 对使用 Codex CLI 的开发者而言，需要在配置文件中手动设置 daemon\_auto\_start = false 才能阻止守护进程自启，这属于未文档化的变通手段；发帖人还建议删除 ~/.codex 下的 pid、lock 等启动文件并替换为指向 /dev/null 的符号链接，再用 chattr +i 标记为不可写。若磁盘占用与权限被改写的报告属实，在磁盘空间有限或与版本控制仓库共存的开发环境中，用户应检查 ~/.codex 的体积并在需要时限制其写入权限。

**「社区讨论」** 评论者普遍质疑守护进程的必要性：icantevenhold 称其在系统上占用约 12GB 并认为 Codex 在资源使用上比 Claude Code 更差，dllu 则表示守护进程的 bug 会让目标每隔几小时被阻塞，已难以信任其执行任务。reacharavindh 则给出相反取向的体验，称改用只依赖 bash 的极简 harness hax 后感觉更轻松；这些均为个人观点与经验，不构成共识或对问题的独立确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blakecrosley.com/guides/codex">Codex CLI Guide 2026: Setup, Sandbox, AGENTS.md &amp; MCP</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**标签**: `#OpenAI Codex`, `#AI coding tools`, `#background daemon`, `#developer tooling`, `#resource usage`

---

<a id="item-tech-news-6"></a>
### [Show HN：PS2 游戏静态重编译为 WebAssembly](https://github.com/snuri00/ps2-web-recomp) ⭐️ 7.0/10

Show HN 项目 ps2-web-recomp 将 PlayStation 2 游戏静态重编译为 WebAssembly，并由 Hacker News 用户 deadxwarrior 提交。该帖获得 263 分和 141 条评论，讨论集中在重编译项目的信任与审核、相关平台移植经验，以及把重编译器本身搬到浏览器中的可能性。现有信息没有给出已支持游戏列表、性能数据或独立验证结果，因此这仍是项目展示，而非已证实的通用 PS2 运行方案。

hackernews · deadxwarrior · 10月12日 06:46 · [社区讨论](https://news.ycombinator.com/item?id=50052251)

**「背景」** 静态重编译不走传统模拟器在运行时逐条解释执行的路线，而是把主机游戏的原始机器码提前翻译并编译成目标平台的原生代码，从而让旧主机软件直接跑在现代硬件上。同一作者的早期项目 psp-web-recomp 已用这一思路处理 PSP：把游戏的 MIPS 机器码提前翻译成 C++、编译为 WebAssembly，并链接一个用 WebGL 2 绘制画面的 PSP 操作系统与图形芯片的小型重实现；本次项目把同样的方式搬到了 PS2 上。

**「影响」** 对打算运行或分发此类 WASM 构建的用户，评论中提出的实际风险是安全审查：aceazzameen 认为 decomp/recomp 项目在信任和审核方面尚不及模拟器社区，用户需要自行评估可执行产物的来源。

**「社区讨论」** 评论中最实质的分歧是安全与审查：aceazzameen 担心新出现的 decomp/recomp 原生构建缺乏模拟器社区那样的信任和审核，并质疑是否可能有隐藏恶意软件；kodablah 则分享了自己为 PS Vita 做的类似项目，称其使用 WASM 中的 ARM-to-WASM 转译器，已测试少数游戏，早期版本在旗舰 Android 手机的 Chrome 移动端运行良好。另有评论建议把编译器本身编译成 WebAssembly，以便托管在任何地方并在浏览器中直接转换项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/snuri00/psp-web-recomp">GitHub - snuri00/psp-web-recomp: PSP games in the browser without...</a></li>
<li><a href="https://www.youtube.com/watch?v=ywWwUuWRgsM">Recompilation : An Incredible New Way to Keep N64 Games Alive</a></li>
<li><a href="https://www.generationamiga.com/2026/08/21/masters-of-teras-kasi-recompilation-targets-windows-macos-and-linux/">Masters of Teras Kasi recompilation targets Windows, macOS and...</a></li>

</ul>
</details>

**标签**: `#WebAssembly`, `#static recompilation`, `#PS2 emulation`, `#binary translation`, `#open source`

---

<a id="item-tech-news-7"></a>
### [LineageOS 24.0 发布，基于 Android 17 重构](https://lwn.net/Articles/1099950/) ⭐️ 7.0/10

LineageOS 项目发布了 LineageOS 24.0，将这个基于 Android 的开源移动发行版重新基于 Android 17 的代码库。项目在公告中称，自 Android 17 于今年 6 月发布以来，团队一直在重新移植此前的修改与功能；得益于过去几个版本对 Google 大规模重构的适配，本次 rebase 比预期更快完成。公告还提到，2026 年 12 月 24 日 LineageOS 将迎来项目十周年。

rss · LWN.net · 10月12日 13:13

**「背景」** LineageOS 是社区维护的 Android 开源发行版，2016 年 12 月从 CyanogenMod 分叉而来，这正是公告中提到的 2026 年 12 月 24 日十周年所对应的起点。上一个版本 LineageOS 23.2（见其 Changelog 31）同样以跟进新的 AOSP 版本、重做自身改动为核心工作，此次 24.0 延续这一模式，rebase 到 2026 年 6 月发布的 Android 17 代码库上。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LineageOS">LineageOS - Wikipedia</a></li>
<li><a href="https://www.lineageos.org/Changelog-31/">Changelog 31 - Masterful Material, Expressive Emotions, Awesome...</a></li>

</ul>
</details>

**标签**: `#LineageOS`, `#Android`, `#open source`, `#mobile OS`, `#custom ROM`

---

<a id="item-tech-news-8"></a>
### [learnc：自动调优 C 代码常量，JPEG 与 WebRTC VAD 指标提升](https://www.reddit.com/r/MachineLearning/comments/1x4dlbm/learnc_fit_the_constants_in_existing_c_code_to/) ⭐️ 7.0/10

Reddit 用户发布了一个名为 learnc 的工具，它针对用户用 C 语言编写的评分函数，自动调整未修改 C 代码中的命名常量，并将新值写回同一文件。据发帖人自述，在 stb\_image\_write.h 的 128 个 JPEG 量化表条目上，用 12 张 Kodak 图像调优、另外 12 张测试，在相同 SSIM 下取得 9.1% BD-rate 改善，并用 scikit-image 在 libjpeg 中独立验证；作为对比，mozjpeg 的量化表为 2.7%。在 Google WebRTC VAD 上，调优 vad\_core.c 的全部常量后，LibriParty 评估集上的 F1 从 0.810 升至 0.859。作者指出的限制包括：低于 1 bpp 时 JPEG 没有增益，工具最适合数十到数百个常量而非大型权重集，代码以 MIT 许可证发布。发帖标题称“9.1% smaller JPEGs”，但文中报告的是同等 SSIM 下的 BD-rate 改善，并非直接的文件体积缩小。

reddit · r/MachineLearning · /u/keep\_up\_sharma · 10月12日 20:51

**「背景」** learnc 处理的对象是 C 源码中以命名常量形式存在的可调参数：用户自己写一个 C 评分函数，工具在不改动代码结构的前提下搜索这些常量的取值并写回同一个文件。它的 JPEG 实验针对 stb\_image\_write.h 中的 128 个量化表项，用 BD-rate 衡量同等 SSIM 质量下的码率变化，并以 mozjpeg 手工调优的量化表作为对照——后者在同一测试中为 2.7%。WebRTC VAD 是 Google 的语音活动检测器，这次实验将其 vad\_core.c 中的全部常量一并纳入调参，而不是像通常那样只调整少数几个。

**「影响」** 对于需要在 C 代码中调整少量常量的开发者，learnc 提供了一条无需改动代码结构、只需编写评分函数的自动调优路径；但由于它会将新值直接写回同一文件，使用前应保留原文件或纳入版本控制。作者也说明其适用范围为数十到数百个常量，因此参数规模更大的权重集并不适合直接用此工具处理。

**标签**: `#C`, `#optimization`, `#JPEG compression`, `#WebRTC VAD`, `#autotuning`

---

<a id="item-tech-news-9"></a>
### [Intel Crescent Island 定名 D270：最高 480GB LPDDR5X，1.3 PFLOPS FP8](https://www.reddit.com/r/LocalLLaMA/comments/1x4g90u/intel_crescent_island_gpu_gets_dseries_name/) ⭐️ 7.0/10

Reddit 上汇总的信息显示，英特尔此前代号 Crescent Island 的 AI GPU 被归入新的 D 系列，型号为 D270：它采用 Xe3P 架构、32 个 Xe 核心和 256 个 XMX 引擎，频率约 2.5GHz，标称 FP8 峰值矩阵吞吐 1.3 PFLOPS、FP64 峰值向量吞吐 10.2 TFLOPS，支持 FP4 至 FP64 多种格式，接口为 PCIe Gen5 x16，TDP 350W，形态为风冷 PCIe CEM 板卡。内存方面，英特尔自有配置最高 160GB LPDDR5X，ODM 配置最高可达 480GB，带宽 1.5TB/s（约 9375Mbps × 1280-bit），支持 ECC，统一 L2 缓存 32MB。这些规格来自社区帖子的整理而非英特尔官方发布，帖子也没有给出价格、上市时间、软件生态支持或第三方基准测试结果。

reddit · r/LocalLLaMA · /u/Monad\_Maya · 10月12日 22:42

**「背景」** Crescent Island 是 Intel 面向 AI 推理的数据中心 GPU，Intel 曾在 2026 年 8 月下旬的 Hot Chips 2026 上公布完整规格：32 个 Xe3P 核心、256 个 XMX 引擎、350W 风冷 TDP（tool-2-2）。与主流 AI 加速器采用 HBM 的路线不同，该芯片选用 LPDDR5X，优先追求大容量与能效而非峰值带宽，容量最高可达 480GB（tool-2-1、tool-2-3）。

**「影响」** 对关注本地大模型推理的用户来说，ODM 配置最高 480GB LPDDR5X、1.5TB/s 带宽和 ECC 支持是容量与可靠性上的关键卖点，但英特尔自有配置只到 160GB，价格、上市时间和软件栈支持均未公布，现阶段无法据此做采购或部署规划；350W TDP、风冷 PCIe CEM 与 PCIe Gen5 x16 的规格也意味着需要匹配的机箱、供电和主板插槽。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wccftech.com/intel-crescent-island-gpus-32-xe3p-cores-for-agentic-ai-low-cost-lpddr5x-up-to-480-gb/">Intel Crescent Island GPUs Pack Up To 32 Xe3P Cores, Optimized...</a></li>
<li><a href="https://www.spheron.network/blog/intel-crescent-island-vs-nvidia-gpus-new-inference-chip-expl/">Intel Crescent Island GPU Specs vs NVIDIA... | Spheron Blog</a></li>
<li><a href="https://www.youtube.com/watch?v=KBjgag0QITQ">Intel ’s New GPU Has Nearly Half a Terabyte! - YouTube</a></li>

</ul>
</details>

**标签**: `#Intel`, `#AI accelerators`, `#local LLM inference`, `#GPU hardware`, `#LPDDR5X memory`

---

<a id="item-tech-news-10"></a>
### [Qwen 发布 QwenGyre：超长智能体训练的弹性 RL 框架](https://www.reddit.com/r/LocalLLaMA/comments/1x41myz/qwen_released_qwengyre_rl_framework_for_training/) ⭐️ 7.0/10

Qwen 在 Reddit 宣布推出 QwenGyre，一个面向极长视野（XLong）智能体训练的弹性强化学习框架。该框架包含 Elastic Scheduler 与 Trajectory Processor：前者在 rollout 与训练之间动态重分配 GPU 且不中断正在执行的任务，后者把压缩、子智能体和重试产生的分支执行转为前缀共享的轨迹树，并对超时后的部分进展计分。帖子称，在 Qwen3.8-2.4T-A95B 上、每次 rollout 约 70 万 token 的规模下，QwenGyre 用 48 步将 NL2RepoBench 从 52.5% 提升到 58.5%，端到端训练时间比 Async 减少约 44%，相对 Colocate 和 Async 分别最高加速 1.85 倍和 1.78 倍。上述性能数字来自发布帖的宣称，尚无论文或独立验证可确认，且帖子引用的 arXiv 编号和模型名等细节也需谨慎对待。

reddit · r/LocalLLaMA · /u/ResearchCrafty1804 · 10月12日 13:18

**「背景」** 智能体强化学习通常先让模型在环境中执行长轨迹（rollout），再用这些轨迹更新策略；当单次任务要跑数小时、单次 rollout 接近 100 万 token 时，rollout 与训练阶段对 GPU 的需求会随时长剧烈波动。此前的常见做法是把 GPU 静态按固定比例分配给 rollout 与训练（Colocate），或让两者完全异步（Async），这两种调度方式并非为极长时程场景设计。据论文页面介绍，QwenGyre 的思路是把 harness 执行、GPU 角色和训练样本的生命周期彼此分离。

**「影响」** 对训练长时程智能体的团队而言，QwenGyre 的弹性调度把 rollout 与训练的 GPU 分配解耦，可在不中断在线执行的情况下减少 GPU 空转，其轨迹处理器还通过前缀共享、部分进度计分和去重来限制训练样本量——这在单次 rollout 达约 70 万 token 时直接影响算力成本。不过，目前可核实的是论文层面的机制与基准（NL2RepoBench 从 52.5% 提升到 58.5%，端到端训练时间较 Async 减少约 44%），来源未说明代码或权重是否开放、支持哪些硬件，落地前需先确认可复现性与集成条件。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.33848">[2609.33848] QwenGyre: An Elastic Reinforcement Learning ...</a></li>
<li><a href="https://arxiv.org/html/2609.33848v1">QwenGyre: An Elastic Reinforcement Learning Framework ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/12/alibaba-qwen-introduces-qwengyre-elastic-reinforcement-learning-rl-for-xlong-horizon-agents/">Alibaba Qwen Introduces QwenGyre: Elastic Reinforcement ...</a></li>
<li><a href="https://huggingface.co/papers/2609.33848">Paper page - QwenGyre : An Elastic Reinforcement Learning...</a></li>
<li><a href="https://arxiv.org/abs/2609.33848">[2609.33848] QwenGyre : An Elastic Reinforcement Learning...</a></li>
<li><a href="https://cctest.ai/en/articles/qwengyre-targets-gpu-idling-and-trajectory-redundancy-in-long-horizon-agent-rl">QwenGyre Improves Reinforcement Learning for Long - Horizon Agents</a></li>

</ul>
</details>

**标签**: `#reinforcement learning`, `#AI agents`, `#long-horizon tasks`, `#distributed training`, `#Qwen`

---

<a id="item-tech-news-11"></a>
### [OpenBMB 发布 MiniCPM-V 4.7 35B-A3B 端侧 MoE 多模态模型](https://www.reddit.com/r/LocalLLaMA/comments/1x47taj/openbmbminicpmv4735ba3b/) ⭐️ 7.0/10

OpenBMB 发布 MiniCPM-V 4.7 的 35B-A3B 变体，这是 MiniCPM-V 系列首个 MoE 模型，延续单图、多图与视频理解能力，并已在 Hugging Face 提供 GGUF 量化版本。官方宣称，配合新提出的 Lookahead Expert Scheduling（LES）、细粒度分层量化与 DSpark 投机采样，该模型成为首个能在端侧流畅运行且不损失性能的开源 MoE 模型，在 iPhone 17 Pro Max 上解码速度达 13+ tokens/s，但这些均为厂商说法，源内容未附独立基准验证。模型支持 iOS、Android、HarmonyOS，并宣称对 Rockchip、Houmo、Intel、AMD、Arm 芯片平台提供 day-0 支持，同时兼容 SGLang、vLLM、llama.cpp、Ollama 等推理框架和 SWIFT、LLaMA-Factory 微调框架，提供 GGUF、BNB、AWQ、GPTQ 量化变体并新增 FP8 量化支持。官方还称 Instruct 模式下 35B-A3B 的整体得分高于 Qwen3.6 35B-A3B 且推理时间更短。

reddit · r/LocalLLaMA · /u/Skyline34rGt · 10月12日 17:16

**「背景」** MiniCPM-V 是面壁智能与清华大学 NLP 实验室开源的多模态模型系列，从早期版本起就以在手机等端侧设备上高效运行为设计目标（tool-2-1）。其底座 MiniCPM-2B 仅有约 24 亿非词嵌入参数、总计约 2.7B 参数，MiniCPM-V 即在此基础上构建，强调同规模模型中的性能与效率平衡，并陆续扩展到图像、视频理解与端侧部署（tool-2-2）。这也解释了为何该系列新推出的 35B 级 MoE 变体会把“端侧推理速度”作为主要卖点之一。

**「对开发者的影响」** 完整 BF16 权重约 70.4 GB、分 16 个分片（tool-3-1），因此本地部署实际上要依赖官方提供的 GGUF、AWQ、GPTQ、BNB 或 FP8 量化版本；同时模型已给出 llama.cpp、Ollama、vLLM、SGLang 的推理支持，现有本地栈可直接接入而无需自建运行时。OpenBMB 宣称的 iPhone 17 Pro Max 上 13+ tokens/s 解码速度和“无损”端侧推理目前只有厂商说法、没有独立基准，开发者在选型时应以自己的目标硬件实测为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/OpenBMB/MiniCPM-V">GitHub - OpenBMB/MiniCPM-V: A Pocket-Sized MLLM for Ultra ...</a></li>
<li><a href="https://github.com/OpenBMB/MiniCPM">GitHub - OpenBMB/MiniCPM: MiniCPM5: SOTA on-device LLMs ... openbmb/MiniCPM-V · Hugging Face MiniCPM-V 4.7: A 35B MoE Vision Model That Runs on an iPhone Inference and Deployment | OpenBMB/MiniCPM | DeepWiki MiniCPM-V Series | OpenBMB/MiniCPM-o | DeepWiki MiniCPM-V: A GPT-4V Level MLLM on Your Phone - arXiv.org</a></li>
<li><a href="https://www.orcarouter.ai/blog/minicpm-v-4-7-vs-ui-venus-2-9b">MiniCPM - V 4 . 7 vs UI-Venus 2.9B Compared</a></li>

</ul>
</details>

**标签**: `#on-device AI`, `#MoE`, `#multimodal LLM`, `#quantization`, `#open-source models`

---

<a id="item-tech-news-12"></a>
### [Decision 3.0 开源多模态决策模型 0.6B 至 27B 发布](https://www.reddit.com/r/LocalLLaMA/comments/1x3th4p/decision_30_open_multimodal_decision_models_from/) ⭐️ 7.0/10

vLLM Semantic Router 团队发布了 Decision 3.0（d3）开源多模态决策模型系列，覆盖 0.6B 到 27B，采用 Apache-2.0 许可，可读文本、图像和视频，权重集合发布在 Hugging Face 的 vllm-sr/decision-30 下。该系列基于 Qwen3.5（0.8B/2B/4B/9B）和 Qwen3.8-27B 构建，参数计数包含视觉编码器（4B 中为 0.33B，27B 中为 0.46B）；支持 choice、yes/no、score 三种决策类型，对每个答案给出概率而不生成文本，同一输入的多个问题可在一次调用中各自前向计算；图像每请求可多张、最高 1.6 MP，视频支持 MP4/WebM/MOV/MKV，按 2 fps 采样、整段最多 32 帧、每帧最高 0.2 MP；权重为 BF16，可用 Transformers 配合 trust\_remote\_code=True 加载，并在 AMD Instinct MI325X 上训练。发布方称，使用官方 Jev 0.3 套件在已发布权重上自测，27B 在文本和视觉两个榜单上分别得 64.7 和 71.6，排名第一，超过包括 Jev 自家模型在内的所有列出模型；0.6B、0.8B、4B、9B 也各自领先同尺寸级别，其中 9B（d3-flash）超过上一代 27B（Decision 2.0）。这些 SOTA 排名和分数来自发布方自报的 Reddit 公告，Jev Decision Index 未经独立验证，也未提供深入技术分析或独立复现；发布方还称，在未参与训练的零样本视频测试中，27B 在全部 19,140 道 Perception Test 验证题上得 77.4，4B 得 70.3。

reddit · r/LocalLLaMA · /u/henzy123 · 10月12日 05:26

**「背景：d3 所引用的 Jev Decision Index 是什么」** 本次发布引用的 Jev Decision Index 并非厂商自建的私有评测，而是一个公开排行榜，用于给 TypeSafe 的 Jev 的各种开源复现排名：它把公开基准、针对同类能力的私有测试，以及来自新领域的私有任务折算到同一评分尺度上，并分别设有文本榜与视觉榜，当前索引版本为 0.3（tool-2-2、tool-2-3）。该索引同时提供可在本地或以单个 Hugging Face Job 复现的评测套件（tool-2-1）。按发布方 vLLM Semantic Router 团队的自述，其上一代产品为 Decision 2.0，本次 9B 的 d3-flash 已超过上一代 27B，这一代际对比来自发布内容本身，而非独立验证。

**「影响」** 对使用 vLLM Semantic Router 构建路由层的开发者而言，d3 提供的是直接输出 choice／yes-no／score 概率而非生成文本的决策组件，这意味着集成时要处理 logits 与概率阈值，而不是解析模型生成的文字；加载权重需用 Transformers 并开启 trust\_remote\_code=True，等于在部署中执行模型自带的自定义代码，需按组织安全策略评估。按发布方自述，9B 的 d3-flash 已超过上一代 27B 的 Decision 2.0，若该结果在自有数据上成立，路由与分类环节可用更小显存占用替代原先的 27B 方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/apolinario/decision-index">GitHub - apolinario/decision-index: Decision Index: reproduce ...</a></li>
<li><a href="https://huggingface.co/spaces/multimodalart/jev-decision-index">Jev Decision Index - a Hugging Face Space by multimodalart</a></li>
<li><a href="https://multimodalart-jev-decision-index.static.hf.space/index.html">Decision Index 0.3</a></li>
<li><a href="https://vllm.ai/blog/2026-07-21-vllm-sr-new-chapter-mom">Beyond a Single Model: Building Mixture-of-Models... | vLLM Blog</a></li>
<li><a href="https://github.com/vllm-project/semantic-router">GitHub - vllm -project/ semantic - router : A programmable...</a></li>

</ul>
</details>

**标签**: `#multimodal models`, `#open-source LLMs`, `#model release`, `#vLLM`, `#decision models`

---

<a id="item-tech-news-13"></a>
### [Meta 发布 Muse Wonder 模型，订阅价 20 美元起](https://research.meta.ai/blog/muse-wonder) ⭐️ 7.0/10

Meta 发布 Muse Wonder 系列模型，包含 Muse Wonder 与 Muse Wonder Full。Meta 称新模型能对标 OpenAI 与 Anthropic 的领先模型，并计划未来用于驱动 Muse AI 智能体，但未公布具体时间。通过 Muse 应用访问需每月 20 或 100 美元订阅；两款模型即日起通过 Meta Model API 与 Muse Code 开放，其中 Muse Wonder Full 仅面向 Muse Code 订阅用户，月费 50 或 200 美元。新模型加入 Active Memory 与 Active Focus，Meta 称可减少智能体偏离目标；目前没有基准测试或独立验证，性能对标说法尚属厂商宣称。

telegram · zaihuapd · 10月12日 17:32

**「背景」** Meta 把 Muse Wonder 系列同时放到三个入口：Meta Model API、Muse Code 和 Muse 应用，并按入口划分订阅档位；第三方汇总页面把该结构概括为覆盖 API、Muse Code 与 Muse 应用的每月 4 至 200 美元价格区间，并称 Meta 将这类智能体模型定价在 OpenAI 与 Anthropic 之下（tool-2-1、tool-2-2）。按现有安排，能力更强的 Muse Wonder Full 只随 Muse Code 订阅提供，而 Muse 应用侧走 20/100 美元档，第三方对比文章也正是围绕 API 价格、订阅入口与基准测试展开（tool-2-3）。

**「影响」** 开发者若需要 Muse Wonder Full，必须订阅 Muse Code（每月 50 或 200 美元），无法通过 Meta Model API 调用，因此现有 API 工作流无法直接使用该高端型号；基础版 Muse Wonder 则可通过 API 访问。由于缺乏公开基准和独立验证，团队在采购或集成前难以评估其是否真能对标 OpenAI 与 Anthropic 模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://shattered.io/meta-muse-wonder-ai-pricing-2026/">Meta Muse Wonder Pricing: $4-$200/Mo Explained [2026]</a></li>
<li><a href="https://tech-insider.org/meta-muse-wonder-ai-model-launch-2026/">Meta Muse Wonder AI Takes on OpenAI at $200/Mo [2026]</a></li>
<li><a href="https://kingy.ai/blog/muse-wonder-full-pricing-benchmarks-comparison/">Muse Wonder vs Wonder Full: Pricing, Specs &amp; Benchmarks</a></li>

</ul>
</details>

**标签**: `#Meta`, `#AI models`, `#AI agents`, `#API pricing`, `#model release`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美联储官员哈马克：或需进一步加息，以防通胀心理固化](https://www.cnbc.com/2026/10/12/beth-hammack-fed-inflation-policy.html) ⭐️ 7.0/10

克利夫兰联储主席贝丝·哈马克（Beth Hammack）10 月 12 日表示，可能需要更紧缩的货币政策，才能确保通胀及时回到 2%的目标，暗示或进一步加息。她引用数据称，8 月个人消费支出（PCE）价格指数同比上涨 3.4%，剔除食品和能源的核心指标同比上涨 3%，并称长期通胀预期目前仍“牢牢锚定”，但通胀高于目标已超过五年。

rss · CNBC Finance · 10月12日 17:15

**「背景」** 美联储上月实施了三年来的首次加息，9 月会议纪要显示官员们可能再次投票加息，但未给出时间表；据芝商所 FedWatch 工具，交易员认为本月会议维持利率不变的概率超过 78%，而 12 月加息的概率接近 88%。

**「影响」** 如果美联储进一步加息，信用卡、汽车贷款和浮动利率房贷的还款成本会随之上升，负债较重的家庭和企业将最先感受到压力。

**标签**: `#Federal Reserve`, `#Monetary policy`, `#Interest rates`, `#Inflation`, `#Beth Hammack`

---

<a id="item-finance-news-2"></a>
### [重建后皇岗口岸开通 实施“一地两检”新通关模式](https://sc.isd.gov.hk/TuniS//www.info.gov.hk/gia/general/202610/09/P2026100900280.htm) ⭐️ 7.0/10

重建后的皇岗口岸于 2026 年 10 月 12 日上午 6 时 30 分正式开通，实施“一地两检”及“合作查验、一次放行”新模式，为旅客和车辆提供 24 小时通关服务。据香港政府新闻网报道，整体通关时间由原来约 30 分钟缩短至约 5 分钟，自助通道最快约 20 秒完成通关。

telegram · zaihuapd · 10月12日 05:12

**「背景」** 皇岗口岸重建涉及在香港境内设立港方口岸区并实施“一地两检”，即两地执法人员在同一个口岸区内完成通关查验；香港立法会 2026 年 7 月曾加快审议相关条例草案，安排在 7 月 19 日表决，以便口岸在 7 月底前开放（tool-1-2）。香港官员此前表示，皇岗将是首个采用“合作查验、一次放行”的口岸（tool-1-1）。

**「影响」** 新口岸设 134 条自助通道和 68 个人工柜台，初期预计每日可处理高峰流量 20 万人次，未来可提升至 30 万人次，跨境旅客及客货运输车辆将直接受惠于通关时间缩短和全天候开放。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.dimsumdaily.hk/chris-tang-says-huanggang-port-ready-for-monday-opening/">Chris Tang says Huanggang Port ready for Monday opening</a></li>
<li><a href="https://www.visahq.news/2026-07-16/hk/legco-races-to-pass-huanggang-port-co-location-bill-ahead-of-31-july-opening/">Legco races to pass Huanggang Port co - location bill ahead of 31...</a></li>

</ul>
</details>

**标签**: `#cross-border travel`, `#Hong Kong`, `#Shenzhen`, `#border policy`, `#infrastructure`

---

<a id="item-finance-news-3"></a>
### [中国将新能源汽车出口退税率由 13%下调至 9%](https://www.news.cn/20261012/9709731f470b42f9a84825c2e4eb914b/c.html) ⭐️ 7.0/10

财政部、税务总局 10 月 12 日发布公告，自 2027 年 4 月 1 日起，将新能源汽车增值税出口退税率由 13%下调至 9%，并取消电子烟设备装置等产品的增值税出口退税；公告称对上述产品中征收消费税的产品，出口消费税退（免）税政策不作调整。

telegram · zaihuapd · 10月12日 11:00

**「背景」** 出口退税是指政府对出口产品退还其在国内已缴纳的增值税，使产品以不含税价格进入海外市场；退税率从 13%降到 9%，意味着企业出口时可退回的税款减少，出口成本相应上升。财政部、税务总局在 10 月 12 日的同一份公告中还说明，对上述产品中征收消费税的产品，出口消费税退（免）税政策不作调整；同期，中国汽车工业协会已将新能源汽车称为拉动中国汽车出口增长的核心动力（tool-1-2）。

**「影响」** 退税率下调 4 个百分点会直接压缩中国新能源汽车出口企业的利润空间：同一批出口车能拿回的增值税退税款减少，等于出口成本相应上升，对退税额占售价比重较高、议价能力较弱的中小车企和贸易商压力更明显。

<details><summary>参考链接</summary>
<ul>
<li><a href="http://m.solarzoom.com/article-200666-1.html">中 国 新 能 源 产品涌向全球，光伏 出 口 单月环比猛翻一倍_SOLARZOOM...</a></li>
<li><a href="https://cnevpost.com/2026/10/12/china-cuts-nev-export-tax-rebates/">China cuts NEV export tax rebates, testing profitability of ...</a></li>
<li><a href="https://finance.biggo.com/news/4db04231-c9b1-40b1-9c7a-103b980c50f0">China Cuts NEV Export Tax Rebate to 9% from April 2027 ...</a></li>

</ul>
</details>

**标签**: `#新能源汽车`, `#出口退税`, `#财政政策`, `#中国贸易`, `#产业政策`

---