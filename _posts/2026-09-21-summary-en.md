---
layout: default
title: "Horizon Summary: 2026-09-21 (EN)"
date: 2026-09-21
lang: en
---

> Data source: Horizon News Radar.
> This window had **27 candidates** (Hacker News 8 · Reddit 9 · RSS 10 · Telegram 0), **2** passed the 7.0 threshold; the shorter-than-usual length is due to the data sources.
> Each item is tagged with the nature of its source: **Estimated / Author's claim / Measured / Assistant inference**; items that cannot be judged are marked "To be verified".

## 1. Top Stories

1. **[Samsung to more than double HBM4 and HBM4E DRAM output](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say)** ⭐️ 7.0/10 — Sedaily reports that Samsung plans to more than double its output of HBM4 / HBM4E high-bandwidth memory for AI accelerators, citing "people familiar with the matter"; the report gives no specific capacity figures, timeline, or customers. (Source nature: **Author's claim** — media citing anonymous sources, no official confirmation; for the parallel discussion see [Community discussion](https://news.ycombinator.com/item?id=49778029))

2. **[Qwen Image 2.1: 7B open-weights text-to-image model released](https://qwen.ai/blog?id=qwen-image-2.1)** ⭐️ 7.0/10 — Parameter count shrinks from the previous generation's 20B to 7B (32-layer Single-Stream DiT), with native 2K resolution and transparent-background (RGBA) output, and ComfyUI native support available on release day; community attention focuses on the **license being stricter than previous Qwen models**, which may restrict commercial use and redistribution. (Source nature: **Author's claim** — parameters and capability items come from the vendor blog; generation-quality comparisons are community self-testing, **To be verified**)

## 2. Deep Dives (Robotics · Embedded · EE/IC · AI)

### Robotics

**0 items in this window.** The arXiv Robotics (cs.RO) feed was crawled normally, but no items passed the 7.0 threshold within the 24-hour window; of this round's 3 hits on Reddit r/robotics, none qualified either. This is a consequence of the data-source structure, not padded.

### Embedded

**0 items in this window.** This round Reddit r/embedded had 4 hits and Hackaday 7, none of which qualified in the firmware, RTOS, driver, or MCU toolchain directions; Embedded.com was crawled normally but produced no qualifying items.

### EE/IC

**Samsung HBM4 / HBM4E capacity expansion** — [Sedaily original](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say)

- **Analysis**: HBM (high bandwidth memory) is high-performance memory built by vertically stacking multiple DRAM dies with through-silicon vias (TSV) and co-packaging it with accelerators such as GPUs; it is a key companion component of today's AI accelerators. The point of this item is not the "doubling of output" figure itself (media citing anonymous sources, **Author's claim, To be verified**), but the supply-structure change it points to: Samsung has previously lagged SK Hynix in HBM and is trying to catch up with HBM4 / HBM4E — according to outside reporting it also plans to raise monthly HBM wafer capacity from about 170,000 wafers to about 250,000 by the end of 2026 (roughly +47%, **Author's claim, To be verified**), which requires freeing up space at its Cheonan campus in South Chungcheong Province and migrating some legacy DRAM and NAND lines out. **Assistant inference**: as memory makers' capacity tilts from standard DRAM toward HBM, the effect will first show up in the supply and price of general-purpose storage, then propagate downstream into whole-device BOMs — this layer of causality is the key to connecting the news to hardware work, but it is my inference based on the report's structure, not the report's own conclusion. The community raised two further points (both **Author's claim**, unverified): the economic viability of wafer-thinning processes at scale is in doubt; and the real bottleneck for Chinese AI accelerators may be CXMT's HBM capacity, not processor chips or ASML equipment.
- **Sources**: [Sedaily original](https://en.sedaily.com/finance/2026/09/20/samsung-to-double-hbm4-output-next-year-sources-say) · [Community discussion](https://news.ycombinator.com/item?id=49778029)

### AI

**Qwen Image 2.1 — miniaturization and license tightening for open-weight text-to-image** — [Original](https://qwen.ai/blog?id=qwen-image-2.1)

- **Analysis**: Three points worth recording. ① **Miniaturization**: the visual generation component is only 7B parameters (32-layer Single-Stream DiT) versus 20B for the previous Qwen-Image 1, and the same track also has the smaller Z-Image Turbo (6B) — on this basis the community treats "open-weight image models are getting smaller" as a trend. ② **Capability items**: generation and editing are integrated into a single model, with native 2K resolution and direct RGBA image output when generating transparent content; the community considers the transparent background a direction few have handled seriously, and text rendering (especially small-type fidelity) is rated clearly ahead in the open-weight market (source nature: **Author's claim** — from community self-testing, N=1, **To be verified**). ③ **License tightening**: previous Qwen models mostly used permissive licenses such as Apache, while 2.1 switches to a stricter license that may restrict commercial use and redistribution — this is the most contested point in this round's discussion, and the recurring "capabilities get stronger, terms get tighter" combination in community comments.
- **Sources**: [Qwen blog](https://qwen.ai/blog?id=qwen-image-2.1) · [Community discussion](https://news.ycombinator.com/item?id=49775499) · [ComfyUI support](https://blog.comfy.org/p/qwen-image-21-in-comfyui-open-weight) · [Hugging Face weights](https://huggingface.co/Qwen/Qwen-Image-2.1)
