---
layout: default
title: "Horizon Summary: 2026-10-16 (EN)"
date: 2026-10-16
lang: en
---

> From 73 items, 9 important content pieces were selected

---

**Technology News**
1. [Neural networks self-assemble learning machinery from local plasticity rules](#item-tech-news-1) ⭐️ 8.0/10
2. [Meta releases open-weight Muse Spark Open 816B-A42B model](#item-tech-news-2) ⭐️ 7.0/10
3. [Goodfire&\#x27;s &\#x27;Neural networks are clean&\#x27; claim sparks interpretability debate](#item-tech-news-3) ⭐️ 7.0/10
4. [Citizen Lab links Discover Tech to zero-click spyware via targeted ads](#item-tech-news-4) ⭐️ 7.0/10
5. [Libreboot 26.10 &quot;Ominous Olive&quot; adds UEFI and Chromebook support](#item-tech-news-5) ⭐️ 7.0/10
6. [Seven Linux stable kernels fix critical networking vulnerability](#item-tech-news-6) ⭐️ 7.0/10
7. [Anthropic tells investors Q3 revenue hit $16.8bn ahead of IPO](#item-tech-news-7) ⭐️ 6.0/10
8. [Android kernel vendor hooks discussed at Linux Plumbers Conference](#item-tech-news-8) ⭐️ 6.0/10
9. [Custom Controller And YOLO Vision Add Motion Tracking To Soonpho M7](#item-tech-news-9) ⭐️ 6.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Neural networks self-assemble learning machinery from local plasticity rules](https://www.reddit.com/r/MachineLearning/comments/1x6hmyg/how_artificial_neural_networks_build_their_own/) ⭐️ 8.0/10

A Reddit post highlights a PNAS paper published 9 October 2026 and covered by MIT News on 13 October reporting that randomly interconnected neuron-like units governed by shared plasticity rules can self-assemble learning motifs and learn pattern recognition and image classification, with performance similar to the backpropagation-trained networks tested. The authors caution that this self-organization does not establish that the brain uses the mechanism, and the work is motivated by biological plausibility rather than evidence of a replacement for backpropagation in large-scale models. Open questions include the stability of the motifs under different initial connectivity and whether the approach extends beyond the demonstrated tasks.

reddit · r/MachineLearning · /u/Dorian182 · Oct 15, 10:01

**「Background」** The backdrop is that machine-learning networks can already learn without detailed instructions from a designer, and the MIT report presents the new study as asking whether that learning machinery can arise from local plasticity rules alone rather than being specified up front. Coverage of the PNAS paper describes the self-assembled motifs, once stacked into a hierarchy, as settling into dynamics that approximate a generalized form of stochastic gradient descent — the error-reducing method that would otherwise have to be built into the network&\#x27;s design.

<details><summary>References</summary>
<ul>
<li><a href="https://allatra.media/science/science-self-assembling-synapses-gradient-learning">The Learning Circuit Nobody Had to Design | ALLATRA Media</a></li>
<li><a href="https://news.mit.edu/2026/how-artificial-neural-networks-build-their-own-learning-machinery-1013">How artificial neural networks build their own learning machinery</a></li>

</ul>
</details>

**Tags**: `#artificial neural networks`, `#self-organization`, `#backpropagation`, `#synaptic plasticity`, `#computational neuroscience`

---

<a id="item-tech-news-2"></a>
### [Meta releases open-weight Muse Spark Open 816B-A42B model](https://research.meta.ai/blog/muse-spark-open) ⭐️ 7.0/10

Meta published Muse Spark Open 816B-A42B, an open-weight mixture-of-experts model, on Hugging Face with deployment documentation and coverage describing it as optimized to run on Mac Studio. Deployment support is unusually broad: a commenter notes Meta&\#x27;s docs cover runners from Unsloth to MLX, and the model can be run locally rather than only through a hosted API. According to a commenter&\#x27;s reading of the license, use is unrestricted except for providing model outputs to third parties as a &quot;Model as a Service&quot; via API or similar interface when the licensee and its affiliates exceed $20 million in aggregate gross revenue. Early comparisons cited in the discussion place it below competing open models, so the release is notable more for its permissive deployment surface than for benchmark leadership.

hackernews · bigwheels · Oct 15, 17:47 · [Discussion](https://news.ycombinator.com/item?id=50107379)

**「Background」** Muse Spark Open is a sparse mixture-of-experts model: of its 816 billion total parameters, only 42 billion are active per token, so per-token compute is closer to that of a much smaller dense model while the full weights still carry the model&\#x27;s capacity. It is published under Meta&\#x27;s own Muse Model License rather than a permissive open-source license, and OpenRouter lists it as a model tuned specifically for agentic coding workflows, with a 1M-token context window. AMD provided day-0 support with both full-precision and Quark-exported MXFP4 builds.

**「Impact」** Developers who can run the model locally gain a widely supported open-weight option through common runtimes, but the license clause described by a commenter means organizations above the $20 million revenue threshold cannot offer Muse Spark Open as a hosted API product — so teams planning a commercial inference service should verify the license terms before building on it.

**「Community Discussion」** Commenters disagreed over the &quot;open weight&quot; label, with one reading the license as permissive apart from the Model-as-a-Service revenue clause, while another argued Artificial Analysis data shows the model underperforming Qwen3.8 Flash Next and GLM 5.3 Flash, which can run on a single B300. One commenter also criticized Artificial Analysis for comparing models only at the highest reasoning level, which they said is largely unusable for high-volume production workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/meta-models/Muse-Spark-Open-816B-A42B">meta - models / Muse - Spark - Open - 816 B - A 42 B · Hugging Face</a></li>
<li><a href="https://www.amd.com/en/developer/resources/technical-articles/2026/day-0-support-for-meta-muse-spark-open-on-amd.html">Day 0 Support for Muse Spark Open on AMD</a></li>
<li><a href="https://openrouter.ai/meta/muse-spark-open">Muse Spark Open - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**Tags**: `#open-weight models`, `#large language models`, `#mixture-of-experts`, `#model licensing`, `#Meta`

---

<a id="item-tech-news-3"></a>
### [Goodfire&\#x27;s &\#x27;Neural networks are clean&\#x27; claim sparks interpretability debate](https://already-clean.goodfire.com/) ⭐️ 7.0/10

Goodfire has published a blog post, &\#x27;Neural networks are clean&\#x27; \(already-clean.goodfire.com\), arguing that neural networks are more interpretable than expected and that mechanistic interpretability is more tractable than the post&\#x27;s author once believed. Hacker News commenters identify the author as Nick Cammarata, who says he co-authored early mechanistic-interpretability work at OpenAI and came away pessimistic because networks appeared messy. The claim is an author/vendor argument rather than an independently verified result; the provided item links to a Twitter/X thread and the blog but does not include the underlying technical evidence.

hackernews · themgt · Oct 15, 16:04 · [Discussion](https://news.ycombinator.com/item?id=50105647)

**「Background」** Goodfire, the company behind the post, has built Ember, a platform that decodes individual neurons to give researchers programmable access to a model&\#x27;s internal features, and it raised a $50M Series A to commercialize this interpretability work \(tool-2-2\). The post argues that neural networks are more interpretable than previously assumed, challenging the prior view that they resist clean interpretation.

**「Community discussion」** Commenters largely challenged the strength of the claims: bluejay2387 argued the post overreaches what is proven, noting that progressive feature complexity and the Lottery Ticket Hypothesis have long been known and are not mutually exclusive with parameter overloading, and cited the Multimodal Gap paper as evidence networks tend toward condensed representations. antics described the post as a massive evidentiary brief for &\#x27;sequencing the AI genome,&\#x27; while dleeftink questioned whether a neuron&\#x27;s genesis and outside context can be captured by its weights alone.

<details><summary>References</summary>
<ul>
<li><a href="https://menlovc.com/perspective/leading-goodfires-50m-series-a-to-interpret-how-ai-models-think/">Leading Goodfire ’s $50M Series A to Interpret How AI Models Think</a></li>

</ul>
</details>

**Tags**: `#mechanistic interpretability`, `#AI safety`, `#neural networks`, `#AI alignment`, `#deep learning`

---

<a id="item-tech-news-4"></a>
### [Citizen Lab links Discover Tech to zero-click spyware via targeted ads](https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/) ⭐️ 7.0/10

Citizen Lab published research alleging that Discover Tech, an Israeli firm, turned targeted advertising infrastructure into a pipeline for delivering zero-click spyware to mobile devices, with The Guardian and The Verge reporting on the finding on October 15, 2026. The allegation is Citizen Lab&\#x27;s own research characterization rather than a vendor admission, independent verification, or a disclosed software patch. The report raises mobile security and adtech accountability concerns, but it does not detail the exact mechanism by which the malware is said to execute without any user interaction.

hackernews · jcomp · Oct 15, 10:43 · [Discussion](https://news.ycombinator.com/item?id=50101813)

**「Prerequisite context」** Citizen Lab&\#x27;s investigation links previously documented Candiru mercenary spyware infections at Al Jazeera to targeted advertisements that triggered attacks without any user click. The report names Discover-Tech as the company operating this ad-based delivery and command-and-control infrastructure, and labels the technique AdFection, describing it as the first public confirmation of zero-click mercenary spyware distributed through targeted ads.

**「Impact」** Citizen Lab&\#x27;s report ties the campaign to ad infrastructure spanning more than 70,000 apps and 120,000 sites, giving app developers and publishers that embed third-party ad SDKs a concrete supply-chain item to audit: the ad slot itself becomes the infection path, so no user click is needed. The Register describes this as the first publicly confirmed case of zero-click delivery through ads, which shifts the practical burden toward ad-network vetting and mobile platform controls rather than user caution.

**「Community Discussion」** An engineer with roughly 13 years in adtech called the report &quot;highly sensationalist&quot; on the zero-click point, saying it describes distribution and command-and-control but stays vague about what actually activates the malware without user action, and argued that the term &quot;ad provider&quot; misrepresents a sprawling ecosystem rather than naming a single accountable party. Other commenters debated whether Israeli cybersecurity firms can be treated as independent of the state, an assertion stated as opinion rather than evidence.

<details><summary>References</summary>
<ul>
<li><a href="https://citizenlab.ca/research/how-discover-tech-turned-targeted-ads-into-a-pipeline-for-spyware/">Exposing AdFection: How Discover-Tech Turned Targeted Ads ...</a></li>
<li><a href="https://thehackernews.com/2026/10/citizen-lab-traces-zero-click-candiru.html">Citizen Lab Traces Zero-Click Candiru Spyware Infections at ...</a></li>
<li><a href="https://tech-insider.org/adfection-spyware-ad-networks-2026/">AdFection Spyware Hit 70,000 Apps via Ads [2026]</a></li>
<li><a href="https://www.theregister.com/security/2026/10/15/spyware-vendors-found-a-way-to-make-targeted-ads-even-worse/5303334">Spyware vendors found a way to make targeted ads even worse</a></li>

</ul>
</details>

**Tags**: `#cybersecurity`, `#spyware`, `#adtech`, `#zero-click exploit`, `#mobile security`

---

<a id="item-tech-news-5"></a>
### [Libreboot 26.10 &quot;Ominous Olive&quot; adds UEFI and Chromebook support](https://libreboot.org/news/libreboot2610.html) ⭐️ 7.0/10

Libreboot 26.10, codenamed &quot;Ominous Olive,&quot; has been released with UEFI/EDK integration and Chromebook support. According to a quoted release note in the discussion, it imports all 233 currently supported Chromebooks from the MrChromebox coreboot distribution, with Baytrail \(Kip\) tested and other devices still needing testing. The release is source-only, so users must build it themselves; no binaries are provided.

hackernews · iamnothere · Oct 15, 12:52 · [Discussion](https://news.ycombinator.com/item?id=50102923)

**「Background」** MrChromebox&\#x27;s coreboot distribution already provides firmware images for the vast majority of x86-based Chromebooks and Chromeboxes, using edk2 as the payload to supply a modern UEFI bootloader. That is the codebase Libreboot&\#x27;s new release draws on: it imports the Chromebook support from that distribution and adds its own UEFI/EDK integration, which is why the EDK payload and ChromeOS hardware appear together. MrChromebox firmware, and therefore the imported Chromebook targets, covers Intel/AMD x86\_64 platforms only, not ARM-based devices.

**「What it means for users」** Anyone with one of the roughly 233 imported Chromebook targets gains a possible Libreboot path, but this release is source-only with no binaries and only Baytrail \(&quot;Kip&quot;\) is reported as tested, so users of other models must build and validate the firmware themselves before flashing. The release also introduces an EDK II-based UEFI stack into a project that promotes itself on fully free firmware; EDK II is BSD-licensed, and commenters elsewhere have questioned whether it qualifies as free software \(tool-3-1\).

**「Community Discussion」** Commenters debated the release&\#x27;s strict LLM-contribution policy, with lf88 calling it refreshing and kyrra pointing to the linked AGENTS policy; iamnothere argued the UEFI/EDK integration and Chromebook support are the bigger technical step, saying it greatly expands Libreboot&\#x27;s device reach. cwiggs said the Chromebook work connects to ChromeOS ports being merged in the Heads project.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.mrchromebox.tech/docs/supported-devices.html">Supported Devices | MrChromebox .tech</a></li>
<li><a href="https://doc.coreboot.org/distributions.html">Distributions — coreboot 26.06-1170-gb34a744391b documentation</a></li>
<li><a href="https://news.slashdot.org/story/26/10/03/1713227/fsf-sponsors-gnu-boot-a-libre-ethical-replacement-for-nonfree-bios-or-uefi">FSF Sponsors &#x27;GNU Boot&#x27;, a Libre, Ethical Replacement for... - Slashdo...</a></li>

</ul>
</details>

**Tags**: `#Libreboot`, `#open-source firmware`, `#UEFI`, `#Chromebooks`, `#embedded systems`

---

<a id="item-tech-news-6"></a>
### [Seven Linux stable kernels fix critical networking vulnerability](https://lwn.net/Articles/1100611/) ⭐️ 7.0/10

Greg Kroah-Hartman announced seven Linux stable kernels — 7.2.11, 6.18.57, 6.12.113, 6.6.159, 6.1.190, 5.15.223, and 5.10.272 — each containing a fix for a critical networking vulnerability, CVE-2026-99999. The flaw is in skb\_checksum\_help\(\), where an IPv4 packet with bad checksum metadata could corrupt the network header and &quot;cause a bunch of mischief,&quot; according to patch author Michael S. Tsirkin. The source states the fix is one of several changes in the series and advises all users to upgrade, but gives no root-cause analysis, exploit details, or independent verification.

rss · LWN.net · Oct 15, 13:01

**「Background」** skb\_checksum\_help\(\) is the kernel helper invoked when a packet&\#x27;s checksum must be completed in software instead of by hardware offload; the Linux kernel&\#x27;s checksum-offload documentation describes it as the point at which the true checksum is filled in, so a defect there operates on packet headers directly. CVE-2026-99999 is being fixed through the stable-tree backport process, which is why the same patch appears across seven separate releases covering the 5.10 through 7.2 lines.

**「Impact」** Users on any of the seven affected kernel series must move to the corresponding release to obtain the CVE-2026-99999 fix; because the same patch was prepared for all seven branches, administrators of long-term kernels from 5.10 through 6.1 have an upgrade available within their existing series rather than needing to change major version.

<details><summary>References</summary>
<ul>
<li><a href="https://www.kernel.org/doc/html/v5.6/networking/checksum-offloads.html">Checksum Offloads — The Linux Kernel documentation</a></li>

</ul>
</details>

**Tags**: `#linux-kernel`, `#security-vulnerability`, `#stable-releases`, `#networking`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [Anthropic tells investors Q3 revenue hit $16.8bn ahead of IPO](https://simonwillison.net/2026/Oct/15/anthropic-tells-investors/) ⭐️ 6.0/10

Anthropic told investors on Wednesday that quarterly revenue rose to $16.8bn in Q3 \(July–September\), up from $11.5bn in Q2 and about $4.8bn in Q1, according to Financial Times reporting summarized by Simon Willison. The same briefing cited $1.70 of revenue for every $1 spent on computing power and adjusted operating margins of 11% excluding stock-based compensation. Anthropic also said distillation — rivals training models on its outputs — accounted for 5% to 7% of revenue and that it had cut that contribution back &quot;materially&quot; in Q3. These are figures Anthropic gave to investors, not audited results, and the source does not detail how the crackdown is enforced.

rss · Simon Willison · Oct 15, 13:04

**「Background」** Anthropic&\#x27;s investor briefings come ahead of an initial public offering: the company filed a confidential draft S-1 registration statement with the SEC on June 1, 2026, after a Series H funding round that set a $965 billion post-money valuation. As of late September and early October 2026 reporting, no official IPO date or price had been announced, though the investor roadshow was reported as potentially starting the week of November 9.

**「Impact」** Labs that train models on Anthropic&\#x27;s outputs lose a path that, by Willison&\#x27;s arithmetic from the 5%–7% figure, was worth over half a billion dollars in a single quarter before the Q3 cutback — meaning affected teams face higher data-acquisition costs or must shift to alternate sources. Separately, Anthropic&\#x27;s shift away from &quot;annualized run-rate revenue&quot; toward these quarterly figures changes how investors can compare its disclosed growth with earlier communications.

<details><summary>References</summary>
<ul>
<li><a href="https://tastytrade.com/learn/markets/industry/anthropic-ipo/">Anthropic IPO 2026: Date, Valuation &amp; Timeline</a></li>
<li><a href="https://admiralmarkets.com/education/articles/shares/anthropic-ipo">Anthropic IPO 2026: Expected Date and Valuation - Admirals</a></li>
<li><a href="https://www.zacks.com/featured-articles/761/anthropic-ipo">Anthropic IPO 2026 Guide: Price Predictions, Dates, and ...</a></li>

</ul>
</details>

**Tags**: `#ai-industry`, `#anthropic`, `#business`, `#ipo`, `#model-distillation`

---

<a id="item-tech-news-8"></a>
### [Android kernel vendor hooks discussed at Linux Plumbers Conference](https://lwn.net/Articles/1098493/) ⭐️ 6.0/10

At the 2026 Linux Plumbers Conference, Todd Kjos led a session in the Android track on kernel vendor hooks, the mechanism Android prefers for carrying the out-of-tree changes that its kernels still require. The talk covered how those hooks are used to manage modifications that have not been merged into mainline Linux, even as Android&\#x27;s shift to the generic kernel image has brought it closer to mainline. The session was an explanatory overview of existing practice, not an announcement: the report gives no new hook interfaces, kernel versions, or availability dates.

rss · LWN.net · Oct 15, 15:09

**「Background」** Android kernels have long diverged from mainline through a layered fork model: Google forks Linux into an &quot;Android common&quot; kernel, and SoC vendors such as Qualcomm, Samsung, and MediaTek then fork that base into chip-specific kernels. The Generic Kernel Image initiative was meant to shrink that divergence by moving hardware-specific code into modules, and vendor hooks remain the sanctioned mechanism for vendor functionality that cannot be pushed upstream.

<details><summary>References</summary>
<ul>
<li><a href="https://arstechnica.com/gadgets/2021/09/android-to-take-an-upstream-first-development-model-for-the-linux-kernel/">Android to take an “upstream first” development model for the Linux ...</a></li>
<li><a href="https://www.classcentral.com/course/youtube-can-mainline-linux-run-on-android-without-vendor-hooks-qais-yousef-271934">Free Video: Can Mainline Linux Run on Android Without Vendor ...</a></li>

</ul>
</details>

**Tags**: `#Android kernel`, `#Linux kernel`, `#vendor hooks`, `#open source`, `#Linux Plumbers Conference`

---

<a id="item-tech-news-9"></a>
### [Custom Controller And YOLO Vision Add Motion Tracking To Soonpho M7](https://hackaday.com/2026/10/15/building-an-m7-pan-tilt-head-controller/) ⭐️ 6.0/10

Maker Kyle Housley has built a custom controller and a YOLO-based vision system to give the consumer Soonpho M7 pan tilt head live motion tracking it does not provide out of the box. The setup aims a camera automatically at moving subjects instead of relying on the head&\#x27;s stock remote-control operation. The available write-up is a short Hackaday teaser, so the microcontroller used, the electrical interface to the M7, the tracking performance, and any code or build details are not described.

rss · Hackaday · Oct 15, 08:00

**「Background」** The Soonpho M7 is an off-the-shelf motorized pan-tilt head used for time-lapse and remote camera aiming; product listings describe 360-degree horizontal rotation, a 52-degree tilt range, eight adjustable rotation speeds, and a built-in battery rated for more than six hours with Type-C charging \(tool-1-1, tool-1-2\). It supports setting the angle and number of shots per interval and can trigger the camera shutter automatically for time-lapse sequences \(tool-1-3\).

**「Impact」** For owners of the M7 or comparable consumer pan tilt heads, the project illustrates that subject tracking can be added without buying a higher-end head, but because the teaser omits the control interface, firmware, and parts list, anyone reproducing it must first determine how the custom controller drives the M7.

<details><summary>References</summary>
<ul>
<li><a href="https://www.newegg.com/p/3C6-038N-03DW2">Soonpho M 7 Time-Lapse Motorized Tripod Head ... - Newegg.com</a></li>
<li><a href="https://tech-troves.com/products/soonpho-m7-time-lapse-motorized-tripod-head-b0gr9ybv7w">Soonpho M 7 Time-Lapse Motorized Tripod Head - One-Touch...</a></li>
<li><a href="https://www.amazon.com/Motorized-Rotating-Panoramic-Camcorders-Smartphones/dp/B0F59XV42N">Soonpho M 7 Motorized Rotating Panoramic Tripod Head for Time Lapse</a></li>

</ul>
</details>

**Tags**: `#embedded systems`, `#computer vision`, `#YOLO`, `#hardware hacking`, `#pan-tilt control`

---