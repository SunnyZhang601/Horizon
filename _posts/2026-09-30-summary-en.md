---
layout: default
title: "Horizon Summary: 2026-09-30 (EN)"
date: 2026-09-30
lang: en
---

> Coverage window: 2026-09-29 ~ 2026-09-30. Data source: Horizon News Radar.
> This crawl **227 items → 164 items passed the 7.0 threshold** (**Measured**).
> ⚠️ **This window has extremely heavy single-source skew**: of the 164 qualifying items, **160 come from arXiv cs.RO** (**Measured**, counted item by item), with only 4 non-arXiv items (OpenAI official / BBC / Hackaday / a personal project site).

---

## 1. Top Stories

1. **OpenAI releases GPT 6.1 Sol: cached input price cut by 50%** ([OpenAI official](https://openai.com/index/introducing-gpt-6-1-sol/) · [Community discussion](https://news.ycombinator.com/item?id=49896586)) ⭐️ 8.0/10
   Officially, cached input drops to **$0.10 / million tokens**, 95% below standard input and 50% below GPT-6 Sol's cached price; the community broadly agrees that **the price cut itself is the core of this release**, while doubting whether quality has improved over the previous generation, and some users say they have switched to competitors. (**Author's claim**: pricing and tiers; **Community relay**: quality dispute and switching to competitors)

2. **FineART: densely annotated bimanual manipulation dataset and VLA model** ([arXiv:2609.36416](https://arxiv.org/abs/2609.36416)) ⭐️ 8.0/10
   The dataset contains 40,543 episodes / 1,718 hours / 533,913 subtasks, and the model can self-predict the next subtask and train mid-episode accordingly; the paper reports spatial disambiguation success rising 32.0%→100.0% and 16.0%→76.0% on unseen long-horizon tasks, with data and weights open-sourced. (**Author's claim**, preprint, pending independent verification)

3. **CrossBFM: a latent behavior space shared across humanoids** ([arXiv:2609.38087](https://arxiv.org/abs/2609.38087)) ⭐️ 8.0/10
   Uses frame-level cross-morphology correspondences provided by retargeting to train a unified encoder, compressing behavior-space training from hundreds of GPU hours to under 1 GPU hour; on unseen robots it can recover up to 89% of the tracking performance of seen robots. (**Author's claim**)

4. **Rho: an open-source dual-arm manipulation VLA model that adapts efficiently** ([arXiv:2609.38164](https://arxiv.org/abs/2609.38164)) ⭐️ 8.0/10
   Open weights + checkpoints for three platforms (YAM Box / UR AI Trainer / FR3 Duo), with built-in online adaptation; the paper claims about 15 correction episodes suffice to handle task situations on the edge of the fine-tuning distribution. (**Author's claim**)

5. **PRISM: counterfactual video generation extends humanoid training** ([arXiv:2609.38172](https://arxiv.org/abs/2609.38172)) ⭐️ 8.0/10
   First uses video-to-video generation to amplify a small set of real videos into hundreds of "counterfactual" human-interaction clips, then retargets them into physically feasible trajectories via a contact-anchored real-to-sim pipeline; no real-world fine-tuning was done at deployment. (**Author's claim**)

6. **MAVLN: formalization and benchmark for multi-agent vision-language navigation** ([arXiv:2609.35965](https://arxiv.org/abs/2609.35965)) ⭐️ 8.0/10
   First formalizes multi-agent VLN as a coordination problem with dependency and resource constraints (presence locks / holding chains), releasing a 145-scenario / 11,724-episode benchmark and the coordination system TRISS. (**Author's claim**)

7. **iTeach: mixed-reality interactive robot perception correction system** ([arXiv:2410.09072](https://arxiv.org/abs/2410.09072)) ⭐️ 8.0/10
   On-site personnel wearing an MR headset correct segmentation failures; each roughly 20-second interaction yields 150–300 densely annotated frames; the paper reports segmentation performance 26.1→80.7 with no catastrophic forgetting, and in a 12-person user study non-expert annotations reached about 95% box IoU. (**Author's claim**)

8. **Disc-shaped magnetostrictive torque sensor for robot joints** ([arXiv:2609.33542](https://arxiv.org/abs/2609.33542)) ⭐️ 7.0/10
   Axial packaging about **1 cm**, a four-magnetometer architecture suppresses parasitic lateral forces, and custom magnetic shielding reduces external stray fields to 1/7 of the original; torque accuracy **1.34 %FS** at 50 Nm full scale. (**Author's claim**; the paper does not address production consistency or long-term reliability)

9. **A 17-DoF dexterous manipulator driven by bidirectional antagonistic tendons** ([arXiv:2609.36241](https://arxiv.org/abs/2609.36241)) ⭐️ 7.0/10
   Human-hand scale **200 mm / 220 g**, 3D-printed; bidirectional antagonistic tendon routing lets joints cross the neutral position with no passive return springs; **transmission error 3.0%, transmission bandwidth 13.2 Hz, max fingertip force 29 N, repeatability up to 0.15 mm**, completing all 33 GRASP Taxonomy grasps. (**Author's claim**)

10. **FINGR: real-world Rubik's cube solving with a single dexterous hand** ([arXiv:2609.33973](https://arxiv.org/abs/2609.33973)) ⭐️ 7.0/10
    Represents the cube's point cloud with each fingertip as reference; future tokens are supervised at multiple timescales on contact force changes, layer-turn progress, and joint displacements; **99.0%** success over 300 layer-turn attempts (79.7% for the base flow policy), solving ten 2×2×2 cubes in about 137 seconds. (**Author's claim**)

11. **Vermont replaces peaker plants with household batteries** ([BBC Future](https://www.bbc.com/future/article/20260928-a-virtual-power-plant-hidden-in-vermont-homes-is-keeping-the-lights-on-during-storms) · [Community discussion](https://news.ycombinator.com/item?id=49897993)) ⭐️ 7.0/10
    A virtual power plant (VPP) aggregates customer-side home batteries to participate in grid dispatch; the report says the project's capacity has reached **110 MW**, making it the state's largest single power resource by capacity, and has already led to the shutdown of two peaker plants. (**Community relay** of the Electrek report it cites; the BBC original not verified item by item)

12. **Dutch government reportedly dropping Windows for Linux** ([Hackaday](https://hackaday.com/2026/09/29/no-more-windows-for-the-dutch-government-its-linux-all-the-way/)) ⭐️ 7.0/10
    Project name DAWO; plans to replace Windows with a NixOS-based desktop; the report says it involves about **30,000** local-government devices, with eight municipalities already participating in testing. (**Author's claim**; the Hackaday original is only a lead paragraph, details come from other reports it cites, and the government's own account is unverified)

13. **Real-time solar system visualization: 526,000 asteroids and satellites** ([space.bl2.net](https://space.bl2.net/) · [Community discussion](https://news.ycombinator.com/item?id=49898778)) ⭐️ 7.0/10
    WebGL2 renders the solar system in the browser in real time at true scale, containing about 526,000 asteroids/comets and every CelesTrak-tracked satellite, with orbit propagation running in web workers and data updated daily; the community marveled that half-a-million-scale objects can already run at over 60 fps in the browser. (**Author's claim**: data scale and technical implementation; **Community relay**: performance experience)

---

## 2. Deep Dives (Robotics · Embedded · EE/IC · AI)

### 🤖 Robotics (this window's focus: joint sensing / dexterous hands / force control and touch)

**1. Direct joint torque sensing: compacting the magnetostrictive approach**
([arXiv:2609.33542](https://arxiv.org/abs/2609.33542) ⭐️ 7.0/10)
The disc-shaped magnetostrictive structure compresses axial size to about 1 cm, fitting exactly into joint assembly space that is tight along the axis to begin with; the combination of four magnetometers + custom magnetic shielding shows that the engineering difficulty of this class of designs has always been **rejecting stray fields**, not sensitivity itself (stray fields drop to 1/7 after shielding). The paper's figure is 1.34 %FS at 50 Nm full scale — **an author's claim**, with no account of production consistency or long-term drift.

**2. Dexterous hand hardware: the bidirectional antagonistic tendon's "cross-the-neutral-position" capability**
([arXiv:2609.36241](https://arxiv.org/abs/2609.36241) ⭐️ 7.0/10)
The key design decision is **replacing passive return springs with active actuation**, letting every degree of freedom cross the neutral position, so the same hand can close into a grasp from both the palmar and dorsal sides without rotating the wrist or changing arm pose. The engineering metrics given (transmission error 3.0%, bandwidth 13.2 Hz, fingertip force 29 N, repeatability 0.15 mm) amount to a complete **benchmarkable checklist** at the 220 g / 3D-printed scale.

**3. Force control and touch: three works in the same direction, pointing to "force should be an action, not an observation"**
- **FP2** ([arXiv:2609.37433](https://arxiv.org/abs/2609.37433) ⭐️ 7.0/10): does not decouple the task policy; it only attaches a high-frequency force-control downstream interface, preserving the foundation model's action-generation capability.
- **Wrench-ACT** ([arXiv:2609.37552](https://arxiv.org/abs/2609.37552) ⭐️ 7.0/10): makes the wrench the **only** action output, handed directly to a pure force controller, instead of outputting target poses.
- **TacForcing** ([arXiv:2608.25798](https://arxiv.org/abs/2608.25798) ⭐️ 7.0/10): replaces action-chunk experts with streaming experts; after execution, new tactile feedback resumes generation from the interrupted state, avoiding "stale within-chunk tactile conditioning".

**4. HACo: the complementarity of fingertip touch and joint torque**
([arXiv:2609.36596](https://arxiv.org/abs/2609.36596) ⭐️ 7.0/10)
Uses fingertip local tactile responses and **joint torque feedback** simultaneously, on the grounds that the latter captures loads transmitted through the multi-joint hand that run outside the coverage of fingertip touch; the paper reports 83% vs 35% for the strongest baseline.

**5. Exploration in dexterous manipulation and real-world benchmarks**
- **ContactExplorer** ([arXiv:2603.10971](https://arxiv.org/abs/2603.10971) ⭐️ 7.0/10): represents contact as the intersection of "object surface points × hand keypoints" and counts it, driving exploration with contact-coverage rewards; the paper claims it is effective across **five dexterous hand embodiments**, reducing reliance on task-specific priors.
- **FINGR** ([arXiv:2609.33973](https://arxiv.org/abs/2609.33973) ⭐️ 7.0/10): continuous Rubik's cube turning with a single dexterous hand, 99.0% success over 300 layer-turn attempts — a real-world benchmark for contact-rich manipulation.
- **Unified vision-tactile-action model** ([arXiv:2609.34182](https://arxiv.org/abs/2609.34182) ⭐️ 7.0/10): builds a tactile motion-capture system and the UVTA dataset (1,000 human demonstrations + 150 robot demonstrations per task), transferring the physics regularities of human tactile data to robots; average success 70% across five task categories (strongest vision-tactile baseline 29%).

**6. ⚠️ One easily misread point (Assistant inference + original checked)**
In **FACT's "articulated twin"** ([arXiv:2609.37067](https://arxiv.org/abs/2609.37067) ⭐️ 7.0/10), *articulated twin* refers to **articulated objects** (everyday objects with revolute joints such as drawers, cabinet doors, and scissors), **not the robot's joints**. The original text is entirely about "object geometry/contact/dynamics fidelity". **Do not read it from the title as a joint-modeling work.**

### 🔌 Embedded

**No standalone qualifying items this window; not padded.** Basis (**Measured**):
- Embedded.com had only **1 item** this window, which did not pass the 7.0 threshold;
- Of Hackaday's **7 items**, only "the Dutch government switching to Linux" passed (7.0), but that item is an **IT governance / digital sovereignty** topic, not an embedded technology item, so it was placed in "Top Stories" rather than this section.

### ⚡ EE/IC

**No standalone qualifying items this window; not padded.** Basis (**Measured**): of the 164 qualifying items, **160 are arXiv cs.RO**, with the rest being AI pricing, energy, and IT governance topics; the only one with electrical/device character is the magnetostrictive torque sensor (leaning mechatronics and sensors), already filed in the Robotics subsection; the Vermont home batteries belong to **power systems/energy storage**, also not an EE/IC design item.

### 🧠 AI

**1. The cost line of coding workflows moves down another notch**
([OpenAI official](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 8.0/10)
Cached input at $0.10 / million tokens is the change that truly matters this time; "officially positioned close to higher-tier models at one-fifth the price" is an **Author's claim**, and the community's disagreement over quality is **community relay**.

**2. RLE-Bench: turning "can coding agents do robotics engineering" into an exam**
([arXiv:2609.34210](https://arxiv.org/abs/2609.34210) ⭐️ 7.0/10)
48 tasks, four workflow classes (interactive control / policy learning / perception and estimation / **mechanical design**), requiring building, integrating, diagnosing, and improving heterogeneous artifacts under resource budgets, aggregated into a 0–100 RLE Index.

**3. Survey of robot in-context learning: four classes of interfaces**
([arXiv:2609.36012](https://arxiv.org/abs/2609.36012) ⭐️ 7.0/10)
Divided along "contextual evidence → execution" into: context-conditioned policies / geometric demonstration transfer / world-model-based control / skill- and agent-based execution; it also stresses evaluating "responsiveness to teaching" separately from "real gains of physical transfer".

**4. CrossBFM: treating the "latent behavior space" itself as a transferable asset**
([arXiv:2609.38087](https://arxiv.org/abs/2609.38087) ⭐️ 8.0/10)
The idea is not to train a model per robot but to make the **space itself** shared across morphologies; the cost claim is a drop from hundreds of GPU hours to under 1 hour. (**Author's claim**)

---
