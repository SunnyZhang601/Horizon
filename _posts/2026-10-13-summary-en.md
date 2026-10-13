---
layout: default
title: "Horizon Summary: 2026-10-13 (EN)"
date: 2026-10-13
lang: en
---

> From 54 items, 16 important content pieces were selected

---

**Technology News**
1. [Python 3.15 released with lazy imports and sampling profiler](#item-tech-news-1) ⭐️ 9.0/10
2. [Cyberattack Triggers Defrost Cycles in European Supermarket Fridges](#item-tech-news-2) ⭐️ 8.0/10
3. [Open-Source Project Turns WiFi 7 Router into 320 Msps SDR Receiver](#item-tech-news-3) ⭐️ 8.0/10
4. [A Modern Web App in C](#item-tech-news-4) ⭐️ 7.0/10
5. [Codex CLI reportedly installs persistent self-updating daemon by default](#item-tech-news-5) ⭐️ 7.0/10
6. [Show HN: PS2 games statically recompiled to WebAssembly](#item-tech-news-6) ⭐️ 7.0/10
7. [LineageOS 24.0 released, rebased onto Android 17](#item-tech-news-7) ⭐️ 7.0/10
8. [learnc tunes constants in unmodified C code, cutting JPEG BD-rate 9.1%](#item-tech-news-8) ⭐️ 7.0/10
9. [Intel Crescent Island GPU Reportedly Named D-Series D270 with up to 480GB LPDDR5X](#item-tech-news-9) ⭐️ 7.0/10
10. [Qwen announces QwenGyre, elastic RL framework for long-horizon agent training](#item-tech-news-10) ⭐️ 7.0/10
11. [OpenBMB releases MiniCPM-V 4.7 35B-A3B, an on-device multimodal MoE](#item-tech-news-11) ⭐️ 7.0/10
12. [Decision 3.0: open multimodal decision models from 0.6B to 27B](#item-tech-news-12) ⭐️ 7.0/10
13. [Meta announces Muse Wonder models with $20/month subscription](#item-tech-news-13) ⭐️ 7.0/10

**Financial News**
1. [Fed&\#x27;s Hammack says restrictive policy may be needed to keep inflation from entrenching](#item-finance-news-1) ⭐️ 7.0/10
2. [Rebuilt Huanggang Port opens with joint border checks and 24-hour clearance](#item-finance-news-2) ⭐️ 7.0/10
3. [China to Cut New Energy Vehicle Export Tax Rebate From 13% to 9%](#item-finance-news-3) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Python 3.15 released with lazy imports and sampling profiler](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 9.0/10

Python 3.15 is out, and Simon Willison highlights PEP 810 explicit lazy imports, PEP 798 unpacking in comprehensions, and a new standard-library sampling profiler; for his open-source work, the release also means dropping Python 3.10 support and adopting Python 3.11 features. PEP 810 adds \`lazy import json\` and \`lazy from pathlib import Path\` syntax so a module is imported only when one of its symbols is first used, which Willison says directly addresses plugin startup costs like installing heavy \`sentence\_transformers\` dependencies for his LLM CLI. \`cProfile\` has been renamed to \`profiling.tracing\` and joined by Tachyon, aka \`profiling.sampling\`, which can attach to a running Python 3.15 process by PID and emit reports, flame graphs, heat maps, and Firefox-profiler-compatible output. Miguel Grinberg&\#x27;s tests against 3.15.0rc3 found performance mostly unchanged from 3.14 except the experimental JIT, which produced a 1.2x speedup over the standard 3.15 interpreter on a Fibonacci test, the first meaningful JIT gain he observed.

rss · Simon Willison · Oct 12, 18:15

**「Background」** Python&\#x27;s comprehension syntax is being extended rather than replaced: PEP 798&\#x27;s unpacking in comprehensions builds on the unpacking generalizations from PEP 448, which the source notes landed in Python 3.5 back in 2015. The release also follows last year&\#x27;s Python 3.14, which Miguel Grinberg&\#x27;s earlier benchmarks found delivered significant speedups over Python 3.13, a contrast that frames his finding that 3.15 performs about the same as 3.14 outside the experimental JIT.

**「Impact」** For developers who support all current Python versions, Python 3.15 means Python 3.10 can be dropped and 3.11-only features adopted, while plugin authors can replace manual lazy-import workarounds with PEP 810 to reduce CLI startup time. The rename of \`cProfile\` to \`profiling.tracing\` is a compatibility change for any tooling that imports the old module name.

**Tags**: `#Python`, `#Python 3.15`, `#PEP 810`, `#lazy imports`, `#open source releases`

---

<a id="item-tech-news-2"></a>
### [Cyberattack Triggers Defrost Cycles in European Supermarket Fridges](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

A reported cyberattack on internet-connected supermarket refrigeration controllers disrupted fridges across Europe, with hackers activating automatic defrosting and also affecting deliveries and store prices, according to Tom&\#x27;s Hardware and the linked reports. The item links Claroty Team82 research into vulnerabilities in Danfoss refrigeration controllers, but the supplied source does not confirm which specific flaw was used or who carried out the attack. The supplied Reuters link names French supermarket chain Intermarché and refers to 150 targets.

hackernews · Zeekaas · Oct 12, 12:16 · [Discussion](https://news.ycombinator.com/item?id=50055304)

**「Background」** Claroty&\#x27;s Team82 research group disclosed in August 2026 that it had found multiple vulnerabilities in the embedded web management interface of Danfoss&\#x27;s AK-SM 800A refrigeration controller platform, warning that successful exploitation could let an attacker manipulate how the device handles requests and control connected equipment. Danfoss released firmware to fix the flaws, and Cybernews reported that a patch for three Danfoss controllers has been available since September 18, meaning the affected hardware family already had a known and partially remediated attack surface before the European supermarket incident.

**「Impact」** For supermarket operators and OT teams, the incident shows that remote management of refrigeration controllers can become an operational risk when legacy devices remain internet-connected; commenters point to end-of-support Danfoss models such as the SM800 \(EOS 2021\) and SC355 \(EOS 2016\) as examples. A practical consequence is that affected organizations need to inventory internet-exposed refrigeration controllers and isolate or upgrade unsupported units, because the reported attack used remote functionality to trigger defrost cycles.

**「Community Discussion」** Commenters debated why refrigeration controllers are internet-connected at all: one cited Danfoss&\#x27;s own material that remote diagnostics and defrost control can generate savings, while another said equipment vendors increasingly require internet subscriptions for machines to run. Others focused on legacy risk, citing end-of-support Danfoss controllers and speculating whether the incident is linked to a reported late-August 2026 disruption at US military bases or a separate group.

<details><summary>References</summary>
<ul>
<li><a href="https://claroty.com/team82/research/freeze-the-controller-defrost-the-food-uncovering-vulnerabilities-in-danfoss-refrigeration-controllers">Freeze the Controller, Defrost the Food: Uncovering ...</a></li>
<li><a href="https://cybernews.com/security/danfoss-refrigeration-hack-france-supermarkets/">Refrigeration Cyberattack Hits French Supermarkets | Cybernews</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#OT/ICS security`, `#IoT`, `#legacy systems`, `#refrigeration controllers`

---

<a id="item-tech-news-3"></a>
### [Open-Source Project Turns WiFi 7 Router into 320 Msps SDR Receiver](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

A GitHub project, w1700k-sdr, demonstrates repurposing a WiFi 7 router into a 320 Msps software-defined radio receiver, bringing a high-sample-rate SDR approach to commodity networking hardware. The item provides no source page details beyond the repository link, so the exact router model, RF tuning range, sample format, and host interface are not established in the supplied material. The project is presented as open source and drew interest from hardware and SDR communities on Hacker News.

hackernews · djfergus · Oct 12, 12:41 · [Discussion](https://news.ycombinator.com/item?id=50055593)

**「Background」** Receiving at microwave frequencies has generally meant dedicated hardware — RTL-SDR-style USB dongles or purpose-built receivers — because commodity Wi-Fi chipsets expose little of their RF front end, and 5 GHz coverage in particular has been expensive to reach cheaply. Wi-Fi 7&\#x27;s much wider channel bandwidth makes a router&\#x27;s radio a plausible wideband sampling front end, which is the premise this project exploits. Commenters also note the same developer previously built an ESP32-based SDR, suggesting this is a continuation of that line of work rather than an isolated experiment.

**「Impact」** For SDR hobbyists and embedded developers, the practical draw is the possibility of using WiFi 7 router hardware for 320 Msps reception, but the supplied material does not verify supported router models, frequency coverage, or host requirements; anyone attempting to reproduce it should confirm those details before relying on the setup.

**「Community Discussion」** Commenters highlighted the same developer&\#x27;s earlier ESP32-based eSpDR project and speculated that the same chipset could extend this to a Banana Pi R4 with PCIe NVMe, while another commenter said it is not DC-to-daylight coverage but is the cheapest way they know to get a 320 Msps receiver at 5 GHz. A third commenter asked whether software-defined radios explain why Samsung requires a contract before third parties can use phone FM radios.

**Tags**: `#software-defined radio`, `#WiFi 7`, `#hardware hacking`, `#open source`, `#embedded systems`

---

<a id="item-tech-news-4"></a>
### [A Modern Web App in C](https://prophitt.me/writing/a-modern-web-app-in-c) ⭐️ 7.0/10

A technical write-up published on prophitt.me describes building a modern web application in C, covering deployment and security practices for software engineers. It discusses using CGI or FastCGI and reducing privileges with chroot or pledge. The post appeared on Hacker News, where commenters compared the approach with alternatives such as Go&\#x27;s single-binary model and busybox&\#x27;s built-in CGI.

hackernews · prophittcorey · Oct 12, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50058528)

**「Background」** CGI has been a standardized way to run programs behind a web server since RFC 3875 defined CGI 1.1, and the setup described here fits what is commonly called the BCHS stack — BSD, C, httpd, SQLite — for which kcgi provides a minimal CGI/FastCGI library for C and C++ applications. On OpenBSD, httpd is privilege-separated and chrooted, with each component pledging only the syscalls it needs, which is the model the write-up builds on for dropping privileges.

**「Community Discussion」** Commenters offered mixed perspectives: one agreed the post&\#x27;s reasoning was sound and highlighted busybox&\#x27;s built-in CGI support, while another argued Go&\#x27;s single-binary model avoids C&\#x27;s concurrency difficulties. A third shared a positive experience running a FastCGI/C web application for over two decades.

<details><summary>References</summary>
<ul>
<li><a href="https://braindetox.kr/en/posts/modern_web_app_in_c_bchs_cgi_2026.html">Decisions Behind a Commercial Web App Built in C and CGI ...</a></li>
<li><a href="https://news.ycombinator.com/item?id=19549085">Secure CGI Applications in C on OpenBSD | Hacker News</a></li>
<li><a href="https://github.com/kristapsdz/kcgi">GitHub - kristapsdz/kcgi: minimal CGI and FastCGI library for ... AsiaBSDCon 2016: Secure CGI Applications in C Privilege Separation and Pledge - OpenBSD kcgi: securing CGI web applications - kristaps.bsd.lv Bob Beck beck@openbsd Pledge,</a></li>

</ul>
</details>

**Tags**: `#C`, `#web development`, `#systems programming`, `#CGI/FastCGI`, `#security`

---

<a id="item-tech-news-5"></a>
### [Codex CLI reportedly installs persistent self-updating daemon by default](https://github.com/openai/codex/issues/48195) ⭐️ 7.0/10

A Hacker News post reports that OpenAI&\#x27;s Codex CLI installs a persistent, self-updating background daemon by default on users&\#x27; systems. Commenters say the daemon writes pid and lock files under ~/.codex at startup and that no documented setting disables it, though a feature flag can be flipped with \`\[features\] daemon\_auto\_start = false\` in ~/.codex/config.toml. Reported consequences include roughly 12 GB of disk use from accumulated old versions and auto-update bugs that can change file permissions and make a project&\#x27;s .git directory read-only.

hackernews · whimblepop · Oct 12, 18:29 · [Discussion](https://news.ycombinator.com/item?id=50060694)

**「Background」** Codex CLI is OpenAI&\#x27;s coding agent that runs locally on a user&\#x27;s machine, and its project page lists installation via npm as \`npm install -g @openai/codex\`. A third-party Codex CLI guide describes daemon-related functionality in the tool, including configurable update schedules, a \`codex app-server daemon update\` command, and thread recovery after daemon restarts — the mechanism at issue in this report, which claims it starts automatically by default.

**「Impact」** For Codex CLI users who want to avoid the default daemon, the reported workaround is to set the undocumented \`daemon\_auto\_start = false\` feature flag and then remove or neutralize the pid and lock files it writes under ~/.codex. Users also need to watch disk usage and permissions: one commenter measured about 12 GB of stale versions, and another reported that auto-updates could leave .git read-only and block coding tasks.

**「Community Discussion」** Commenters are split between practical mitigation and broader frustration: one commenter supplies the config flag and file workarounds, while others report 12 GB of old versions, permission-corrupting auto-updates, and frequent blocks that make the tool hard to trust. One developer argues the alternative is a minimal harness like hax that relies mostly on bash, calling the heavier Codex setup overengineered.

<details><summary>References</summary>
<ul>
<li><a href="https://blakecrosley.com/guides/codex">Codex CLI Guide 2026: Setup, Sandbox, AGENTS.md &amp; MCP</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai / codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**Tags**: `#OpenAI Codex`, `#AI coding tools`, `#background daemon`, `#developer tooling`, `#resource usage`

---

<a id="item-tech-news-6"></a>
### [Show HN: PS2 games statically recompiled to WebAssembly](https://github.com/snuri00/ps2-web-recomp) ⭐️ 7.0/10

A Show HN project, ps2-web-recomp, statically recompiles PlayStation 2 games to WebAssembly; the repository is at github.com/snuri00/ps2-web-recomp. The item does not specify supported titles, performance, build steps, release artifacts, or license, so the practical maturity of the project is not established. It is aimed at developers and retro-gaming readers interested in WebAssembly, binary translation, and emulation.

hackernews · deadxwarrior · Oct 12, 06:46 · [Discussion](https://news.ycombinator.com/item?id=50052251)

**「Background」** Static recompilation translates a game&\#x27;s original machine code ahead of time into source that is compiled for the host platform, instead of interpreting that code at runtime inside a conventional emulator \(tool-2-3\). The same author previously released psp-web-recomp, which translates PSP MIPS code into C++, compiles it to WebAssembly, and links it against a small reimplementation of the PSP&\#x27;s operating system and graphics chip drawn with WebGL 2 \(tool-2-1\); the PS2 project applies a browser-targeted recompilation approach to a different console.

**「Community discussion」** Commenters debated trust and vetting: aceazzameen argued that the growing number of decompilation/static-recompilation projects do not yet have the emulator scene&\#x27;s level of trust and vetting, raising hidden-malware concerns. kodablah reported a related PS Vita project, vitaslop, that instead builds an ARM-to-WASM transpiler in WebAssembly and adds WebGPU shader and audio transcoding; they said it is early, tested on only a few games, but works well in Chrome mobile on flagship Android phones.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/snuri00/psp-web-recomp">GitHub - snuri00/psp-web-recomp: PSP games in the browser without...</a></li>
<li><a href="https://www.generationamiga.com/2026/08/21/masters-of-teras-kasi-recompilation-targets-windows-macos-and-linux/">Masters of Teras Kasi recompilation targets Windows, macOS and...</a></li>

</ul>
</details>

**Tags**: `#WebAssembly`, `#static recompilation`, `#PS2 emulation`, `#binary translation`, `#open source`

---

<a id="item-tech-news-7"></a>
### [LineageOS 24.0 released, rebased onto Android 17](https://lwn.net/Articles/1099950/) ⭐️ 7.0/10

LineageOS 24.0 has been released, rebasing the community Android distribution onto Android 17, which Google released in June 2026. The project says it moved its changes and features onto the Android 17 code base faster than anticipated, noting it is &quot;early this year&quot; compared with previous cycles. The announcement also states that LineageOS will mark 10 years on December 24, 2026, but gives no device list, build schedule, or further technical detail.

rss · LWN.net · Oct 12, 13:13

**「Background」** LineageOS is a community-developed, Android-based distribution that succeeded CyanogenMod, from which it was forked in December 2016 — the origin of the ten-year anniversary the project notes alongside this release. The prior release line was already a rebase effort: LineageOS 23.2 was described by the project as a &quot;Halftime Release&quot; built while updating onto newer AOSP code, and 24.0 continues that pattern by moving the distribution onto Android 17.

**「Impact」** Because the project describes the Android 17 rebase as faster than anticipated, LineageOS 24.0 reaches the Android 17 base earlier in the release cycle than prior LineageOS versions did, shortening the interval between Android 17&\#x27;s release and LineageOS builds based on it for devices whose maintainers port them. The announcement does not name supported devices or a build timeline, so per-device availability is unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/LineageOS">LineageOS - Wikipedia</a></li>
<li><a href="https://www.lineageos.org/Changelog-31/">Changelog 31 - Masterful Material, Expressive Emotions, Awesome...</a></li>

</ul>
</details>

**Tags**: `#LineageOS`, `#Android`, `#open source`, `#mobile OS`, `#custom ROM`

---

<a id="item-tech-news-8"></a>
### [learnc tunes constants in unmodified C code, cutting JPEG BD-rate 9.1%](https://www.reddit.com/r/MachineLearning/comments/1x4dlbm/learnc_fit_the_constants_in_existing_c_code_to/) ⭐️ 7.0/10

learnc is an MIT-licensed tool that optimizes named constants in unmodified C source against a user-written C score function and writes the updated values back to the same file. On held-out data, the author reports 9.1% BD-rate at equal SSIM for the 128 quantization-table entries in stb\_image\_write.h, tuned on 12 Kodak images and tested on the other 12, with the result checked independently in libjpeg using scikit-image; mozjpeg&\#x27;s tables reach 2.7% on the same measure. For Google&\#x27;s WebRTC VAD, tuning every constant in vad\_core.c on LibriParty dev raised F1 from 0.810 to 0.859 on LibriParty eval. These are self-reported results from a Reddit project post rather than independent verification, and the author notes no JPEG gain below 1 bpp and that the approach suits tens to hundreds of constants, not large weight sets.

reddit · r/MachineLearning · /u/keep\_up\_sharma · Oct 12, 20:51

**「Background」** JPEG quantization tables are grids of constant divisors that set the compression-versus-quality trade-off, and mozjpeg&\#x27;s widely used tables were arrived at by hand-tuning; BD-rate is the standard metric for reporting average bitrate change at equal measured quality \(here SSIM\). Google&\#x27;s WebRTC voice-activity detector likewise depends on hard-coded thresholds and constants in vad\_core.c. learnc&\#x27;s premise is to replace that manual tuning with automated search over named constants scored by a user-written C function.

**「Impact」** Developers with a measurable objective and a fixed set of tunable constants in existing C code can apply learnc without restructuring their source, but should expect the method to break down for large parameter sets and for JPEG quality below 1 bpp, where the author reports no gain.

**Tags**: `#C`, `#optimization`, `#JPEG compression`, `#WebRTC VAD`, `#autotuning`

---

<a id="item-tech-news-9"></a>
### [Intel Crescent Island GPU Reportedly Named D-Series D270 with up to 480GB LPDDR5X](https://www.reddit.com/r/LocalLLaMA/comments/1x4g90u/intel_crescent_island_gpu_gets_dseries_name/) ⭐️ 7.0/10

A Reddit post on r/LocalLLaMA reports that Intel&\#x27;s Crescent Island GPU has been named the D-Series D270, with up to 480GB of LPDDR5X memory for ODMs and 160GB for Intel&\#x27;s own configuration, 1.5TB/s of memory bandwidth, and up to 1.3 PFLOPS of FP8 performance. The reported specifications also list 32 Xe3P cores, 256 XMX engines, 32MB of L2 cache, support for FP4 to FP64 formats, PCIe Gen5 x16, a 350W TDP, and a PCIe CEM air-cooled form factor. The post includes no pricing or availability details, and the figures are not confirmed by Intel or independent benchmarks.

reddit · r/LocalLLaMA · /u/Monad\_Maya · Oct 12, 22:42

**「Background」** Intel had already detailed the specifications of its Crescent Island data-center GPU at Hot Chips 2026 \(the week of Aug. 24, 2026\), listing 32 Xe3P cores, 256 XMX engines, and a 350 W air-cooled TDP. Coverage of that disclosure highlighted Intel&\#x27;s choice of LPDDR5X instead of HBM, trading peak memory bandwidth for much larger capacity and lower power in an inference-oriented design. The Reddit post&\#x27;s new element is therefore the D-Series product name \(D270\) rather than the underlying architecture or spec sheet.

**「Impact」** If the reported specifications hold, the 480GB ODM configuration would be the relevant option for maximum local LLM model capacity, while Intel&\#x27;s own listed 160GB configuration would offer less. Prospective buyers still lack pricing, launch timing, and software ecosystem details, and the original poster notes that no generic blower-style variant for prosumer workstations has been announced.

<details><summary>References</summary>
<ul>
<li><a href="https://www.spheron.network/blog/intel-crescent-island-vs-nvidia-gpus-new-inference-chip-expl/">Intel Crescent Island GPU Specs vs NVIDIA... | Spheron Blog</a></li>
<li><a href="https://www.youtube.com/watch?v=KBjgag0QITQ">Intel ’s New GPU Has Nearly Half a Terabyte! - YouTube</a></li>

</ul>
</details>

**Tags**: `#Intel`, `#AI accelerators`, `#local LLM inference`, `#GPU hardware`, `#LPDDR5X memory`

---

<a id="item-tech-news-10"></a>
### [Qwen announces QwenGyre, elastic RL framework for long-horizon agent training](https://www.reddit.com/r/LocalLLaMA/comments/1x41myz/qwen_released_qwengyre_rl_framework_for_training/) ⭐️ 7.0/10

Qwen announced QwenGyre, an &quot;elastic&quot; reinforcement-learning framework for training agents on extreme-long-horizon tasks, with two stated components: an Elastic Scheduler that reallocates GPUs between rollout and training as demand shifts without interrupting live executions, and a Trajectory Processor that converts branching executions — compaction, sub-agents, retries — into prefix-shared trajectory trees with bounded, deduplicated training samples, including scoring of partial progress after a timeout. In the announcement, Qwen says the scheduler delivers up to 1.85× speedup over Colocate and 1.78× over Async, and that scaling to a model it calls Qwen3.8-2.4T-A95B with roughly 700K tokens per rollout raised NL2RepoBench from 52.5% to 58.5% in 48 steps while cutting end-to-end training time about 44% versus Async. These figures are the vendor&\#x27;s own claims in a Reddit post; no independent measurement, code release, or verification is provided in the source, and the linked paper is given only as arXiv:2609.33848.

reddit · r/LocalLLaMA · /u/ResearchCrafty1804 · Oct 12, 13:18

**「Background」** Agent reinforcement learning typically alternates between rollout generation and policy updates, and existing systems either colocate both phases on the same GPUs or run them asynchronously with fixed resource splits. That arrangement becomes costly for extreme-long-horizon work, where a single harness execution can run for hours and process close to a million tokens, shifting GPU demand constantly between the two phases. The paper behind QwenGyre \(arXiv:2609.33848, posted September 2026\) describes separating the lifetimes of harness executions, GPU roles, and training samples so capacity can be reallocated without interrupting live rollouts.

**「Impact」** For teams running RL on long-horizon agent tasks, QwenGyre replaces a fixed rollout/training GPU split with an elastic one: its scheduler reassigns GPUs as demand shifts without interrupting live executions, which the project reports as up to 1.85× faster than Colocate and 1.78× faster than Async. The paired trajectory processor also changes what counts as usable training data — branching executions are reconstructed into prefix-shared trees, redundant paths are deduplicated, and partial progress after a timeout is still scored — so pipelines that currently discard timed-out or retried rollouts would need branch-aware sampling to reproduce the reported efficiency and benchmark gains.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.33848">[2609.33848] QwenGyre: An Elastic Reinforcement Learning ...</a></li>
<li><a href="https://arxiv.org/html/2609.33848v1">QwenGyre: An Elastic Reinforcement Learning Framework ...</a></li>
<li><a href="https://www.marktechpost.com/2026/10/12/alibaba-qwen-introduces-qwengyre-elastic-reinforcement-learning-rl-for-xlong-horizon-agents/">Alibaba Qwen Introduces QwenGyre: Elastic Reinforcement ...</a></li>
<li><a href="https://huggingface.co/papers/2609.33848">Paper page - QwenGyre : An Elastic Reinforcement Learning...</a></li>
<li><a href="https://cctest.ai/en/articles/qwengyre-targets-gpu-idling-and-trajectory-redundancy-in-long-horizon-agent-rl">QwenGyre Improves Reinforcement Learning for Long - Horizon Agents</a></li>

</ul>
</details>

**Tags**: `#reinforcement learning`, `#AI agents`, `#long-horizon tasks`, `#distributed training`, `#Qwen`

---

<a id="item-tech-news-11"></a>
### [OpenBMB releases MiniCPM-V 4.7 35B-A3B, an on-device multimodal MoE](https://www.reddit.com/r/LocalLLaMA/comments/1x47taj/openbmbminicpmv4735ba3b/) ⭐️ 7.0/10

OpenBMB announced MiniCPM-V 4.7 in a 35B-A3B variant, the first mixture-of-experts model in the MiniCPM-V series, with GGUF weights published on Hugging Face. The vendor claims it is the first open-source MoE to run smoothly on-device without performance loss, combining Lookahead Expert Scheduling \(LES\), fine-grained layer-wise quantization, and DSpark speculative sampling to reach 13+ tokens/s on an iPhone 17 Pro Max — figures that come from OpenBMB&\#x27;s model card and have no independent benchmark confirmation in the supplied material. It supports iOS, Android, and HarmonyOS, claims day-0 support for Rockchip, Houmo, Intel, AMD, and Arm chips, and lists inference frameworks SGLang, vLLM, llama.cpp, and Ollama plus GGUF, BNB, AWQ, GPTQ, and FP8 quantization variants. OpenBMB also says the Instruct mode scores higher overall in less inference time than Qwen3.6 35B-A3B, and released Self-Replay Fine-Tuning alongside fine-tuning support for SWIFT and LLaMA-Factory.

reddit · r/LocalLLaMA · /u/Skyline34rGt · Oct 12, 17:16

**「Background」** MiniCPM-V is OpenBMB&\#x27;s series of multimodal LLMs designed for efficient vision-language understanding across image, video, and text inputs on end-side devices; earlier members in the repository include MiniCPM-Llama3-V 2.5, MiniCPM-V 2.6, and MiniCPM-V 4.0. According to the model card, the new 35B-A3B variant is the first mixture-of-experts model in that MiniCPM-V line, whereas earlier entries were dense models. The series itself traces back to OpenBMB and Tsinghua&\#x27;s NLP lab, whose initial MiniCPM-2B work established the on-device, small-parameter focus and supporting deployments such as llama.cpp.

**「Deployment Constraint」** Developers who want this model on a single local machine face a size barrier: the BF16 checkpoint holds 35.2B parameters across roughly 70.4 GB in sixteen shards, so running it locally depends on the released GGUF, BNB, AWQ, GPTQ, or FP8 quantized variants or a multi-device split. Existing SGLang, vLLM, llama.cpp, and Ollama pipelines are supported, so no new inference framework is required, though the advertised 13+ tokens/s on iPhone 17 Pro Max remains a vendor claim rather than an independently measured figure.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/OpenBMB/MiniCPM-V">GitHub - OpenBMB/MiniCPM-V: A Pocket-Sized MLLM for Ultra ...</a></li>
<li><a href="https://github.com/OpenBMB/MiniCPM">GitHub - OpenBMB/MiniCPM: MiniCPM5: SOTA on-device LLMs ... openbmb/MiniCPM-V · Hugging Face MiniCPM-V 4.7: A 35B MoE Vision Model That Runs on an iPhone Inference and Deployment | OpenBMB/MiniCPM | DeepWiki MiniCPM-V Series | OpenBMB/MiniCPM-o | DeepWiki MiniCPM-V: A GPT-4V Level MLLM on Your Phone - arXiv.org</a></li>
<li><a href="https://huggingface.co/openbmb/MiniCPM-V">openbmb/MiniCPM-V · Hugging Face</a></li>
<li><a href="https://www.orcarouter.ai/blog/minicpm-v-4-7-vs-ui-venus-2-9b">MiniCPM - V 4 . 7 vs UI-Venus 2.9B Compared</a></li>

</ul>
</details>

**Tags**: `#on-device AI`, `#MoE`, `#multimodal LLM`, `#quantization`, `#open-source models`

---

<a id="item-tech-news-12"></a>
### [Decision 3.0: open multimodal decision models from 0.6B to 27B](https://www.reddit.com/r/LocalLLaMA/comments/1x3th4p/decision_30_open_multimodal_decision_models_from/) ⭐️ 7.0/10

The vLLM Semantic Router team announced Decision 3.0 \(d3\), an Apache-2.0 family of open multimodal decision models spanning 0.6B to 27B parameters, built on Qwen3.5 \(0.8B / 2B / 4B / 9B\) and Qwen3.8-27B, with the vision encoder included in the parameter counts. The models return a probability for choice, yes/no, and score decisions instead of generating text, accepting multiple images per request at up to 1.6 MP and multiple MP4/WebM/MOV/MKV videos sampled at 2 fps with at most 32 frames per clip at up to 0.2 MP each; weights are BF16 and load through Transformers with trust\_remote\_code=True. Using the official Jev 0.3 kit on the released weights, the team reports the 27B ranked first on both boards \(64.7 text, 71.6 vision\), each smaller size leading its class, the 9B \(d3-flash\) beating the previous-generation 27B \(Decision 2.0\), and the 27B scoring 77.4 with the 4B at 70.3 zero-shot across all 19,140 Perception Test validation video questions despite no video in training. These results are self-reported in the release announcement and the benchmark index is not independently verified here.

reddit · r/LocalLLaMA · /u/henzy123 · Oct 12, 05:26

**「What the Jev Decision Index measures」** The Jev Decision Index is an open reproduction of TypeSafe&\#x27;s Jev decision-model benchmark: it ranks open reproductions by a &quot;Full score&quot; that combines public benchmarks, private tests of the same skills, and private tasks drawn from new domains on one scale, with per-model breakdowns and a separate vision board—the two boards referenced by the release. A companion decision-index repository lets others reproduce the suite locally or as a single Hugging Face Job, which is the kit the Decision 3.0 authors say they ran on the released weights.

**「Impact」** Developers building Mixture-of-Models routing with vLLM Semantic Router — a programmable layer that selects or composes a model path per request across heterogeneous LLM infrastructure — can use the d3 checkpoints as the decision component, since the family is Apache-2.0 and released as regular Hugging Face weights rather than a hosted API. Two integration conditions come from the release itself: the weights are BF16 and load through Transformers with trust\_remote\_code=True, meaning repository-supplied code executes, and the models return a probability for each choice/yes-no/score answer instead of generated text, so calling code must consume probabilities rather than text completions.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/apolinario/decision-index">GitHub - apolinario/decision-index: Decision Index: reproduce ...</a></li>
<li><a href="https://huggingface.co/spaces/multimodalart/jev-decision-index">Jev Decision Index - a Hugging Face Space by multimodalart</a></li>
<li><a href="https://multimodalart-jev-decision-index.static.hf.space/index.html">Decision Index 0.3</a></li>
<li><a href="https://vllm.ai/blog/2026-07-21-vllm-sr-new-chapter-mom">Beyond a Single Model: Building Mixture-of-Models... | vLLM Blog</a></li>
<li><a href="https://github.com/vllm-project/semantic-router">GitHub - vllm -project/ semantic - router : A programmable...</a></li>

</ul>
</details>

**Tags**: `#multimodal models`, `#open-source LLMs`, `#model release`, `#vLLM`, `#decision models`

---

<a id="item-tech-news-13"></a>
### [Meta announces Muse Wonder models with $20/month subscription](https://research.meta.ai/blog/muse-wonder) ⭐️ 7.0/10

Meta announced the Muse Wonder and Muse Wonder Full model series, saying they will rival leading OpenAI and Anthropic models and eventually power Muse AI agents, without giving a timeline. The company said both models are available immediately through the Meta Model API and Muse Code, though Muse Wonder Full is restricted to Muse Code subscribers at $50 or $200 per month. Muse app access costs $20 or $100 per month, and the models add Active Memory and Active Focus intended to keep agents from drifting off task. Meta did not publish benchmarks or technical details, so the performance claims remain unverified.

telegram · zaihuapd · Oct 12, 17:32

**「Background」** Meta&\#x27;s Muse Wonder series is a new family of agent-focused models split into Muse Wonder and Muse Wonder Full, with the Full model reserved for Muse Code subscribers. Meta says the models add Active Memory and Active Focus to reduce agent drift, and external coverage of the October 12, 2026 launch frames the lineup as a price-focused challenge to OpenAI and Anthropic, though Meta&\#x27;s brief does not include benchmarks or technical specifications.

**「Impact」** Developers who want Muse Wonder Full must subscribe to Muse Code at $50 or $200 per month, and Muse app users face $20 or $100 monthly tiers. Because Meta provided no benchmarks or technical documentation, prospective users cannot yet independently assess compatibility or performance against OpenAI and Anthropic models.

<details><summary>References</summary>
<ul>
<li><a href="https://tech-insider.org/meta-muse-wonder-ai-model-launch-2026/">Meta Muse Wonder AI Takes on OpenAI at $200/Mo [2026]</a></li>

</ul>
</details>

**Tags**: `#Meta`, `#AI models`, `#AI agents`, `#API pricing`, `#model release`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed&\#x27;s Hammack says restrictive policy may be needed to keep inflation from entrenching](https://www.cnbc.com/2026/10/12/beth-hammack-fed-inflation-policy.html) ⭐️ 7.0/10

Cleveland Fed President Beth Hammack, a voting member of the Fed&\#x27;s rate-setting committee, said Monday that a restrictive monetary policy stance is appropriate to return inflation to the central bank&\#x27;s 2% target, signaling further interest rate increases are possible. The Fed&\#x27;s preferred inflation gauge, the personal consumption expenditures price index, was 3.4% higher than a year earlier in August, with the core measure — which excludes food and energy — at 3.0% year over year.

rss · CNBC Finance · Oct 12, 17:15

**「Background」** The Fed raised rates last month for the first time in three years, and Hammack said inflation has run above the 2% target for more than five years; traders price a nearly 88% chance of another increase at the December meeting, according to CME&\#x27;s FedWatch tool.

**「Impact」** A further rate increase would raise borrowing costs for households and businesses, the channel the Fed uses to cool demand and inflation.

**Tags**: `#Federal Reserve`, `#Monetary policy`, `#Interest rates`, `#Inflation`, `#Beth Hammack`

---

<a id="item-finance-news-2"></a>
### [Rebuilt Huanggang Port opens with joint border checks and 24-hour clearance](https://sc.isd.gov.hk/TuniS//www.info.gov.hk/gia/general/202610/09/P2026100900280.htm) ⭐️ 7.0/10

The rebuilt Huanggang Port opened at 6:30 a.m. on October 12, 2026, using &quot;co-location&quot; checks — Hong Kong and mainland border formalities handled in one place — plus a single joint inspection-and-release step, with 24-hour clearance for travelers and vehicles. According to the government announcement, typical processing time falls from about 30 minutes to about 5 minutes, with self-service gates clearing travelers in as little as 20 seconds.

telegram · zaihuapd · Oct 12, 05:12

**「Background」** Co-location \(&quot;one place, two checks&quot;\) means Hong Kong and mainland officers work in the same building, so travellers clear both sides in one place; Hong Kong lawmakers fast-tracked the Huanggang Port Hong Kong Port Area Bill to permit this at the rebuilt checkpoint. Unlike older co-location crossings, where travellers still queue twice, Huanggang&\#x27;s process requires only one queue.

**「Impact」** Cross-border travelers and freight moving through the Shenzhen–Hong Kong crossing stand to face shorter queues: the port has 134 self-service channels and 68 staffed counters, with an initial estimated daily peak capacity of 200,000 people that officials say can rise to 300,000.

<details><summary>References</summary>
<ul>
<li><a href="https://www.visahq.news/2026-07-16/hk/legco-races-to-pass-huanggang-port-co-location-bill-ahead-of-31-july-opening/">Legco races to pass Huanggang Port co - location bill ahead of 31...</a></li>
<li><a href="https://www.scmp.com/opinion/comment/article/3362912/new-huanggang-port-must-deliver-its-promise-seamless-borders">Editorial | New Huanggang Port must deliver on its promise of...</a></li>

</ul>
</details>

**Tags**: `#cross-border travel`, `#Hong Kong`, `#Shenzhen`, `#border policy`, `#infrastructure`

---

<a id="item-finance-news-3"></a>
### [China to Cut New Energy Vehicle Export Tax Rebate From 13% to 9%](https://www.news.cn/20261012/9709731f470b42f9a84825c2e4eb914b/c.html) ⭐️ 7.0/10

China&\#x27;s Ministry of Finance and State Taxation Administration announced on October 12 that the value-added tax export rebate rate for new energy vehicles will be lowered from 13% to 9%, effective April 1, 2027. The same notice cancels VAT export rebates for e-cigarette devices and related products, while consumption tax rebate or exemption treatment for affected goods that are subject to consumption tax remains unchanged.

telegram · zaihuapd · Oct 12, 11:00

**「Background」** An export VAT rebate refunds value-added tax that exporters have already paid on their inputs, letting them sell abroad without carrying that tax; lowering the rate from 13% to 9% therefore raises their effective tax cost unless they raise prices or absorb it. New energy vehicles have been described by the China Association of Automobile Manufacturers as a core driver of growth in China&\#x27;s vehicle exports, so the change is aimed at a sector with large export volumes.

**「Impact」** Chinese new energy vehicle exporters, including makers of the 67 product categories covered by the change, would absorb a smaller VAT refund on each exported unit from April 2027, effectively raising their export cost and compressing margins unless they pass it on through prices.

<details><summary>References</summary>
<ul>
<li><a href="http://m.solarzoom.com/article-200666-1.html">中 国 新 能 源 产品涌向全球，光伏 出 口 单月环比猛翻一倍_SOLARZOOM...</a></li>
<li><a href="https://cnevpost.com/2026/10/12/china-cuts-nev-export-tax-rebates/">China cuts NEV export tax rebates, testing profitability of ...</a></li>
<li><a href="https://www.reuters.com/world/china-lower-vat-export-rebate-new-energy-vehicles-2026-10-12/">China to lower VAT export rebate on new energy vehicles</a></li>
<li><a href="https://finance.biggo.com/news/4db04231-c9b1-40b1-9c7a-103b980c50f0">China Cuts NEV Export Tax Rebate to 9% from April 2027 ...</a></li>

</ul>
</details>

**Tags**: `#新能源汽车`, `#出口退税`, `#财政政策`, `#中国贸易`, `#产业政策`

---