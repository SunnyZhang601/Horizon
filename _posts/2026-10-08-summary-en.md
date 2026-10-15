---
layout: default
title: "Horizon Summary: 2026-10-08 (EN)"
date: 2026-10-08
lang: en
---

> Data source: Horizon (24h window; **Measured** — 199 items crawled → 128 items passed the 7.0 threshold).
> This window is **extremely single-source skewed**: of the 128 qualifying items, about 123 come from arXiv cs.RO (robotics / embodied AI preprints, all noted below), and only 5 are non-arXiv (GPT-6 / Claude Haiku 5.5 / Hamilton obituary / RP2040 VGA / TikTok dataset / NVIDIA review controversy).
> **`Embedded.com` and the EE/IC direction have no independent qualifying items**, explicitly flagged in Section 2, not padded.
> Each item is tagged with its evidence nature (Estimated / Author's claim / Measured / Assistant inference / To be verified), applied consistently throughout.

## 1. Top Stories

1. **OpenAI releases GPT-6, touting "an intelligent UI everyone can use"** ⭐️ 9.0/10
   [Official blog](https://openai.com/index/gpt-6-for-everyone/) · ([Community discussion](https://news.ycombinator.com/item?id=49996425))
   OpenAI released GPT-6 along with an interaction layer called Intelligent UI, where answers can compose text, visuals, and interactive components on demand. The HN thread has 709 points / 415 comments. Community relay of the system card (`gpt-6-october.pdf`) claims GPT-6 Sol / Luna showed a statistically significant regression versus GPT-5.6 on standard self-harm and other safety evaluations. (**Author's claim** + community relay; original details not verifiable)

2. **Anthropic releases Claude Haiku 5.5** ⭐️ 8.0/10
   [Official](https://www.anthropic.com/claude-haiku-5-5) · ([Community discussion](https://news.ycombinator.com/item?id=49996437))
   Uses a 100k-token boundary pricing scheme: below it $0.10 / $0.50 per million tokens, above it jumps to $0.50 / $2.50 (the boundary applies to Haiku only). Plotly's DataAnalyticsBench shows it is 9x cheaper than Haiku 4.5 while improving scores by two letter grades. (**Author's claim** + third-party benchmark)

3. **Apollo software pioneer Margaret Hamilton dies** ⭐️ 8.0/10
   [MIT News](https://news.mit.edu/2026/margaret-hamilton-computing-pioneer-dies-1007) · ([Community discussion](https://news.ycombinator.com/item?id=49998895))
   She led the onboard flight software team for the Apollo Guidance Computer and coined the term "software engineering"; she was 90 (1936-08-17 – 2026-09-30). The HN thread has 1931 points / 213 comments. (**Measured** — the obituary source is MIT News official)

4. **OpenAI retracts several AI-generated math papers** ⭐️ 8.0/10
   [GitHub change history](https://github.com/openai/math/blob/main/history.md) · ([Community discussion](https://news.ycombinator.com/item?id=50003107))
   On 10-06, 722 internally model-generated math manuscripts were publicly released (with formalized proofs and change logs); the next day 3 were pulled down after errors were found. The discussion touched on the risk of Lean formalization "compiling but not matching semantics" and on the infeasibility of human review. (**Author's claim** + community relay)

5. **AI solving only ~5% of long-unsolved math problems sparks controversy** ⭐️ 8.0/10
   [Scott Aaronson blog](https://scottaaronson.blog/?p=10169) · ([Community discussion](https://news.ycombinator.com/item?id=49997718))
   Per community citations, a model was tested on roughly 8000 open math problems, solving only about 5% with single ~3-hour attempts; one comment roughly estimated ~60 hours of compute per solved problem. The paper's writing quality was questioned. (**Estimated** + **To be verified** — both the 5% and the 60 hours are back-of-envelope community-comment estimates; proof validity unconfirmed)

6. **Terence Tao on how, in the AI era, math progress needs to be measured more holistically** ⭐️ 7.0/10
   [Original Mastodon post](https://mathstodon.xyz/@tao/117395269325940185) · ([Community discussion](https://news.ycombinator.com/item?id=50002008))
   Terence Tao proposed "Math 2.0", arguing that math progress should not be measured by benchmarks like "how many open problems solved", and that verification burden and actual contribution should weigh more. The HN thread has 482 points / 470 comments. (**Author's claim**)

7. **Workhorse: learning humanoid whole-body loco-manipulation from human data** ⭐️ 8.0/10
   [arXiv preprint](https://arxiv.org/abs/2610.09117)
   Learns directly from human-only demonstrations without robot teleoperation or motion retargeting; a visual planner predicts the poses of five links (torso / both wrists / both feet), and an RL whole-body tracker follows them. On a real Unitree G1 it completed tidying boxes, catching and tossing a box, and knocking over then climbing onto a suitcase; in simulation the box-tidying success rate was 77%, dropping to 64% under 40 N·s of push force. (**Author's claim**)

8. **RoboJEPA: scaling laws for latent world models across 12 robot embodiments** ⭐️ 8.0/10
   [arXiv preprint](https://arxiv.org/abs/2610.10515)
   Trained on large-scale real-robot data covering 12 embodiments, it finds that "imagination error" falls as a second-order power law with compute and strongly correlates with downstream planning performance, making it a proxy metric for real-robot evaluation; 8B parameters, checkpoints, and deployment code are all open-sourced. (**Author's claim**)

9. **World models become a covert poisoning entry point in the robot learning supply chain** ⭐️ 8.0/10
   [arXiv preprint](https://arxiv.org/abs/2606.09499)
   Injects malicious prompts / harmful transition dynamics into **ostensibly safe** teleoperation datasets that activate only after world-model processing, generating dangerous synthetic trajectories and forming an end-to-end backdoor into downstream DRL policies; a proof of concept is given for the VLA setting. (**Author's claim** — preprint, no real deployment impact demonstrated yet)

10. **Rubix: a new method for global alignment of point sets without correspondences** ⭐️ 8.0/10
    [arXiv preprint](https://arxiv.org/abs/2610.10408)
    Uses "permutohedral polygon" geometry to give a globally optimal solution for equal-weight planar Procrustes-Wasserstein alignment, proves a tight bound of n(n−1) vertices, and answers Rote's rotation-assignment open problem; on MPEG-7 shapes it averages 12 ms and is 50x faster than rotation-grid methods at equal accuracy. (**Author's claim**)

11. **An amateur OS driving 640×480 VGA on RP2040 with no framebuffer** ⭐️ 7.0/10
    [Community discussion (r/embedded)](https://www.reddit.com/r/embedded/comments/1x028y1/rp2040_driving_640480_vga_without_a_framebuffer/)
    Because 640×480×8-bit needs 300 KB while the RP2040 has only 264 KB of SRAM, the project uses no framebuffer at all: display data is stored as 34 KiB blocks, and core 1 software-composites each scanline just before PIO fetches it (8008 cycles per line budget at 252 MHz); keyboard / mouse go through a second RP2040, with events embedded in a 1 Mbaud UART as tagged frames. **The only qualifying embedded item in this window.** (**Author's claim** — self-reported in the original Reddit post)

12. **NVIDIA DreamDojo paper said to be erroneous yet accepted as ICML spotlight** ⭐️ 7.0/10
    [Community discussion (r/MachineLearning)](https://www.reddit.com/r/MachineLearning/comments/1x0i6b5/nvidias_erroneous_paper_accepted_as_icmls/)
    The allegation says the robot world-model paper reports only about 0.5 dB PSNR improvement yet used roughly 44k hours of human data + 256 H100s for pretraining; the poster says a colleague, using Claude, found a bug in the post-training code that invalidated all post-training code, and found two more bugs affecting pretraining in the GitHub issues. **The allegations come from a Reddit discussion, are independently unverified, and ICML has not responded.** (**Community allegation** + **To be verified**)

13. **560 million TikTok video metadata records published to Hugging Face** ⭐️ 7.0/10
    [Community discussion (r/MachineLearning)](https://www.reddit.com/r/MachineLearning/comments/1x04235/uploaded_56_billion_tiktok_videos_metadata_on/)
    Contains a creator table of 4.5 billion rows / a video table of 5.6 billion rows / an audio table of 633 million rows, spanning 2014 – October 2026; the author self-hosts ClickHouse for queries. No data collection methodology details are provided. (**Author's claim**)

## 2. Deep Dives (Robotics · Embedded · EE/IC · AI)

### Robotics

- **Three tactile / contact-force perception items in a row this window, each on a different path** (all **Author's claim**, arXiv preprints)
  - **SAFE** ([2610.08802](https://arxiv.org/abs/2610.08802)): two passive PVDF **acoustic** sensors + motor proprioception, no vision and no prior material knowledge; a unified classifier outputs three states — normal / slip / crush; leave-one-grasp-out cross-validation gives Alert-F1 0.884, with confusion between slip and crush near zero; the controller runs at 104 Hz on a Jetson Orin Nano, and 46 closed-loop trials gave 91.3% success, 82.4% on unseen objects.
  - **Soft optical tactile online estimation of contact force and task frame** ([2610.10020](https://arxiv.org/abs/2610.10020)): maps a single image of elastomer deformation to indentation depth, two tilt angles, and 3D contact force (with uncertainty), fuses it with proprioception in an EKF, and continuously updates the task frame; on UR10 + DigiTac it achieves closed-loop contact force regulation **using touch alone**. The cost is assuming the contact is locally planar and contact torques are negligible.
  - **Visible Touch** ([2609.14156](https://arxiv.org/abs/2609.14156)): **renders contact signals into the same spatial frame as vision**, so any image-conditioned policy can use touch without architecture changes; on LIBERO BC-Transformer gains +15.7 pp, and when fine-tuning VLAs miniVLA gains +25 pp and π0.5 gains +30 pp on four contact-rich real-robot tasks.

- **Dexterous grasp stability: the value of high-resolution dynamic touch, quantified** ([2610.10283](https://arxiv.org/abs/2610.10283), **Author's claim**)
  With a multi-finger hand fitted with 4 Digit 360 tactile sensors, 10000 grasps were collected across 200 objects to train an end-to-end temporal multimodal model that predicts post-lift stability from **pre-lift** observations; ablations show that adding high-resolution dynamic touch does help; once deployed as an online "lift / regrasp" gate, the success rate on unseen objects is 10.5 pp higher than with a no-touch gate. The dataset is public.

- **Humanoid whole-body control: two paths from human demos to real hardware** (both **Author's claim**, arXiv preprints)
  - **Workhorse** ([2610.09117](https://arxiv.org/abs/2610.09117)): visual planner + RL tracker, with the two policies **independently trained separately** on the same batch of human poses, no motion retargeting, and each injecting the other's deployment errors as augmentation during training.
  - **ResGAC** ([2610.09479](https://arxiv.org/abs/2610.09479)): geometric admittance control (GAC) provides structured SE(3) task-space feedback and produces nominal joint position targets, while residual RL compensates unmodeled dynamics and coordinates balance in a **shared joint position action space**; a left-invariant geometric formulation lets it use a ground-fixed heading frame and remove pelvis roll/pitch/height disturbances. On a real Unitree G1 it beats baselines including SONIC on four standing end-effector tracking benchmarks, with peg-in-hole assembly success at 90% (SONIC 50%).

- **Joint control and execution timing: two lightweight "don't touch the policy, change only the downstream" methods** (both **Author's claim**, arXiv preprints)
  - **PHRetune** ([2610.05755](https://arxiv.org/abs/2610.05755)): **offline**, derives the stiffness and damping gains of the downstream **impedance controller** for a frozen policy — learning a port-Hamiltonian model from demos, estimating effort and energy budgets, then giving a single gain scaling in **closed form** after comparison against demos; no rollouts, no prior arm model, no retraining needed. On LIBERO Diffusion Policy gains up to +9.4 pp, on four real tasks it beats both the nominal policy and empirical gain sweeps, and it reduces the VLA backbone's acceleration and jerk.
  - **RoboPace** ([2610.09696](https://arxiv.org/abs/2610.09696)): online re-times action chunks without changing the geometric path, adjusting execution speed by predicted contact state (slowed by actuator/tracking limits at contact, yet faster in free space), with no policy retraining; on three contact-rich dual-arm tasks, four of five instructions finished in about half the time with higher overall success.

### Embedded

- **RP2040 no-framebuffer VGA OS** ([Community discussion](https://www.reddit.com/r/embedded/comments/1x028y1/rp2040_driving_640480_vga_without_a_framebuffer/), **Author's claim**)
  Already expanded in Top Stories item 11. The engineering trade-offs are worth recording: **out of memory → skip the framebuffer and composite scanlines in real time**, with worst-case boot benchmarks done on silicon; plus a real pitfall hit along the way — a cheap 5 V microSD module keeps driving MISO even when not selected, corrupting touch readings; a 3.3 V adapter board fixed it.
- The remaining embedded sources (Embedded.com RSS with only 1 qualifying item, Hackaday etc.) produced **no independent above-threshold items** in this window. (**Measured**)

### EE/IC

- **No qualifying items this window** (**Measured** — no EE/IC-type candidate in the window passed the 7.0 threshold, not padded).
- *Note*: almost all qualifying items this window come from the single source arXiv cs.RO, and The Robot Report RSS still returns 403; this is **source skew**, not an indication that the field has no progress. (**Assistant inference**)

### AI

- **GPT-6 and Intelligent UI** ([Official blog](https://openai.com/index/gpt-6-for-everyone/), **Author's claim**) — answers can compose text / visuals / interactive components per question; free and Go users gain access gradually starting the next day. The "statistically significant regression" safety claim comes from a community relay of the system card, unverified against the original text.
- **Claude Haiku 5.5's pricing trap** ([Simon Willison measured test](https://simonwillison.net/2026/Oct/7/claude-haiku-5-5/), **Author's claim + first-hand measurement**) — within 100k tokens it matches GPT-6 Luna in price but scores higher on benchmarks; above that the price jumps 5x while Luna only rises to $0.20/$0.75 at 272k tokens; also measured that the same long prompt **costs about 1.25x more tokens** on the new model, a hidden price increase. **Conclusion framing**: comparing model prices requires checking tokenizer changes and tiered thresholds together.
- **VLA models are highly sensitive to instruction wording** ([2610.10526](https://arxiv.org/abs/2610.10526), **Author's claim**) — rephrasing rules can mitigate it; appeared in the same batch as mechanistic interpretability research on "whether VLAs truly understand instructions".
- **NVIDIA DreamDojo review controversy** (see Top Stories 12) — if the allegations hold, it directly affects world-model researchers building on its open-sourced code; but **independently unverified**.
- **560 million TikTok video metadata records** (see Top Stories 13) — an unprecedented-scale social media metadata resource, but the collection methodology is undisclosed and ClickHouse credentials must be requested via comments.
