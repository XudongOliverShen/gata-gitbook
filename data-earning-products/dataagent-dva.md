# 🤖DataAgent: DVA

<figure><img src="https://files.gitbook.com/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FIpgICGCeDtlQSOATHGKE%2Fuploads%2FE5jySQvXOA9ACgSVTDAu%2F%E6%88%AA%E5%B1%8F2025-01-20%20%E4%B8%8B%E5%8D%884.25.05.png?alt=media&#x26;token=f13beec4-75a1-4dca-b649-8c87af74802f" alt="" width="563"><figcaption><p>Gata DataAgent Platform</p></figcaption></figure>

### 1. Gata DataAgent Platform <a href="#id-1.-gata-dataagent-platform" id="id-1.-gata-dataagent-platform"></a>

Gata is building the DataAgent Platform, enabling individuals to run various DataAgents that automatically generate cutting-edgee data and earn passive rewards.

### 2. DVA DataAgent <a href="#id-2.-dva-dataagent" id="id-2.-dva-dataagent"></a>

DVA (Data Validation Agent) is Gata's first DataAgent. It runs locally to assess the quality of [image-caption pairs from the whole internet](https://github.com/mlfoundations/datacomp), assigning a score between -1 and 1. DVA scores help select the highest-quality image-caption data, which are then used to train various vision-language AIs, such as Stable Diffusion, DALL-E, and GPT-4o.

### 3. Motivation <a href="#id-3.-motivation" id="id-3.-motivation"></a>

Internet-scale image-caption datasets, such as [LAION](https://laion.ai/blog/laion-5b/) and [DataComp](https://arxiv.org/abs/2304.14108), underpin the pre-training of all vision-language AIs. These datasets, comprising tens of billions of image-caption pairs scraped from the internet, power text-to-image generative AI models like Stable Diffusion and DALL-E, as well as vision-language models like GPT-4V and GPT-4o.However, the AI industry faces two major challenges with internet-scale image-caption datasets:

1. **Exhaustion of Publicly Accessible Data**: Most publicly available image-caption data has already been utilized.
2. **Noisy Captions**: Captions derived from web scraping often fail to accurately represent the corresponding images.

Both academia and industry have explored two key approaches to address these challenges:

1. **Filtering**: By evaluating the quality of image-caption pairs and assigning scores, high-quality subsets can be filtered for better training, as demonstrated in Apple's recent work.
2. **Synthetic Caption Generation**: Vision-language models can be used to generate more accurate captions, significantly enhancing dataset quality, another approach explored by Apple.

#### **DVA: The First DataAgent for Image-Caption Data**

DVA evaluates the quality of image-caption pairs from across the internet and assigns scores ranging from -1 to 1. It is based on the [Data Filtering Networks](https://arxiv.org/abs/2309.17425). These scores enable the selection of the highest-quality data, exemplifying the filtering approach.

<figure><img src="../.gitbook/assets/截屏2025-02-03 上午11.57.38.png" alt="" width="563"><figcaption><p>When running the DVA DataAgent, its inputs and outputs are displayed in real-time, ensuring transparency.</p></figcaption></figure>

### 4. Frequently Asked Questions

**Q: Why can I only process one job every 45 seconds?**\
A: Although the jobs are computationally light, we enforce a 45-second limit to prevent any one user from monopolizing DataAgent jobs and to ensure everyone can participate.

**Q: I've run jobs for a while and completed some, but I haven't earned any Intelligence points. Why?**\
A: Intelligence points are earned only when the majority of peers running the same job agree on the result through our consensus mechanism. This process can take days, and even correct executions might not earn points if the peers disagree.
