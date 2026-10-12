---
layout: default
title: "Horizon Summary: 2026-10-12 (EN)"
date: 2026-10-12
lang: en
---

> From 33 items, 8 important content pieces were selected

---

**Technology News**
1. [Terence Tao&\#x27;s Math 2.0 Slides Prompt Debate on AI in Mathematics](#item-tech-news-1) ⭐️ 8.0/10
2. [Critique Argues Passkeys Create Platform Lock-In and Portability Problems](#item-tech-news-2) ⭐️ 7.0/10
3. [Compressed RoBERTa AI-text detector to 97 MB for in-browser ONNX inference](#item-tech-news-3) ⭐️ 7.0/10
4. [Sliced-Wasserstein embeddings and HNSW index for color-scheme search over 48k paintings](#item-tech-news-4) ⭐️ 7.0/10
5. [Shing-Tung Yau launches math and AI laboratory alliance at Tsinghua](#item-tech-news-5) ⭐️ 7.0/10

**Technology Blog**
1. [Software Engineers Don&\#x27;t Get to Be Luddites About AI](#item-tech-blog-1) ⭐️ 5.0/10

**Financial News**
1. [Foreign investors withdraw about $131 billion from Korean stocks this year](#item-finance-news-1) ⭐️ 7.0/10
2. [中国商务部：中欧就混动与电动汽车贸易达成多项共识](#item-finance-news-2) ⭐️ 7.0/10

---

## Technology News

<a id="item-tech-news-1"></a>
### [Terence Tao&\#x27;s Math 2.0 Slides Prompt Debate on AI in Mathematics](https://teorth.github.io/tao-web/slides/math-2-0-caltech-2026.pdf) ⭐️ 8.0/10

The item is a Hacker News submission linking to Terence Tao&\#x27;s &quot;Math 2.0&quot; slide deck \(PDF\), which the item&\#x27;s analysis summary says addresses AI&\#x27;s growing role in mathematics. The supplied material does not include the slides themselves, so specific claims or proposals in the deck cannot be verified here. The accompanying Hacker News thread drew 421 comments, with participants debating AI-driven mathematical discovery, research culture, and domain expertise.

hackernews · Anon84 · Oct 11, 13:16 · [Discussion](https://news.ycombinator.com/item?id=50043026)

**「Background」** Tao&\#x27;s &quot;Math 2.0&quot; slides follow his earlier International Congress of Mathematicians 2026 public lecture and an August 2026 arXiv essay, both titled &quot;Mathematics in the Age of AI,&quot; which argued that mathematical research communities need a response to AI tools now capable of research-level work. In the blog post accompanying this talk, Tao describes a historical &quot;Math 1.0&quot; state of mathematics and a current phase shaped by what he characterizes as excessive emphasis on automated solving of open problems, against which he sets his &quot;Math 2.0&quot; vision of AI sustaining both the mathematical community and the role of mathematical understanding. The full text of the Caltech slides was not available in the source material, so the specific claims in the deck itself could not be verified here.

**「Community Discussion」** Commenters pushed back on Tao&\#x27;s cancer-medicine example: dekhn and squidmaster argued that medicine already uses treatments whose mechanisms are incompletely understood, so an effective AI-created drug might still be prescribed without full mechanistic understanding. thomasahle interpreted Tao&\#x27;s broader point as a software analogy—pure mathematics as a theory &quot;codebase&quot; that current math AI does not try to extend elegantly—while samuelknight relayed reports from researchers whose open problems were solved by AI, including rewritten grant proposals and a sense of loss.

<details><summary>References</summary>
<ul>
<li><a href="https://teorth.github.io/tao-web/slides/age-of-ai-icm-2026.pdf">Mathematics in the age of AI - Public lecture, International ...</a></li>
<li><a href="https://terrytao.wordpress.com/2026/10/10/math-2-0/">Math 2.0 | What&#x27;s new</a></li>
<li><a href="https://arxiv.org/pdf/2608.16753">MATHEMATICS IN THE AGE OF AI - arXiv.org</a></li>

</ul>
</details>

**Tags**: `#AI for mathematics`, `#Terence Tao`, `#mathematical research`, `#AI in science`, `#research culture`

---

<a id="item-tech-news-2"></a>
### [Critique Argues Passkeys Create Platform Lock-In and Portability Problems](https://nonfunctional.substack.com/p/passkeys-are-a-trap-do-not-use-them) ⭐️ 7.0/10

A Substack essay titled &quot;Passkeys are a trap,&quot; discussed on Hacker News, argues that passkeys — WebAuthn-based credentials offered as a password replacement — produce platform lock-in and portability problems, and it frames their spread as a trap for users. It is an opinion and analysis piece rather than a vendor announcement or an independently measured result, and no article text was supplied, so its specific claims could not be verified from the available material. Commenters add technical detail: attestation can only be required when a credential is registered, not retroactively at login, and browsers present a permission prompt when a site requests it \(agwa\); separately, some platforms restrict which authenticators they accept, with one commenter saying OpenAI requires hardware passkeys and appears to decide based on the device name reported \(bramhaag\).

hackernews · laurex · Oct 11, 21:59 · [Discussion](https://news.ycombinator.com/item?id=50048312)

**「Background」** Passkeys are digital credentials tied to a user account and a website or application, allowing users to authenticate without entering a username or password or providing an additional authentication factor. During credential registration, a relying party can request passkey attestation, which conveys information about the authenticator \(typically residing on the authenticator&\#x27;s TPM\) and can support device- or manufacturer-based restrictions.

**「Impact」** For developers and platform operators, the constraint agwa describes means attestation-based device restrictions have to be enforced at registration: WebAuthn cannot require attestation at login if it was never obtained, so a site that wants to exclude certain authenticators must reject the registration request up front rather than screen at sign-in. That limits how much device gating can be imposed after users have already enrolled.

**「Community Discussion」** bmitch3020 says they have never voluntarily enabled passkeys because they want portable credentials they can back up, lock away, and vary in strength per service, and they consider a phone thumbprint weaker than a long password in a password manager. danpalmer points out that the essay&\#x27;s own closing addendum footnote concedes passkeys are domain-bound and resistant to man-in-the-middle attacks — the security property the main argument otherwise downplays.

<details><summary>References</summary>
<ul>
<li><a href="https://developers.yubico.com/Passkeys/Passkey_relying_party_implementation_guidance/Attestation/">Attestation</a></li>
<li><a href="https://developers.google.com/identity/passkeys">Passkeys | Google for Developers</a></li>

</ul>
</details>

**Tags**: `#passkeys`, `#authentication`, `#security`, `#platform lock-in`, `#WebAuthn`

---

<a id="item-tech-news-3"></a>
### [Compressed RoBERTa AI-text detector to 97 MB for in-browser ONNX inference](https://www.reddit.com/r/MachineLearning/comments/1x3vqip/compressed_a_roberta_aitext_detector_from_500_mb/) ⭐️ 7.0/10

An open-source project, tinydetect, runs AI text and image detection entirely client-side in the browser through ONNX Runtime Web 1.30, using the WebGPU build when a GPU adapter is present and threaded WASM otherwise. The author compressed the Apache-2.0 fakespot-ai/roberta-base-ai-text-detection-v1 text detector from roughly 500 MB in fp32 to about 97 MB: a mixed-precision quantized transformer body of about 75 MB, plus the word embedding matrix stored as int4 with fp16 per-row scales \(about 19 MB plus 2 MB\) that is dequantized in JavaScript and passed to the transformer. The image detector is a quantized Community Forensics ViT \(commfor-model-384, MIT\) at about 26 MB. No new detectors were trained—the author reports light fine-tuning on a mix of human and AI text, WiSE-FT interpolation to keep the tuned weights from drifting too far from the original, and self-measured runtimes of about 60 ms for a ~100-token text check and about 200 ms for an image on their laptop.

reddit · r/MachineLearning · /u/Alternative\_Detail31 · Oct 12, 07:44

**「Background」** The project wraps two pre-existing open detectors rather than training new ones: Fakespot&\#x27;s RoBERTa-base AI-text detection model \(Apache-2.0\) and OwensLab&\#x27;s Community Forensics commfor-model-384 \(MIT\), a whole-image AI-generated-image detector trained on thousands of generators, with checkpoints released on Hugging Face and a paper presented at CVPR 2025. Because both base models already existed, the author&\#x27;s contribution is the tuning and deployment work — light fine-tuning, WiSE-FT interpolation between original and tuned weights, mixed-precision quantization, an int4 word-embedding matrix kept outside the ONNX graph, and a browser runtime built on ONNX Runtime Web.

**「Impact」** For anyone reusing this deployment, threaded WASM on GitHub Pages depends on a service worker that adds COOP/COEP headers, and the first load is a large download—the author flags this as especially heavy on phones—so the service worker&\#x27;s caching of the model and runtime files matters for repeat use. The author also states that a high score does not prove who wrote a text and that both models become less accurate on short or casual text, paraphrasing, heavy editing, screenshots, crops, and newer generators.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/fakespot-ai/roberta-base-ai-text-detection-v1">fakespot - ai / roberta - base - ai - text - detection - v 1 · Hugging Face</a></li>
<li><a href="https://huggingface.co/OwensLab/commfor-model-384">OwensLab/commfor- model - 384 · Hugging Face</a></li>
<li><a href="https://github.com/JeongsooP/Community-Forensics">GitHub - JeongsooP/ Community - Forensics : Project page: https...</a></li>

</ul>
</details>

**Tags**: `#model compression`, `#ONNX Runtime Web`, `#client-side ML`, `#AI-text detection`, `#quantization`

---

<a id="item-tech-news-4"></a>
### [Sliced-Wasserstein embeddings and HNSW index for color-scheme search over 48k paintings](https://www.reddit.com/r/MachineLearning/comments/1x39uu6/sliced_wasserstein_embeddings_hnsw_for/) ⭐️ 7.0/10

An independent developer published Palette Atlas, a color-scheme search tool for public-domain paintings built on a sliced-Wasserstein embedding plus a from-scratch HNSW index over 48,695 images. Each painting is reduced to 128 equal-weight OKLab colors, for which exact Earth Mover&\#x27;s Distance costs about 6 ms per pair, so the author projects colors onto 8 directions on a Fibonacci hemisphere, sorts, and averages into 16 quantiles, where L1 between vectors lower-bounds the true W1. On 240 queries, the sliced 8x16 L1 embedding matched 78% of the exact EMD top 10 with those neighbors 1.8% farther on average, versus 45%/13.5% for a soft color histogram under Hellinger distance and 3%/161% for mean color; the HNSW index \(M=16, efConstruction=200\) reports recall@10 of 1.000 at ef=32 in 0.25 ms against 14 ms for brute force. The design departs from the referenced paper by seeding the top layer with 8 k-means landmarks instead of random nodes, which the author reports leaves search cost essentially unchanged \(2,558 vs 2,556 distance computations on average\). These are self-reported numbers from a side project, not peer-reviewed or independently measured results.

reddit · r/MachineLearning · /u/Potential-Barber8658 · Oct 11, 14:39

**「Background」** Earth Mover&\#x27;s Distance — the 1-Wasserstein distance between color distributions — is the natural metric for comparing palettes, but exact computation is far too slow for pairwise nearest-neighbor search over tens of thousands of images. Sliced Wasserstein embeddings sidestep this by projecting colors onto a set of 1D directions, where the distance reduces to a closed-form L1 between sorted quantiles and serves as a lower bound on the true W1. HNSW is the standard layered-graph index for approximate nearest-neighbor search; the author cites Munyampirwa et al.&\#x27;s ICML 2025 oral &quot;Down with the Hierarchy&quot; on when that hierarchy stops paying off, a question directly relevant to the roughly 11-dimensional vectors used here.

**「Impact」** The reported tradeoff is concrete for anyone building similarity search over palette or distribution-shaped data: exact EMD at roughly 6 ms per pair is impractical across 48k items, and the sliced L1 embedding returns about 78% of the exact top 10, so roughly one in five exact nearest matches can be missed while query latency drops to 0.25 ms. The author also measures the embedding vectors&\#x27; intrinsic dimension at about 11 and notes this still leaves the HNSW hierarchy useful, citing Munyampirwa et al. 2025 on settings where it is not.

<details><summary>References</summary>
<ul>
<li><a href="https://icml.cc/virtual/2025/48994">ICML Oral 2: Down with the Hierarchy : The ‘H’ in HNSW Stands for...</a></li>

</ul>
</details>

**Tags**: `#Wasserstein distance`, `#HNSW`, `#image retrieval`, `#color palettes`, `#nearest-neighbor search`

---

<a id="item-tech-news-5"></a>
### [Shing-Tung Yau launches math and AI laboratory alliance at Tsinghua](https://www.beijing.gov.cn/fuwu/lqfw/gggs/202610/t20261012_4897748.html) ⭐️ 7.0/10

Fields medalist and Tsinghua University chair professor Shing-Tung Yau is leading a new Mathematics and Artificial Intelligence Laboratory Alliance, established at Tsinghua on October 11 with more than 1,000 scientists from multiple institutions and Yau as chairman. The alliance says it will develop China-specific large models for mathematics, build AI-assisted mathematical research infrastructure, and extend into quantum computing, life sciences, and finance and economics. Yau described AI&\#x27;s impact on mathematics as a tsunami that researchers should choose to surf rather than avoid. The announcement did not disclose funding, model specifications, timelines, or results, and no independent verification of the alliance&\#x27;s plans was provided.

telegram · zaihuapd · Oct 12, 03:00

**「Background」** Shing-Tung Yau is a Fields Medal-winning mathematician and a Tsinghua University chair professor. He has publicly described AI&\#x27;s impact on mathematics as being &quot;like a tsunami&quot; and argued that researchers should engage with it rather than avoid it, which frames the new alliance&\#x27;s focus on China-specific mathematics large models and AI-assisted mathematical research infrastructure, according to Beijing Daily and Lianhe Zaobao.

**「Impact」** Since the announcement specifies no model architecture, training data, license, or release date, developers cannot yet plan to integrate or benchmark the alliance&\#x27;s planned math model; the concrete comparison point in Chinese-language math AI remains existing open math-specialized models such as Qwen2.5-Math, which already targets Chinese and English math benchmarks using chain-of-thought and tool-integrated reasoning. Until the alliance publishes weights, an API, or evaluation results, its practical effect on developers is a stated intention rather than a usable capability.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/QwenLM/Qwen2.5-Math">GitHub - QwenLM/Qwen2.5-Math: A series of math-specific large ...</a></li>

</ul>
</details>

**Tags**: `#AI for mathematics`, `#large language models`, `#research alliance`, `#China AI`, `#Tsinghua University`

---

## Technology Blog

<a id="item-tech-blog-1"></a>
### [Software Engineers Don&\#x27;t Get to Be Luddites About AI](https://seangoedecke.com/software-engineers-dont-get-to-be-luddites-about-ai/) ⭐️ 5.0/10

rss · Sean Goedecke · Oct 12, 00:00

**「Background」** In this polemical essay, Sean Goedecke responds to software engineers who are angry that AI is automating their skills, arguing that they are the last people who should object. The article uses the history of Luddism and textile mechanization as its central analogy.

**「Solution」** Goedecke argues that software engineering has always automated other people&\#x27;s work: every commercial program takes over a task someone would otherwise pay a human to do. He notes that VisiCalc&\#x27;s creator worried about putting bookkeepers out of work, and lists industries software has displaced, including video rental stores, business directories and encyclopedias, typesetting, travel agencies, record stores, typing pools, data entry, and trading-floor runners. Engineers who adopt the Luddites as heroes misread the analogy, he says: the Luddites were displaced textile workers, while software engineers resemble the smiths and mechanics who built the power looms. Those mechanics were themselves automated away about fifty years later when unskilled &quot;illegal men&quot; could run the machines; their dispute was less violent and the striking engineers returned after four months when their money ran out, partly because they were seen as hypocrites—a Times quote called their cry like that of handloom weavers against inevitable laws. Goedecke further argues that software engineering&\#x27;s essence is replacing human labor with faster, cheaper machine labor, even if from the inside it feels like elegant puzzle-solving. He acknowledges the optimistic view of automation as progress is unfashionable today, citing climate change, the 2008 crash, social media&\#x27;s harms, and right-wing tech politics, and says he does not know which side is right, though he leans toward the Industrial Revolution being a net positive.

**「Takeaway」** Goedecke concludes that coming out against AI automation now is undignified and hypocritical: engineers who have participated in destroying or transforming other jobs should accept the same transformation of their own, or at least admit they want to pull the ladder up behind them.

**Tags**: `#AI and employment`, `#software engineering labor`, `#automation history`, `#technology ethics`, `#Luddism`

---

## Financial News

<a id="item-finance-news-1"></a>
### [Foreign investors withdraw about $131 billion from Korean stocks this year](https://m.gelonghui.com/live/2705107) ⭐️ 7.0/10

A Gelonghui report says foreign investors have net withdrawn about $131 billion \(roughly 876.7 billion yuan\) from Korean stocks so far this year. The KOSPI, Korea&\#x27;s benchmark stock index, has fallen about 22% in the second half, and market trading value is down 70% from its late-May peak.

telegram · zaihuapd · Oct 11, 12:13

**「Background」** The report attributes the selloff to the market&\#x27;s heavy reliance on Samsung Electronics and SK Hynix, two memory-chip makers; Samsung&\#x27;s foreign ownership has dropped to 46.38%, its lowest since the 2008 global financial crisis, even though Samsung&\#x27;s quarterly operating profit grew nearly tenfold year-on-year.

**Tags**: `#Korean stocks`, `#foreign outflows`, `#Samsung Electronics`, `#memory chips`, `#market concentration`

---

<a id="item-finance-news-2"></a>
### [中国商务部：中欧就混动与电动汽车贸易达成多项共识](https://www.mofcom.gov.cn/xwfb/sjfzrfb/art/2026/art_4d502e1d49fd4480b39a6cfd0d752038.html) ⭐️ 7.0/10

中国商务部表示，中欧在贸易投资磋商机制下就混动汽车和电动汽车贸易深入讨论并达成多项共识，其中混动汽车安排将以2025年为基准向上，中方配额不低于欧方其他进口来源地。电动汽车方面，商务部称欧方将继续推进企业价格承诺及其他复审程序，同时中方保留在世贸组织框架下的争端解决等权利。

telegram · zaihuapd · Oct 12, 06:19

**「Background」** In late October 2024, the EU imposed anti-subsidy duties of up to 35.3% on Chinese battery-electric cars, on top of a 10% base tariff—a barrier of up to 45.3% for five years—prompting Chinese automakers to shift exports toward plug-in hybrids that were then outside the tariff framework \(tool-1-2\). The EU’s goods trade deficit with China, which neared €360 billion in 2025, made those vehicle imports politically sensitive \(tool-1-3\).

**「Impact」** Chinese hybrid and EV exporters would keep EU market access no less favourable than other import sources, with duty relief available to individual manufacturers that agree minimum-price undertakings — a mechanism industry reporting illustrates with Volkswagen Anhui&\#x27;s arrangement, which lifted a 20.7% countervailing duty on CUPRA Tavascan exports \(tool-2-1\) — while European carmakers that compete with cheaper Chinese hybrids remain under pressure \(tool-2-2\).

<details><summary>References</summary>
<ul>
<li><a href="https://post.smzdm.com/p/anv9okk0/">post.smzdm.com/p/anv9okk0</a></li>
<li><a href="https://stom-vet.ru/manyvoices/read/news_ifeng_com_c_8x71vmgstto_4bde8184">中 欧 “各退一步”，开了一个好头 - ManyVoices</a></li>
<li><a href="https://www.chinaautosupplier.com/show_article-87647.html">chinaautosupplier.com/show_article-87647.html</a></li>
<li><a href="https://stom-vet.ru/manyvoices/read/news_ifeng_com_c_8x71vmgstto_4bde8184">中 欧 “各退一步”，开了一个好头 - ManyVoices</a></li>

</ul>
</details>

**Tags**: `#中欧贸易`, `#电动汽车`, `#混动汽车`, `#贸易政策`, `#商务部`

---