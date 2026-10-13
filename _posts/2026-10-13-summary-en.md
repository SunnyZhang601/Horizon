---
layout: default
title: "Horizon Summary: 2026-10-13 (EN)"
date: 2026-10-13
lang: en
---

> From 46 items, 14 important content pieces were selected

---

**Technology News**
1. [Reported Cyberattack Activates Defrosting in European Supermarket Fridges](#item-tech-news-1) ⭐️ 8.0/10
2. [Open-Source Project Turns WiFi 7 Router into 320 Msps SDR Receiver](#item-tech-news-2) ⭐️ 8.0/10
3. [Meta Announces Muse Wonder AI Model, Drawing Benchmarks and Privacy Concerns](#item-tech-news-3) ⭐️ 8.0/10
4. [Python 3.15 ships with explicit lazy imports and a sampling profiler](#item-tech-news-4) ⭐️ 8.0/10
5. [learnc tunes named constants in unmodified C code: 9.1% smaller JPEGs](#item-tech-news-5) ⭐️ 8.0/10
6. [A Modern Web App in C: Deployment and Privilege Separation Discussion](#item-tech-news-6) ⭐️ 7.0/10
7. [Codex CLI installs a persistent self-updating daemon by default](#item-tech-news-7) ⭐️ 7.0/10
8. [LineageOS 24.0 released, rebased onto Android 17](#item-tech-news-8) ⭐️ 7.0/10
9. [Looped Diffusion Transformer reuses blocks per denoising step, loop depth set at sampling time](#item-tech-news-9) ⭐️ 7.0/10
10. [Anthropic reports 90–99% drop in distilled Claude data](#item-tech-news-10) ⭐️ 7.0/10

**Financial News**
1. [Fed&\#x27;s Hammack says restrictive policy may be needed to curb inflation](#item-finance-news-1) ⭐️ 8.0/10
2. [China to Cut NEV Export VAT Rebate From 13% to 9% in 2027](#item-finance-news-2) ⭐️ 8.0/10
3. [China and EU reach consensus on hybrid, EV trade; China&\#x27;s quota to be no lower than other import sources](#item-finance-news-3) ⭐️ 7.0/10
4. [China&\#x27;s new tax penalty benchmark takes effect Nov 1, adding employer social-insurance arrears](#item-finance-news-4) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Reported Cyberattack Activates Defrosting in European Supermarket Fridges](https://www.tomshardware.com/tech-industry/cyber-security/unprecedented-cyberattack-cripples-supermarket-fridges-across-europe-as-hackers-activate-automatic-defrosting-delivery-and-store-prices-also-impacted-by-incident) ⭐️ 8.0/10

A cyberattack reportedly disrupted supermarket refrigeration across Europe, with hackers activating automatic defrosting in internet-connected Danfoss refrigeration controllers. French supermarket chain Intermarché was affected, with reports saying 150 stores were targeted and that the incident forced refrigerator shutdowns and disrupted deliveries and store prices. Claroty research on Danfoss controller vulnerabilities has been cited as related context, but the specific exploited vulnerability and the attackers&\#x27; identity have not been confirmed.

hackernews · Zeekaas · Oct 12, 12:16 · [Discussion](https://news.ycombinator.com/item?id=50055304)

**「Background」** In August 2026, Claroty&\#x27;s Team82 research team published findings on the attack surface of Danfoss&\#x27;s AK-SM 800A refrigeration controller platform, describing multiple vulnerabilities in its embedded web management interface and saying Danfoss addressed them in a new firmware release; the trio was tracked as CVE-2025-41450, CVE-2025-41451 and CVE-2025-41520. The AK-SM 800A is a centralised system manager that coordinates refrigeration controllers, and as of The Stack&\#x27;s report on the European supermarket outages, which specific vulnerabilities were exploited remained contested.

**「Impact」** For supermarkets running these controllers, the consequence is operational: remotely triggered defrost cycles spoil refrigerated stock and, per the source, disrupt store pricing and delivery. Commenters note the implicated models, such as the Danfoss SM800 \(end of support 2021\) and SC355 \(2016\), are past end-of-support, so operators cannot rely on firmware fixes and instead face segmenting or replacing internet-exposed controllers. Intermarché&\#x27;s operating group has also confirmed a breach affecting nearly 300,000 customers&\#x27; click-and-collect history, extending the fallout beyond refrigeration.

**「Community Discussion」** Commenters cited older Danfoss controllers, such as the SM800 \(end-of-support 2021\) and SC355 \(end-of-support 2016\), as possible suspects and argued that cost and maintenance constraints leave such equipment without security reviews or timely replacement. One commenter quoted Danfoss material saying internet connectivity enables remote diagnostics and efficiency savings, while another speculated about a link to a reported late-August 2026 incident at US military bases; that connection remains unconfirmed.

<details><summary>References</summary>
<ul>
<li><a href="https://claroty.com/team82/research/freeze-the-controller-defrost-the-food-uncovering-vulnerabilities-in-danfoss-refrigeration-controllers">Freeze the Controller, Defrost the Food: Uncovering ...</a></li>
<li><a href="https://www.thestack.technology/french-supermarkets-hacked-danfoss-vulnerabilities-blamed/">French supermarkets hacked: Danfoss vulnerabilities blamed</a></li>
<li><a href="https://www.connexionfrance.com/news/intermarche-cyberattack-affects-nearly-300000-customers/806317">Intermarché cyberattack 2026 : Nearly 300,000 customers&#x27; data stolen...</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#OT security`, `#embedded systems`, `#industrial control systems`, `#Danfoss`

---

<a id="item-tech-news-2"></a>
### [Open-Source Project Turns WiFi 7 Router into 320 Msps SDR Receiver](https://github.com/h0m3us3r/w1700k-sdr) ⭐️ 8.0/10

An open-source GitHub project, w1700k-sdr, demonstrates converting a WiFi 7 router into a 320 Msps software-defined radio receiver. The project targets commodity router hardware to make high-sample-rate SDR more accessible, but the supplied material does not include independent performance measurements, supported router models, or host-compatibility requirements. The repository is presented as a working demonstration rather than an independently verified benchmark or commercial product.

hackernews · djfergus · Oct 12, 12:41 · [Discussion](https://news.ycombinator.com/item?id=50055593)

**「Background」** Wi-Fi radio chips such as the MediaTek MT7996 are already software-defined in structure, but their stock firmware normally exposes only 802.11 traffic rather than raw IQ samples. This project&\#x27;s approach is to replace that firmware register by register so the radio on the Gemtek W1700K comes up from cold power-on as a general-purpose wideband receiver. A Hacker News commenter noted that the same developer previously built an SDR from an ESP32 Wi-Fi microcontroller, making the router version a higher-sample-rate follow-on to that work.

**「Hardware compatibility」** Prospective users should check the router&\#x27;s chipset rather than the WiFi 7 label: a commenter claims the same chipset appears in the Banana Pi BPI-R4, a WiFi 7 router board built on the MediaTek MT7988A \(Filogic 880\) with M.2/PCIe support, which could make the receiver portable to that board. That remains an untested community claim about a specific board, not a confirmed port, so anyone buying hardware to reproduce the setup should verify board and firmware support first.

**「Community Discussion」** Commenters described the project as a potentially cheap way to get a 320 Msps receiver at 5 GHz, with one calling it “not DC to daylight” but likely the cheapest option they knew. Another commenter speculated that the same chipset should work on the Banana Pi R4, and a third pointed to the same developer’s earlier ESP32-based eSpDR project as evidence of broader SDR experimentation on commodity Wi-Fi hardware.

<details><summary>References</summary>
<ul>
<li><a href="https://daily.dev/posts/turn-a-wifi-7-router-into-a-320msps-software-defined-radio-receiver-38irzaw8t">Turn a WiFi 7 Router into a 320Msps Software Defined...</a></li>
<li><a href="https://zeli.app/story/50055593">Wi-Fi 7 router turned into a 320 Msps · 56 HN comments | Zeli</a></li>
<li><a href="https://www.youtube.com/watch?v=vX3PTE8jCeQ">Banana Pi BPI- R 4 Wifi 7 Router with MTK MT 7988 , test... - YouTube</a></li>
<li><a href="https://banana-pi.org/en/bananapi-router/155.html">Banana Pi BPI- R 4 Wifi 7 Router board with MTK MT 7988 A design...</a></li>

</ul>
</details>

**Tags**: `#software-defined radio`, `#WiFi 7`, `#hardware hacking`, `#open source`, `#RF signal processing`

---

<a id="item-tech-news-3"></a>
### [Meta Announces Muse Wonder AI Model, Drawing Benchmarks and Privacy Concerns](https://research.meta.ai/blog/muse-wonder) ⭐️ 8.0/10

Meta announced a new AI model called Muse Wonder in a post on its research blog, and the announcement drew roughly 550 points and 303 comments on Hacker News. The supplied item contains no model card, version number, licensing, or availability details, and Meta&\#x27;s published benchmark figures could not be independently verified here. In comments, developers reported hands-on comparisons: one image-to-HTML test placed Muse Wonder well below Opus 5.5, closer to Sonnet or Haiku, which the tester called disappointing given the benchmark numbers. A separate commenter reported that signing into a Quest-only Meta account through the Muse Code developer site exposed other people&\#x27;s names, profiles, and emails in the login flow — an unconfirmed user claim, but a serious one.

hackernews · meetpateltech · Oct 12, 16:48 · [Discussion](https://news.ycombinator.com/item?id=50059115)

**「Background」** Muse Wonder is the latest entry in a Meta model family that already existed: Meta announced Muse as a personal AI agent in September 2026, and Muse Spark variants have been shipping through third-party API channels, where Muse Spark 1.3 is listed with a 1,048,576-token context window and independent benchmark scores. Commenters in the current thread ground their comparisons in that lineage, noting Muse Spark 1.2 in August and Muse 1.3 in September as the prior points of reference for image-to-SVG output.

**「Impact」** Developers testing Muse Code sign in with a Meta account, and one commenter reported that doing so listed unrelated people&\#x27;s profiles and emails in the login authorization flow and left account settings inaccessible; that is a user-reported experience, not independently verified. Meta&\#x27;s own privacy documentation states that Muse can be kept on a separate account so its interactions are not shared with other Meta products, which is the concrete mitigation available to anyone evaluating the model now.

**「Community Discussion」** Commenters split between benchmarking and a reported privacy problem: jjcm&\#x27;s image-to-HTML test rated Muse Wonder far weaker than Opus 5.5 and closer to Sonnet or Haiku, while simonw posted SVG &quot;pelican&quot; comparisons against earlier runs with Muse Spark 1.2 and Muse 1.3. pmuse reported that the Muse Code site surfaced unrelated people&\#x27;s profiles and emails during Meta account sign-in and that account settings were inaccessible, and atleastoptimal argued that having several frontier labs is preferable to one holding all the power — a general claim not tied to evidence about Muse Wonder.

<details><summary>References</summary>
<ul>
<li><a href="https://about.fb.com/news/2026/09/introducing-muse-personal-ai-agent/">Introducing Muse : The World’s First Personal AI Agent Built for Everyone</a></li>
<li><a href="https://openrouter.ai/meta/muse-spark-1.3">Muse Spark 1.3 - API Pricing &amp; Benchmarks | OpenRouter</a></li>
<li><a href="https://muse.ai/privacy">Muse Privacy Policy</a></li>

</ul>
</details>

**Tags**: `#Meta AI`, `#LLM release`, `#model benchmarking`, `#AI privacy`, `#Hacker News`

---

<a id="item-tech-news-4"></a>
### [Python 3.15 ships with explicit lazy imports and a sampling profiler](https://simonwillison.net/2026/Oct/12/python-3-15/) ⭐️ 8.0/10

Python 3.15 has been released, with the &quot;What&\#x27;s new&quot; guide curated by 3.14 and 3.15 release manager Hugo van Kemenade. The headline addition is PEP 810 explicit lazy imports, which let code write \`lazy import json\` or \`lazy from pathlib import Path\` so the module loads only when those symbols are first used; PEP 798 adds unpacking syntax in comprehensions such as \`\[\*sublist for sublist in lists\]\`. The standard library gains a sampling profiler called Tachyon \(\`profiling.sampling\`\) that can attach to a running process by PID and produce reports, flame graphs and Firefox-profiler output, while the existing tracing profiler is renamed from \`cProfile\` to \`profiling.tracing\`. On performance, Miguel Grinberg&\#x27;s tests against the 3.15.0rc3 release found speeds mostly unchanged from 3.14, except for the experimental JIT, which gave a 1.2x boost over the standard 3.15 interpreter on a Fibonacci benchmark.

rss · Simon Willison · Oct 12, 18:15

**「Background」** Python 3.15 is the annual release that follows 3.14, and its headline feature, PEP 810 explicit lazy imports, was proposed in October 2025: the \`lazy import\` syntax defers loading a module until one of its symbols is first used, which the PEP frames as a way to cut startup time and memory use in command-line tools, test suites, and applications with large dependency graphs. The new comprehension unpacking syntax extends PEP 448, the unpacking generalization that landed in Python 3.5 in 2015, from calls, literals and assignments into comprehensions.

**「Impact」** For developers who keep libraries working across every supported Python version, dropping Python 3.10 means 3.11-only features become usable; Willison describes making exactly that transition. Lazy imports also remove a previously documented workaround for his LLM CLI tool, where plugin authors had to hand-roll lazy loading because plugins using heavy dependencies such as \`sentence\_transformers\` could add multiple seconds to every \`llm\` invocation.

<details><summary>References</summary>
<ul>
<li><a href="https://peps.python.org/pep-0810/">PEP 810 – Explicit lazy imports | peps.python.org</a></li>
<li><a href="https://docs.python.org/3/whatsnew/3.15.html">What’s new in Python 3.15 — Python 3.15.0 documentation</a></li>

</ul>
</details>

**Tags**: `#Python`, `#Python 3.15`, `#PEP 810`, `#lazy imports`, `#programming languages`

---

<a id="item-tech-news-5"></a>
### [learnc tunes named constants in unmodified C code: 9.1% smaller JPEGs](https://www.reddit.com/r/MachineLearning/comments/1x4dlbm/learnc_fit_the_constants_in_existing_c_code_to/) ⭐️ 8.0/10

learnc, an MIT-licensed tool, optimizes named constants in unmodified C code against a score function the user writes in C, then writes the same file back with the new values. On held-out data it reports 9.1% BD-rate at equal SSIM when tuning the 128 quantization-table entries in stb\_image\_write.h \(tuned on 12 Kodak images, tested on the other 12\), independently checked in libjpeg with scikit-image, compared with 2.7% for mozjpeg&\#x27;s tables. Tuning every constant in Google&\#x27;s WebRTC vad\_core.c on LibriParty dev raised F1 on the LibriParty eval set from 0.810 to 0.859. The author states the method yields no JPEG gain below 1 bpp and works best for tens to hundreds of constants, not large weight sets.

reddit · r/MachineLearning · /u/keep\_up\_sharma · Oct 12, 20:51

**「Why tuning hard-coded constants matters」** JPEG encoders ship fixed quantization tables: the Annex K table defines the standard baseline, while encoders such as mozjpeg offer an alternative custom table tuned for MS-SSIM, and Guetzli&\#x27;s closed-loop optimizer jointly optimizes global quantization tables and per-block DCT coefficients to cut bitrate \(tool-2-1, tool-2-2\). Those earlier efforts changed the tables themselves; learnc instead takes named constants already present in arbitrary C source — here the 128 quantization-table entries in stb\_image\_write.h and the constants in Google&\#x27;s WebRTC vad\_core.c — and searches for new values against a user-supplied C score function.

**「Impact」** Because learnc edits existing source files in place instead of requiring a rewrite or framework, developers can point it at C code whose constants were hand-tuned, but the reported WebRTC VAD result came from changing every constant in vad\_core.c, so adopters should re-validate behavior on their own held-out data. The stated limits bound where it is worth trying: no JPEG gain below 1 bpp, and poor scaling beyond hundreds of constants.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/imagemin/imagemin-mozjpeg">GitHub - imagemin/imagemin- mozjpeg : Imagemin plugin for mozjpeg</a></li>
<li><a href="https://arxiv.org/pdf/1703.04421">Guetzli: Perceptually Guided JPEG Encoder</a></li>

</ul>
</details>

**Tags**: `#C`, `#program optimization`, `#JPEG`, `#WebRTC VAD`, `#open-source tooling`

---

<a id="item-tech-news-6"></a>
### [A Modern Web App in C: Deployment and Privilege Separation Discussion](https://prophitt.me/writing/a-modern-web-app-in-c) ⭐️ 7.0/10

A Hacker News-discussed blog post titled “A Modern Web App in C” describes building a modern web application in C, with commenters highlighting its treatment of deployment and privilege dropping, including pledge and chroot. The post is a technical write-up, not a release announcement, and the supplied material does not include its full source content, so the app&\#x27;s specific architecture and performance cannot be independently verified. Commenters frame the approach against CGI, FastCGI, busybox&\#x27;s built-in CGI support, and persistent backends.

hackernews · prophittcorey · Oct 12, 16:13 · [Discussion](https://news.ycombinator.com/item?id=50058528)

**「Background」** The post revives the CGI model, in which a web server forks a separate program for each request instead of keeping a long-lived application process in memory. According to search results, in 1994 a dynamic website meant writing a C program, dropping it into a cgi-bin directory, and letting Apache fork it per request, and the author&\#x27;s commercial product marketyour.games runs on the BCHS stack \(BSD, C, httpd, SQLite\).

**「Impact」** The discussion surfaces a concrete deployment trade-off for developers considering C web services: a CGI-style process-per-request model can drop privileges with pledge and chroot, but it cannot keep in-process state, whereas a persistent backend can maintain state, according to commenters. Commenters did not present benchmarks or a definitive recommendation.

**「Community discussion」** Commenters disagreed on deployment: ramses0 praised the post&\#x27;s privilege-dropping details and noted busybox&\#x27;s built-in CGI support, while brainless preferred a long-running, stateful Rust/SQLite backend over nginx invoking a binary per request. asimpleaspossi reported running a FastCGI-based C web business for years, and OleksandrC shared a separate C++/WebAssembly game project as another unusual web architecture.

<details><summary>References</summary>
<ul>
<li><a href="https://zeli.app/story/50058528">A Modern Web App in C · 153 HN comments | Zeli</a></li>
<li><a href="https://upstract.com/x/ff7e87d60c67529f">A Modern Web App in C - upstract.com</a></li>

</ul>
</details>

**Tags**: `#C`, `#web applications`, `#systems programming`, `#deployment`, `#privilege separation`

---

<a id="item-tech-news-7"></a>
### [Codex CLI installs a persistent self-updating daemon by default](https://github.com/openai/codex/issues/48195) ⭐️ 7.0/10

A Hacker News discussion and linked GitHub issue report that OpenAI&\#x27;s Codex CLI installs a persistent, self-updating background daemon by default for users. Commenters point to a feature flag, \`daemon\_auto\_start = false\` under \`\[features\]\` in \`~/.codex/config.toml\`, to prevent the daemon from starting automatically, though one poster notes there was no documented setting and describes pid and lock files written to \`~/.codex\`. User reports include roughly 12 GB of disk use from old versions and an auto-update bug that changed permissions so \`.git\` became read-only; these complaints are anecdotal and not independently verified.

hackernews · whimblepop · Oct 12, 18:29 · [Discussion](https://news.ycombinator.com/item?id=50060694)

**「Background」** Codex CLI&\#x27;s daemon auto-start became the stable default in v0.157.0, a change reported on September 25, 2026 that replaced the earlier per-session behaviour; the exec-server can still be invoked explicitly with \`codex exec-server\`, and the auto-start behaviour is configured in \`~/.codex/config.toml\`. Coverage of the same change describes the daemon as updating itself hourly and as being able to interrupt active agent turns, which is the behaviour users are now objecting to.

**「Impact」** Developers who install Codex CLI globally via npm receive the background daemon without an install-time prompt, and the only described way to stop it is an edit to \`~/.codex/config.toml\` setting \`daemon\_auto\_start = false\` under \`\[features\]\` — which commenters say is an undocumented feature flag. Leaving it enabled has been reported to accumulate old versions \(one user measured roughly 12 GB on disk\) and, in one account, to change file permissions during auto-update until \`.git\` became read-only and blocked the agent&\#x27;s task; these are individual user reports rather than confirmed vendor behavior.

**「Community Discussion」** Commenters debated whether the daemon&\#x27;s default behavior is acceptable: one said such persistence is expected when running a client but can be alarming for an NPM-installed CLI, while another recommended a bare-bones harness called hax over what they described as overengineered tools. A separate commenter reported many daemon bugs, including auto-updates that randomly ruined permissions and blocked goals when \`.git\` became read-only.

<details><summary>References</summary>
<ul>
<li><a href="https://codex.danielvaughan.com/2026/09/25/codex-cli-daemon-auto-start-stable-default-v0157/">Daemon Auto-Start Is Now the Stable Default in Codex CLI v0 ...</a></li>
<li><a href="https://elsolitario.org/en/2026/10/12/codex-cli-daemon-auto-start-opt-in-en/">Codex CLI Daemon: Why Users Want It Opt-In - elsolitario.org</a></li>
<li><a href="https://github.com/openai/codex">GitHub - openai/ codex : Lightweight coding agent that runs in your...</a></li>

</ul>
</details>

**Tags**: `#Codex CLI`, `#background daemon`, `#AI coding agents`, `#developer tooling`, `#privacy/security`

---

<a id="item-tech-news-8"></a>
### [LineageOS 24.0 released, rebased onto Android 17](https://lwn.net/Articles/1099950/) ⭐️ 7.0/10

LineageOS has released version 24.0, rebasing its Android-based distribution for mobile devices onto the Android 17 codebase that Google released in June. The project says it had been rebasing its changes and features since that release, and that prior work adapting to Google&\#x27;s refactoring across recent versions let it complete the move faster than anticipated. The same announcement notes that LineageOS will mark its 10-year anniversary on December 24, 2026. The supplied announcement excerpt does not list supported devices, build availability, or a rollout schedule.

rss · LWN.net · Oct 12, 13:13

**「Background」** LineageOS is a community-built Android distribution that must rebase its custom features and device support onto each new Android release. Android 17 shipped in June, and LineageOS says work adapting to Google&\#x27;s previous refactoring let it rebase onto the Android 17 codebase faster than expected. The 24.0 release also precedes the project&\#x27;s 10-year anniversary on December 24, 2026.

**「Who Gets It」** Devices officially supported on Linux 4.4 or 4.9 kernels are not moving to LineageOS 24 and remain on LineageOS 22.2 under the project&\#x27;s security-support policy, so users of those older builds should not expect the Android 17 rebase. The release also introduces browser-based WebUSB flashing, letting users on supported devices install builds directly from a browser rather than relying solely on a host-side utility.

<details><summary>References</summary>
<ul>
<li><a href="https://www.androidsage.com/2026/10/12/lineageos-24-released-based-on-android-17-in-browser-webusb-flashing-canvas-photo-editor-and-kernel-overhauls/">LineageOS 24 Released: Android 17 Features &amp; WebUSB</a></li>
<li><a href="https://easternherald.com/2026/10/12/lineageos-24-android-17-browser-flashing/">LineageOS 24 Adds Android 17 and Browser Flashing Tools</a></li>

</ul>
</details>

**Tags**: `#LineageOS`, `#Android`, `#open source`, `#mobile OS`, `#custom ROM`

---

<a id="item-tech-news-9"></a>
### [Looped Diffusion Transformer reuses blocks per denoising step, loop depth set at sampling time](https://www.reddit.com/r/MachineLearning/comments/1x49d61/looped_diffusion_transformer_the_same_blocks_run/) ⭐️ 7.0/10

The Looped Diffusion Transformer \(arXiv 2609.40305, posted 30 Sep\) proposes running a shared group of transformer blocks several times inside each denoising step of a text-to-image DiT instead of making the model bigger. The authors report that naive looping does not reliably help and address this with deep supervision on every loop plus self-modulating attention; they claim a 260M looped model beats a model 6.5x larger on several benchmarks using 4.9x less inference compute, and that at a fixed inference budget more loop depth helps more than more denoising steps. The Reddit author ran a small independent reproduction of the MIT-licensed B/16 code and Hugging Face weights \(published under sensenova\) on an M5 Pro using PyTorch MPS in fp32, 100 Euler steps, CFG 6.0, and one seed per prompt at loop depths 1 through 4, finding most of the change occurred before depth 3 and that depths 3 and 4 were very close on all five prompts shown, with roughly 23-24 seconds per image at depth 1 versus 43-47 seconds at depth 4. That loop depth can be changed at sampling time without retraining is the authors&\#x27; and README&\#x27;s claim, supported here only by this small single-machine run rather than peer-reviewed or independent benchmarking.

reddit · r/MachineLearning · /u/Fit-Ant2238 · Oct 12, 18:13

**「Background」** Looped-DiT builds on MiniT2I, a pixel-space denoiser based on the MMDiT architecture, which the authors chose as a backbone because its simple training pipeline provides a controlled setting for studying loop depth. Conventionally, text-to-image diffusion transformers gain quality by adding unique parameters or running more denoising evaluations; the looped approach instead repeatedly reuses a subset of transformer blocks within each denoising step.

**「Impact」** Because the B/16 code and weights are released under MIT and loop depth is chosen at sampling time, users can download the checkpoint and trade latency for refinement per image without retraining—in the author&\#x27;s MPS run, an image took roughly 23–24 seconds at depth 1 versus 43–47 seconds at depth 4, with depths 3 and 4 nearly indistinguishable across the five prompts shown. Practitioners optimizing throughput should therefore expect diminishing returns past depth 3 on these prompts and test depth before assuming a quality gain, since the observation is a single-seed reproduction on one machine rather than a validated default. The paper&\#x27;s headline claim—that a 260M looped model surpasses a model 6.5x larger across multiple text-to-image benchmarks at 4.9x lower inference compute, under matched-parameter and matched-compute settings—remains the authors&\#x27; reported result, not independently confirmed here.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2609.40305">[ 2609 . 40305 ] Looped Diffusion Transformer</a></li>
<li><a href="https://arxiv.org/html/2609.40305">Looped Diffusion Transformer</a></li>
<li><a href="https://www.alphaxiv.org/abs/2609.40305">Looped Diffusion Transformer | alphaXiv</a></li>
<li><a href="https://arxiv.org/abs/2609.40305">[2609.40305] Looped Diffusion Transformer - arXiv.org</a></li>
<li><a href="https://github.com/OpenSenseNova/Looped-DiT">GitHub - OpenSenseNova/Looped-DiT: PyTorch implementation of ...</a></li>

</ul>
</details>

**Tags**: `#diffusion models`, `#transformer architecture`, `#efficient inference`, `#text-to-image`, `#model replication`

---

<a id="item-tech-news-10"></a>
### [Anthropic reports 90–99% drop in distilled Claude data](https://www.anthropic.com/research/distillation-defenses) ⭐️ 7.0/10

Anthropic said on October 12 that preliminary evidence shows its new defenses against model-distillation attacks reduced extracted Claude capability data by roughly 90% to 99%. The company said it banned tens of thousands of accounts tied to such attacks, some within two hours of the activity starting. The measures include restricting inference content from moving across sessions, models, and accounts, plus a two-stage classifier and ongoing patching of bypass techniques; Anthropic reports a false-positive rate below 0.1%. Some developers will need to update their integrations, and blocked requests may still be billed.

telegram · zaihuapd · Oct 13, 01:25

**「Background」** Model distillation is a method of training a smaller model on outputs from a larger one; without permission, AI providers treat it as model extraction and an abuse of API access. Anthropic&\#x27;s new defenses, described in the source, are aimed at accounts that use the Claude API for this kind of bulk capability extraction.

**「Impact」** Anthropic says some developers must update their integrations because the defenses restrict how reasoning content moves across conversations, models, and accounts, and third-party coverage of the rollout frames the change as a required developer migration rather than a transparent backend fix. Anthropic also states that requests blocked by the new classifier may still be billed, so even a sub-0.1% false-positive rate can cost developers money without producing a usable response.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/research/distillation-defenses">Strengthening our defenses against distillation attacks</a></li>
<li><a href="https://www.explainx.ai/blog/anthropic-distillation-defenses-preserved-thinking-classifier-90-99-percent-2026">Anthropic Distillation Defenses: 90-99% Less Data Stolen ...</a></li>

</ul>
</details>

**Tags**: `#AI security`, `#model distillation`, `#Anthropic`, `#Claude API`, `#model extraction`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Fed&\#x27;s Hammack says restrictive policy may be needed to curb inflation](https://www.cnbc.com/2026/10/12/beth-hammack-fed-inflation-policy.html) ⭐️ 8.0/10

Cleveland Fed President Beth Hammack said Monday that a restrictive monetary policy stance is appropriate to ensure a timely return to the central bank&\#x27;s 2% inflation target, implying further interest rate hikes remain possible. The Fed&\#x27;s preferred price gauge, the core personal consumption expenditures index, was 3% higher than a year earlier in August, and traders priced a nearly 88% chance of a rate hike at the Fed&\#x27;s December meeting, according to CME&\#x27;s FedWatch tool.

rss · CNBC Finance · Oct 13, 02:58

**「Background」** The Fed raised rates last month for the first time in three years, and minutes from its September meeting indicated officials could vote to raise them again without specifying when; Hammack is a voting member of the committee that sets rates.

**「Impact」** If rates rise again as traders now largely expect, households and businesses carrying variable-rate debt such as credit cards and loans would face higher borrowing costs while inflation remains above the Fed&\#x27;s 2% goal.

**Tags**: `#Federal Reserve`, `#Monetary policy`, `#Inflation`, `#Interest rates`, `#Central bank communication`

---

<a id="item-finance-news-2"></a>
### [China to Cut NEV Export VAT Rebate From 13% to 9% in 2027](https://www.news.cn/20261012/9709731f470b42f9a84825c2e4eb914b/c.html) ⭐️ 8.0/10

China&\#x27;s Ministry of Finance and State Taxation Administration announced on October 12 that the value-added tax export rebate rate for new energy vehicles will be lowered from 13% to 9% effective April 1, 2027, and that VAT export rebates for e-cigarette devices will be cancelled. The notice, reported by Xinhua, adds that consumption tax refund or exemption policies for affected products subject to consumption tax remain unchanged.

telegram · zaihuapd · Oct 12, 11:00

**「Background」** An export VAT rebate refunds Chinese exporters the value-added tax already paid on goods they sell abroad, which effectively lowers their selling price overseas. This cut scales back that support as NEV exports have become a key driver of the industry&\#x27;s growth, according to cnevpost.

**「Impact」** With new energy vehicles making up more than half of China&\#x27;s vehicle exports in July 2026 \(553,000 units\), the cut trims the refund Chinese exporters receive on each vehicle sold abroad, leaving them to absorb the cost, raise prices or shift further toward overseas production.

<details><summary>References</summary>
<ul>
<li><a href="https://cnevpost.com/2026/10/12/china-cuts-nev-export-tax-rebates/">China cuts NEV export tax rebates, testing profitability of ...</a></li>
<li><a href="https://chinaevhome.com/2026/08/12/chinas-new-energy-vehicle-sales-share-tops-60-for-first-time-in-july/">China &#x27;s New Energy Vehicle Sales Share Tops 60... | ChinaEVHome</a></li>

</ul>
</details>

**Tags**: `#China NEV exports`, `#export tax rebates`, `#fiscal policy`, `#automotive industry`, `#e-cigarettes`

---

<a id="item-finance-news-3"></a>
### [China and EU reach consensus on hybrid, EV trade; China&\#x27;s quota to be no lower than other import sources](https://www.mofcom.gov.cn/xwfb/sjfzrfb/art/2026/art_4d502e1d49fd4480b39a6cfd0d752038.html) ⭐️ 7.0/10

China&\#x27;s Ministry of Commerce said China and the EU reached several consensuses on hybrid and electric vehicle trade, including that China&\#x27;s quota will be no lower than that granted to the EU&\#x27;s other import sources; the hybrid arrangement will use 2025 as its baseline and rise from there, with no specific quota figure disclosed. The ministry said both sides affirmed respect for facts, non-discrimination and compliance, and that China retains its right to pursue dispute settlement under World Trade Organization rules, while the EU will continue with company price-undertaking and other review procedures for electric vehicles.

telegram · zaihuapd · Oct 12, 06:19

**「Background」** The EU had imposed anti-subsidy tariffs on Chinese electric vehicles, and in January 2026 the two sides moved to a price-undertaking framework setting minimum import prices instead of those tariffs, according to later trade reporting \(tool-1-2, tool-1-3\). The current talks extend the discussion to hybrid vehicles, using 2025 as the baseline for the arrangement.

**「Impact」** Chinese automakers exporting hybrids and electric vehicles would keep access to the EU market on terms no worse than those of other foreign suppliers, although the actual volumes depend on quota levels that have not been published.

<details><summary>References</summary>
<ul>
<li><a href="https://informedclearly.com/en/trade-war/57721/eu-china-ev-price-floor-trade-2026">EU-China EV Price Floor: Redrawing Global Trade Rules in 2026</a></li>
<li><a href="https://informedclearly.com/en/trade-war/62505/eu-china-ev-price-floor-trade-deal-2026">EU-China EV Price Floor: 2026 Global Trade Truce Explained</a></li>

</ul>
</details>

**Tags**: `#China-EU trade`, `#electric vehicles`, `#hybrid vehicles`, `#trade policy`, `#auto industry`

---

<a id="item-finance-news-4"></a>
### [China&\#x27;s new tax penalty benchmark takes effect Nov 1, adding employer social-insurance arrears](https://fgk.chinatax.gov.cn/zcfgk/c100012/c5252754/content.html) ⭐️ 7.0/10

China&\#x27;s State Taxation Administration issued Announcement No. 20 of 2026, publishing the National Tax Administrative Penalty Discretion Benchmark \(2026 Edition\), effective November 1, 2026, which adds employers&\#x27; overdue or underpaid social-insurance contributions to the penalty items — fines are tiered by the amount and share of arrears and can reach 3 times the unpaid amount, but only after an employer fails to pay within a deadline set by order, and the employer must also repay the arrears plus a daily late fee of 0.05% \(万分之五\); the authority said the benchmark cannot be used on its own as the basis for a penalty, and violations committed before the effective date generally follow the rules then in force.

telegram · zaihuapd · Oct 13, 02:45

**「Background」** A tax penalty discretion benchmark is a nationwide standard that guides tax authorities in choosing a fine amount within the range already set by the underlying law; the announcement states it cannot by itself serve as the legal basis for a penalty, and violations committed before 1 November 2026 are generally judged under the rules in force at the time.

**「Impact」** Employers that fall behind on employee social insurance and fail to pay within the deadline set by tax authorities face up to three times the unpaid amount plus a daily late fee, raising the cost of non-compliance for Chinese firms; their workers&\#x27; unpaid contributions would still have to be made up.

**Tags**: `#税务处罚`, `#社保欠缴`, `#裁量基准`, `#企业合规`, `#中国政策`

---