

<h1 id="X2CDF">2603</h1>

<h2 id="q5cZK">UNITE:End-to-End Training for Unified Tokenization and Latent Denoising</h2>

[https://arxiv.org/abs/2603.22283](https://arxiv.org/abs/2603.22283)

[https://github.com/ShivamDuggal4/UNITE-tokenization-generation#](https://github.com/ShivamDuggal4/UNITE-tokenization-generation#)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1776505797287-a31fa36b-bdaa-4ec2-a9ee-c7f5fe83b2ce.png" alt="" width="50%" />
</div>



UNITE 是一个把 tokenizer 和 latent diffusion denoiser 合并成同一个共享网络的端到端训练框架，它证明了单阶段同时学习重建和生成是可行的，而且不依赖 DINO 这类外部 pretrained encoder 也能达到接近 SOTA 的效果。


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1776506295574-59543ced-a72a-470f-bcb5-9796ec394f7b.png" alt="" width="50%" />
</div>


<h2 id="tuPCU">GAE:Geometric Autoencoder for Diffusion Models</h2>

[https://arxiv.org/abs/2603.10365](https://arxiv.org/abs/2603.10365)

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1776508778139-21382302-6cef-4618-8efc-4641dd991fd7.png" alt="" width="50%" />
</div>



GAE 是一个为 diffusion model 专门设计的 autoencoder。它用 DINOv2 语义特征训练一个低维 semantic teacher，然后直接**监督 autoencoder 的 latent bottleneck**；再用 Latent Normalization 和 Dynamic Noise Sampling 让 latent 分布稳定、decoder 对噪声鲁棒。最终得到的 latent 低维、语义强、重建稳定，因此能显著加速和提升后续 diffusion 训练



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1776508810458-9f8d82ad-0830-434d-a44f-3517131aebda.png" alt="" width="50%" />
</div>



<h2 id="wtLJ6"><font style="color:rgb(0, 0, 0);">MacTok: Robust Continuous Tokenization for Image Generation</font></h2>

[https://arxiv.org/abs/2603.29634](https://arxiv.org/abs/2603.29634)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1778113740175-6b49acff-2cf1-450d-b686-82afb772b545.png" alt="" width="50%" />
</div>


核心是对 encoder 输入端的 image tokens 做 masked reconstruction 来防止 continuous tokenizer 的 posterior collapse，其中 mask 包括 random mask 和 DINO-guided semantic mask；DINO 通过 cls-token 与 patch-token 相似度选择语义重要区域，同时还用于 global/local representation alignment 来增强 latent 语义结构。



<h2 id="ZnuBW"></h2>






<h1 id="xTuF4">2512</h1>


<h2 id="LUu8z"><font style="color:rgb(0, 0, 0);">Improved Mean Flows: On the Challenges of Fastforward Generative Models</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1764828213803-78c9a578-c806-4281-b6c3-0ca2f58a40b5.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2512.02012](https://arxiv.org/abs/2512.02012)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1764829215443-900cf8f2-2268-4737-b34b-8425007a64aa.png" alt="" width="50%" />
</div>


> 改进的点有三：1.将计算JVP时候的速度换为网络的输出；2.是将条件注入的方式AdaLN-zero换为了InContext-Conditioning(最早用在DiT);3.将CFG的系数作为网络的输入条件；



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1764857269111-6623b671-044c-4528-8748-1ec56b039fc5.png" alt="" width="50%" />
</div>


分析一下其和MeanFlow的伪代码就可以看出区别（带CFG的可以看论文）


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1764857443890-8bcfe527-d21a-4520-ae7b-3dc80925932e.png" alt="" width="50%" />
</div>


<h2 id="ys37T"><font style="color:rgb(0, 0, 0);">BiFlow:Bidirectional Normalizing Flow: From Data to Noise and Back</font></h2>

[https://arxiv.org/abs/2512.10953](https://arxiv.org/abs/2512.10953)









<h1 id="kZcwE">2511</h1>

<h2 id="hOl3j"><font style="color:rgb(0, 0, 0);">Understanding, Accelerating, and Improving MeanFlow Training</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1764857665345-1f56e549-de59-4bd2-9c87-01848fd81ebc.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2511.19065](https://arxiv.org/abs/2511.19065)





<h2 id="eygAy"><font style="color:rgb(0, 0, 0);">MF-RAE：MeanFlow Transformers with Representation Autoencoders</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1763648077264-96e1e36d-01bb-4f4f-adcd-1c72e35a6394.png" alt="" width="50%" />
</div>


[https://www.arxiv.org/abs/2511.13019](https://www.arxiv.org/abs/2511.13019)

[https://github.com/sony/mf-rae](https://github.com/sony/mf-rae)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1763648340056-8c38c2b2-3479-4bc5-bd76-f68cf700a940.png" alt="" width="50%" />
</div>


<h2 id="TXPuO"><font style="color:rgb(0, 0, 0);">ReMeanFlow:Flow Straighter and Faster: Efficient One-Step Generative Modeling via MeanFlow on Rectified Trajectories</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1764814722064-b47a643f-4770-4b61-bceb-f9fcbee7582c.png" alt="" width="50%" />
</div>


[https://www.arxiv.org/abs/2511.23342](https://www.arxiv.org/abs/2511.23342)

[https://github.com/Xinxi-Zhang/Re-MeanFlow](https://github.com/Xinxi-Zhang/Re-MeanFlow)

<h2 id="RqGMO"></h2>

<h1 id="deRtZ">2510</h1>

<h2 id="YTUGT"><font style="color:rgb(0, 0, 0);">HyCa:Let Features Decide Their Own Solvers: Hybrid Feature Caching for Diffusion Transformers (ICLR 2026)</font></h2>

[https://arxiv.org/abs/2510.04188](https://arxiv.org/abs/2510.04188)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1776357713099-ce0c4704-f524-45aa-a6c1-8e843f3dcc31.png" alt="" width="50%" />
</div>


> 主要是用来在扩散 Transformer 采样时做**特征缓存（feature caching）**。它的关键思想不是“所有特征都用同一种预测/缓存策略”，而是让**不同特征维度根据自己的动态特性，选择最合适的数值求解器**来预测下一步特征，从而在基本不掉质的情况下显著加速采样

This paper proposes a training-free diffusion transformer acceleration framework, HyCa, which models hidden feature evolution as a mixture of ODEs and performs dimension-wise hybrid solver assignment for feature caching, yielding strong speed-quality trade-offs across image, video, editing, and distilled settings


<h2 id="xHbkc"><font style="color:rgb(0, 0, 0);">SVG:Latent Diffusion Model without Variational Autoencoder</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761892849210-41728316-efe4-445a-957d-1b316fcfd38c.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2510.15301](https://arxiv.org/abs/2510.15301)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761892864543-16928b31-0a02-4ac4-a298-3850cf8a311d.png" alt="" width="50%" />
</div>






<h2 id="pncVF"><font style="color:rgb(0, 0, 0);">RAE:Diffusion Transformers with Representation Autoencoders</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1760426361733-a21621ff-1a26-4f1c-ade6-5941f4219730.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2510.11690](https://arxiv.org/abs/2510.11690)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1760427553149-1a236394-3ecc-45bc-836f-b3c7e28220bc.png" alt="" width="50%" />
</div>


<font style="color:rgb(0, 0, 0);">The core insight is that replacing traditional VAEs with Representation Autoencoders (RAEs)—built on frozen, semantically-rich encoders like DINO—creates a higher-dimensional latent space that enables diffusion transformers to achieve superior generation quality and efficiency, challenging the long-held belief that semantic and generative objectives are incompatible.</font>

<h2 id="BDu0n"><font style="color:rgb(0, 0, 0);">AR-Drag:Real-Time Motion-Controllable Autoregressive Video Diffusion</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1760155801719-6d228dcc-0883-4d28-8159-8116eea7adb4.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2510.08131](https://arxiv.org/abs/2510.08131)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1760155866092-8c148008-56cd-4139-aaed-1a8053aeec66.png" alt="" width="50%" />
</div>


南洋理工与Xmax.ai等提出AR-Drag：强化学习赋能，实现实时可控的自回归视频生成 - 我爱计算机视觉的文章 - 知乎

[https://zhuanlan.zhihu.com/p/1960305323458945600](https://zhuanlan.zhihu.com/p/1960305323458945600)

<font style="color:rgb(25, 27, 31);">AR-Drag 的实现主要分为两个阶段：首先通过微调让模型具备基础的运动控制能力，然后利用强化学习进行“精修”，让控制更精准、效果更惊艳。</font>



<h2 id="zpH42"><font style="color:rgb(0, 0, 0);">FARMER: Flow AutoRegressive Transformer over Pixels</font></h2>

[https://arxiv.org/abs/2510.23588](https://arxiv.org/abs/2510.23588)



<h1 id="kTG42">2509</h1>

<h2 id="vQLWF"><font style="color:rgb(0, 0, 0);">Bidirectional Sparse Attention for Faster Video Diffusion Training</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756994491068-28e7eace-5c02-4754-9295-3392be91a82e.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2509.01085](https://arxiv.org/abs/2509.01085)







<h2 id="QHS3I"><font style="color:rgb(0, 0, 0);">RecA:Reconstruction Alignment Improves Unified Multimodal Models</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1757743412725-d76d994f-b4f7-4e18-a5fb-6781be288119.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2509.07295](https://arxiv.org/abs/2509.07295)







<font style="color:rgb(0, 0, 0);">这篇论文的动机是解决统一多模态模型（UMMs）在训练时严重依赖图像-文本对，而文本描述通常是稀疏的，会遗漏大量细粒度的视觉细节（如空间布局、几何结构、属性等），导致模型的理解和生成能力之间存在偏差。</font>

<font style="color:rgb(0, 0, 0);">其创新点在于提出了</font>**<font style="color:rgb(0, 0, 0);">重建对齐（Reconstruction Alignment, RecA）</font>**<font style="color:rgb(0, 0, 0);">方法，这是一种资源高效的后训练策略。它利用模型自身的视觉理解编码器提取的密集语义嵌入作为“文本提示”，通过自监督的图像重建损失来重新对齐UMM的理解和生成能力，无需任何额外的标注数据。</font>


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1757743560247-f9de5d06-5990-4aa8-bf5e-7f34ab69aef4.png" alt="" width="50%" />
</div>


<h1 id="zBIz1">2508</h1>

<h2 id="JVP9e"><font style="color:rgb(0, 0, 0);">S^2-Guidance: Stochastic Self Guidance for Training-Free Enhancement of Diffusion Models</font></h2>

[https://arxiv.org/abs/2508.12880](https://arxiv.org/abs/2508.12880)

<h3 id="61502d87">动机总结</h3>

本文的动机源于对当前扩散模型中广泛使用的**Classifier-free Guidance (CFG)**技术的深入分析。通过高斯混合模型的闭式解实验，作者发现CFG存在以下关键问题：

**次优预测问题**  
CFG生成的样本与真实数据分布存在明显偏差（如图3所示），这种偏差会导致语义不连贯和低质量输出。例如，在1D高斯混合实验中，CFG预测的分布峰值会偏离真实模态位置（红色框标注区域）：  



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756020302726-0f0ec480-e120-4681-9f26-48ade70b389c.png" alt="" width="50%" />
</div>


1. **训练依赖性缺陷**  
现有改进方法（如Autoguidance）需要额外训练弱模型或依赖人工调整网络结构（如注意力区域修改），这在大规模预训练模型中难以实现。
2. **计算效率瓶颈**  
初步提出的Naive S²-Guidance虽能提升质量，但需要多次前向传播计算子网络预测，计算成本过高（如图8所示）。

---

<h3 id="271ed8ad">创新点总结</h3>

<h4 id="3809d2f9">1. **理论创新：揭示模型自校正机制**</h4>

+ 通过实验证明**模型自身的子网络**可以模拟弱模型的行为（如图2所示），其预测能有效修正CFG的次优结果。
+ 提出贝叶斯视角的解释：子网络预测通过蒙特卡洛采样近似后验分布均值，其偏差方向指示了需要规避的低质量区域。  



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756020303090-2ece7110-1420-461d-9131-459ed9675930.png" alt="" width="50%" />
</div>


<h4 id="3d794902">2. **方法创新：随机块丢弃策略**</h4>

+ **动态子网络构建**：提出通过随机丢弃模型块（如10%比例）生成子网络，无需训练即可模拟弱模型（算法1）。
+ **单步自校正机制**：发现每个时间步仅需一次块丢弃即可实现有效引导（对比图10中Naive与S²-Guidance效果相似），计算量降低至与CFG相当。


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756020359607-0ad1fb38-36d3-46a3-92d0-a0903df1bc7a.png" alt="" width="50%" />
</div>


<h4 id="441451c0">3. **应用创新：通用高效适配**</h4>

+ **多模态兼容性**：在文本生成图像（SD3/SD3.5）和视频（Wan-1.3B/14B）任务中均显著超越基线（表1、表2）。
+ **质量-多样性平衡**：如图4所示，S²-Guidance在保持分布保真度的同时提升条件对齐：  



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756020302888-333a5e85-dcfd-4cd6-926e-e155ec854a5c.png" alt="" width="50%" />
</div>


<h4 id="8d9df9b3">4. **性能突破**</h4>

+ **定量指标**：在HPSv2.1基准上平均提升0.6%（SD3）和0.7%（SD3.5），T2I-CompBench组合属性得分提升5-8%（表1）。
+ **人类评估**：用户研究中31%的总体偏好率（图11），显著优于CFG（18.3%）和CFG-Zero（21%）。



<h1 id="b2Nx2">2507</h1>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761879419473-9461c121-9b98-4abb-b4ba-55bd99f05a97.png" alt="" width="50%" />
</div>


<h2 id="EDpXg"></h2>

<font style="color:rgb(0, 0, 0);"></font>

<h2 id="j8man"><font style="color:rgb(0, 0, 0);">REG:Representation Entanglement for Generation:Training Diffusion Transformers Is Much Easier Than You Think</font></h2>

[https://arxiv.org/pdf/2507.01467](https://arxiv.org/pdf/2507.01467)

<font style="color:rgb(0, 0, 0);"></font>


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1758530957272-ab243687-9b6b-4908-84d2-7e069b16f325.png" alt="" width="50%" />
</div>


<h2 id="DmZQa"><font style="color:rgb(0, 0, 0);">KARL:Single-pass Adaptive Image Tokenization for Minimum Program Search (NeurIPS 2025)</font></h2>

[https://arxiv.org/abs/2507.07995](https://arxiv.org/abs/2507.07995)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1779010982615-bb75c0e5-0599-4ca8-847d-7759f15cefde.png" alt="" width="50%" />
</div>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1779011031027-6be8bfb9-2b17-4b63-a4d8-07738cae9727.png" alt="" width="50%" />
</div>


根据图像的内容来选择分配多少token表示这张图，可以在重建损失约束下去完成图像的表征。









<h1 id="PZN0I">2506</h1>

<h2 id="V5oLn"><font style="color:rgb(0, 0, 0);">Contrastive Flow Matching （ICCV 25）</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761915444849-531f739f-78b6-442a-bf16-212a34e049d7.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2506.05350](https://arxiv.org/abs/2506.05350)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761915503400-8acef1fe-952f-4af2-ab84-5ebfbcc9ae12.png" alt="" width="50%" />
</div>




+ 动机：<font style="color:rgb(0, 0, 0);">flows from different conditions may overlap, leading to more ambiguous generations</font>
+ 创新点：<font style="color:rgb(0, 0, 0);">adds a contrastive objective that maximizes dissimilarities between predicted flows from arbitrary sample pairs</font>

<font style="color:rgb(0, 0, 0);"></font>


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761915554535-7535b2a5-cf49-4c7c-9fb3-d8b168063e2e.png" alt="" width="50%" />
</div>


<h2 id="B61c6"><font style="color:rgb(0, 0, 0);">Align Your Flow: Scaling Continuous-Time Flow Map Distillation</font></h2>

[https://arxiv.org/abs/2506.14603](https://arxiv.org/abs/2506.14603)

<h2 id="IaRBf"><font style="color:rgb(0, 0, 0);">PPFlow：</font><font style="color:rgb(0, 0, 0);">Pyramidal Patchification Flow for Visual Generation</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1757743785088-14e1727e-2fd0-4741-a09e-b1d5eaba62b9.png" alt="" width="50%" />
</div>


[https://arxiv.org/pdf/2506.23543](https://arxiv.org/pdf/2506.23543)



<font style="color:rgb(0, 0, 0);">这篇论文的动机是</font>**<font style="color:rgb(0, 0, 0);">提升扩散变换器（DiT）的推理效率</font>**<font style="color:rgb(0, 0, 0);">，特别是减少去噪过程中输入到DiT块的token数量，从而降低计算成本。</font>

<font style="color:rgb(0, 0, 0);">其核心创新点是一种名为</font>**<font style="color:rgb(0, 0, 0);">金字塔式分块流（Pyramidal Patchification Flow, PPFlow）</font>**<font style="color:rgb(0, 0, 0);">的方法，具体包括：</font>

1. **<font style="color:rgb(0, 0, 0);">动态分块策略</font>**<font style="color:rgb(0, 0, 0);">：根据噪声水平（时间步）动态调整Patchify操作中的块大小。高噪声时用</font>**<font style="color:rgb(0, 0, 0);">大块</font>**<font style="color:rgb(0, 0, 0);">（如4x4），低噪声时用</font>**<font style="color:rgb(0, 0, 0);">小块</font>**<font style="color:rgb(0, 0, 0);">（如2x2），以减少高噪声阶段（计算量主要集中于此）的token数量。</font>
2. **<font style="color:rgb(0, 0, 0);">全分辨率操作</font>**<font style="color:rgb(0, 0, 0);">：与需要在不同分辨率金字塔表征间转换的Pyramidal Flow等方法不同，PPFlow始终在</font>**<font style="color:rgb(0, 0, 0);">全分辨率潜在表征</font>**<font style="color:rgb(0, 0, 0);">上进行操作，避免了复杂的“再噪声（renoisng）”技巧和“跳跃点”问题。</font>
3. **<font style="color:rgb(0, 0, 0);">共享与独有参数</font>**<font style="color:rgb(0, 0, 0);">：不同块大小级别</font>**<font style="color:rgb(0, 0, 0);">共享DiT块的全部参数</font>**<font style="color:rgb(0, 0, 0);">，但各有其</font>**<font style="color:rgb(0, 0, 0);">独立的Patchify和Unpatchify线性投影层参数</font>**<font style="color:rgb(0, 0, 0);">。</font>
4. **<font style="color:rgb(0, 0, 0);">高效训练方式</font>**<font style="color:rgb(0, 0, 0);">：支持</font>**<font style="color:rgb(0, 0, 0);">从头训练</font>**<font style="color:rgb(0, 0, 0);">和</font>**<font style="color:rgb(0, 0, 0);">基于预训练DiT微调</font>**<font style="color:rgb(0, 0, 0);">两种模式。微调时通过巧妙的参数初始化，能用极少的额外训练成本（<10% FLOPs）获得高性能模型。</font>

**<font style="color:rgb(0, 0, 0);">最终效果</font>**<font style="color:rgb(0, 0, 0);">：在保证甚至略微提升图像生成质量（FID, IS）的同时，实现了</font>**<font style="color:rgb(0, 0, 0);">1.6倍至2.0倍的推理加速</font>**<font style="color:rgb(0, 0, 0);">。</font>


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1757743854485-dfdf5686-cb5f-459e-8051-022c95810bed.png" alt="" width="50%" />
</div>


<h2 id="lFpxR"></h2>


<h1 id="kQQxT">2505</h1>

<h2 id="rUUkQ">Jenga：<font style="color:rgb(0, 0, 0);">Training-Free Efficient Video Generation via Dynamic Token Carving</font></h2>

[https://arxiv.org/pdf/2505.16864](https://arxiv.org/pdf/2505.16864)



<h2 id="TMtlb">Flow-GRPO : Training Flow Matching Models via Online RL  </h2>

[https://www.arxiv.org/pdf/2505.05470](https://www.arxiv.org/pdf/2505.05470)



<h2 id="AvMCD">BLIP3-o: A Family of Fully Open Unified Multimodal Models-Architecture, Training and Dataset</h2>

[https://arxiv.org/pdf/2505.09568v1](https://arxiv.org/pdf/2505.09568v1)





<h2 id="mfhhv"><font style="color:rgb(0, 0, 0);">Swin DiT: Diffusion Transformer using Pseudo Shifted Windows</font></h2>

[https://arxiv.org/abs/2505.13219](https://arxiv.org/abs/2505.13219)



<h2 id="JLuUE">GRAT：Grouping First, Attending Smartly: Training-Free Acceleration for Diffusion Transformers</h2>

[https://arxiv.org/abs/2505.14687](https://arxiv.org/pdf/2505.14687)

DIT架构中存在空间稀疏attention机制


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1748163247570-b85cb124-e4ce-4597-bb81-642f1046f6b5.png" alt="" width="50%" />
</div>


然后通过使用不同的sparse机制实现了更快的attention加速


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1748163310152-59b6201c-fdf1-4543-83d7-f0a1f5b4e426.png" alt="" width="50%" />
</div>


性能比较：GRAT的两个版本实现了更大的稀疏度，同时GRAT-B（类似NATTN）速度更快；


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1748159554190-7d803983-928c-4952-8700-c1a52237626f.png" alt="" width="50%" />
</div>






<h1 id="QoLNw">2504</h1>

<h2 id="Xh9qc"><font style="color:rgb(0, 0, 0);">D2iT: Dynamic Diffusion Transformer for Accurate Image Generation</font></h2>

[https://arxiv.org/abs/2504.09454](https://arxiv.org/abs/2504.09454)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1754917966495-2488622a-4109-4990-94df-2075b0189af6.png" alt="" width="50%" />
</div>



<h1 id="VVADS">2503</h1>

<h2 id="orirf"><font style="color:rgb(0, 0, 0);">REPA:Aligning Text to Image in Diffusion Models is Easier Than You Think</font></h2>

[https://arxiv.org/abs/2503.08250](https://arxiv.org/abs/2503.08250)

<h2 id="Py1Wa"><font style="color:rgb(0, 0, 0);">OminiControl2: Efficient Conditioning for Diffusion Transformers</font></h2>

[https://arxiv.org/abs/2503.08280](https://arxiv.org/abs/2503.08280)



<h2 id="vBtIg"><font style="color:rgb(0, 0, 0);">Direct Discriminative Optimization: Your Likelihood-Based Visual Generative Model is Secretly a GAN Discriminator</font></h2>

[https://arxiv.org/pdf/2503.01103](https://arxiv.org/pdf/2503.01103)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1754917710210-a994446c-aa4c-4189-aab2-7f623c480a36.png" alt="" width="50%" />
</div>






<h1 id="u25lS">2502</h1>

<h2 id="Ck8ug"><font style="color:rgb(0, 0, 0);">MG: Diffusion Models without Classifier-free Guidance</font></h2>

[https://arxiv.org/abs/2502.12154](https://arxiv.org/abs/2502.12154)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1740574461592-e190ee52-b329-493c-90cd-a7f8fae93319.png" alt="" width="50%" />
</div>


<h2 id="lW0ht"><font style="color:rgb(0, 0, 0);">FlashVideo:Flowing Fidelity to Detail for Efficient High-Resolution Video Generatio</font></h2>

[https://arxiv.org/abs/2502.05179](https://arxiv.org/abs/2502.05179)

> 区别于使用低分辨率视频作为条件生成高分辨率视频，作者采用Flow Matching的方法将前一阶段的结果当作第二阶段的起点，使得第二阶段高分辨率视频生成过程steps更短。

**细节:**第二阶段的起点从像素域和特征域共同构造，可以更好地保留细节和结构



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1739256097394-bc27490d-3fc5-4ce6-8566-2adcc68e673d.png" alt="" width="50%" />
</div>


**实验结果：**


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1739255827571-94147058-4861-4050-b870-3633e6ab2eb4.png" alt="" width="50%" />
</div>



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1739256275642-508b5d1d-6588-4863-ad93-35713e8509e4.png" alt="" width="50%" />
</div>




<h2 id="vDNj0"><font style="color:rgb(0, 0, 0);">Fast Video Generation with Sliding Tile Attention</font></h2>

[https://arxiv.org/abs/2502.04507v1](https://arxiv.org/abs/2502.04507v1)

代码：[https://github.com/hao-ai-lab/FastVideo](https://github.com/hao-ai-lab/FastVideo)



<h2 id="Rdm47">Efficient-vDiT: Efficient Video Diffusion Transformers With Attention Tile</h2>

[https://arxiv.org/abs/2502.06155v2](https://arxiv.org/abs/2502.06155v2)



<h2 id="MH5W2"><font style="color:rgb(0, 0, 0);">Improving the Diffusability of Autoencoders(ICML2025)</h2>

[https://arxiv.org/pdf/2502.14831v3](https://arxiv.org/pdf/2502.14831v3)



<h2 id="e55dbcf3"><font style="color:teal;">EQ-VAE</font><font style="color:rgb(54, 54, 54);">: Equivariance Regularized Latent Space for Improved Generative Image Modeling （ICML 2025)</font></h2>

[https://arxiv.org/abs/2502.09509](https://arxiv.org/abs/2502.09509)





<h1 id="s4X50">2501</h1>


<h2 id="cORmq"><font style="color:rgb(0, 0, 0);">TREAD: Token Routing for Efficient Architecture-agnostic Diffusion Training</font></h2>

[https://arxiv.org/abs/2501.04765v2](https://arxiv.org/abs/2501.04765v2)

传统训练中，所有Token必须顺序通过所有网络层，计算冗余高（如Transformer的二次复杂度）。

残差网络（如DiT）的层间输出高度相似（图4），表明**部分计算可能冗余**，但直接丢弃Token（如掩码）会破坏扩散模型的渐进去噪特性。


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756025972623-eef5cd23-497c-4a86-b2cc-e50d71ee8bcd.png" alt="" width="50%" />
</div>


作者提出：

+ **动态子网络训练**：提出**随机路由（Routing）**机制，让部分Token跳过中间层（恒等映射），其余Token正常计算（图3b）。
+ **无损信息流**：跳过的Token在更深层重新引入，避免掩码方法的永久信息丢失（对比MaskDiT）。


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756025837637-bb837a8f-f152-4e04-83af-3a29a05395bb.png" alt="" width="50%" />
</div>


保持单一重建损失，无需额外损失函数（如MAE）。


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1756026005298-1d7f8db3-847e-4ce5-9f85-2da141fc2751.png" alt="" width="50%" />
</div>


其核心创新在于**利用层间冗余**，以无损方式实现效率与效果的“双赢”，为扩散模型的低成本训练开辟了新路径。

<h2 id="wtCuC"></h2>


<h2 id="CBgx5">VA-VAE:<font style="color:rgb(0, 0, 0);">Reconstruction vs. Generation: Taming Optimization Dilemma in Latent Diffusion Models</font></h2>

[https://arxiv.org/abs/2501.01423](https://arxiv.org/abs/2501.01423)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1747995051813-46afbee5-a926-443b-ba5a-a8a082391670.png" alt="" width="50%" />
</div>


**论文创新点**：



<h2 id="qEgMv"><font style="color:rgb(0, 0, 0);">AnyStory: Towards Unified Single and Multiple Subject Personalization in Text-to-Image Generation  </font></h2>

[https://arxiv.org/pdf/2501.09503](https://arxiv.org/pdf/2501.09503)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1737270549244-0a18e05a-c8f4-4ffd-8c51-4b59fb7fd67d.png" alt="参考图引导的T2I生成" width="50%" />
</div>




<h1 id="hr51I">2412</h1>

<h2 id="F7gkt"><font style="color:rgb(0, 0, 0);">SparseDiT: Token Sparsification for Efficient Diffusion Transformer (NeurIPS 2025)</font></h2>

[https://arxiv.org/abs/2412.06028v2](https://arxiv.org/abs/2412.06028v2)

<h2 id="wyyX7"><font style="color:rgb(0, 0, 0);">CLEAR: Conv-Like Linearization Revs Pre-Trained Diffusion Transformers Up</font></h2>

[https://arxiv.org/abs/2412.16112v1](https://arxiv.org/abs/2412.16112v1)



<h2 id="Z3P2P"><font style="color:rgb(0, 0, 0);">HunyuanVideo: A Systematic Framework For Large Video Generative Models</font></h2>

[https://arxiv.org/abs/2412.03603v6](https://arxiv.org/abs/2412.03603v6)



<h2 id="gZomW"><font style="color:rgb(0, 0, 0);">Causal Diffusion Transformers for Generative Modeling</font></h2>

[https://arxiv.org/abs/2412.12095v2](https://arxiv.org/abs/2412.12095v2)



<h2 id="TAmqF"><font style="color:rgb(0, 0, 0);">Distillation++：</font><font style="color:rgb(0, 0, 0);">Inference-Time Diffusion Model Distillation (ICCV 25)</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761916046195-f9ba13f9-40a9-4ce2-b54b-558ad3841e93.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2412.08871](https://arxiv.org/abs/2412.08871)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761916079412-36ef0e86-f16c-4202-9771-2c39af258026.png" alt="" width="50%" />
</div>


+ 动机：<font style="color:rgb(0, 0, 0);">Diffusion distillation models exhibit a performance gap compared to their pre-trained diffusion model counterparts</font>
+ <font style="color:rgb(0, 0, 0);">做法：integrate distillation optimization during reverse sampling, which can be viewed as teacher guidance that drives student sampling trajectory towards the clean manifold using pre-trained diffusion models</font>


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1761916091843-a00de1e0-8424-4fcb-8467-3be645632bf0.png" alt="" width="50%" />
</div>








<h1 id="LuVyU">2411</h1>

<h2 id="Mlsaa"><font style="color:rgb(0, 0, 0);">Factorized Visual Tokenization and Generation</font></h2>

[https://arxiv.org/abs/2411.16681](https://arxiv.org/abs/2411.16681)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1754917821693-63f20e8f-d68a-417a-9452-ddd9f59f2b6f.png" alt="" width="50%" />
</div>






<h1 id="kO1hc">2410</h1>

<h2 id="Te6Mr"><font style="color:rgb(31, 35, 40);">Pyramidal Flow Matching for Efficient Video Generative Modeling</font></h2>

[https://arxiv.org/pdf/2410.05954](https://arxiv.org/pdf/2410.05954)

<h2 id="w4iZz"><font style="color:rgb(0, 0, 0);">One Step Diffusion via Shortcut Models</font></h2>

[https://arxiv.org/pdf/2410.12557](https://arxiv.org/pdf/2410.12557)

<h1 id="JhIsm">2409</h1>

<h2 id="va6g6"><font style="color:rgb(0, 0, 0);">OmniGen: Unified Image Generation</font></h2>

[https://arxiv.org/abs/2409.11340](https://arxiv.org/abs/2409.11340)





<h1 id="RZwwP">2408·</h1>

<h2 id="S74IO"><font style="color:#117CEE;">Imagen 3</font></h2>

arxiv: [https://arxiv.org/pdf/2408.07009](https://arxiv.org/pdf/2408.07009)

<h1 id="SyvN7">2407</h1>

<h2 id="SV7v0"><font style="color:rgb(0, 0, 0);">Diffusion Forcing: Next-token Prediction Meets Full-Sequence Diffusion</font></h2>

[https://arxiv.org/abs/2407.01392v4](https://arxiv.org/abs/2407.01392v4)





<h1 id="wJPqs">2406</h1>

<h2 id="x48zM"><font style="color:rgb(0, 0, 0);">Guiding a Diffusion Model with a Bad Version of Itself (</font><font style="color:rgb(0, 0, 0);">NeurIPS 2024)</font></h2>

[https://arxiv.org/abs/2406.02507v1](https://arxiv.org/abs/2406.02507v1)

How to describe the defination and process of diffuison model, we can learn from:


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1757244384944-efe764df-f0ca-4d0f-9bf3-a21de91a98b8.png" alt="" width="50%" />
</div>


Autoguidance 用一个更小、更少训练的同条件 diffusion model 作为负向参考，通过主模型和弱模型的差异方向提升采样质量，从而比 CFG 更好地保留多样性，并且还能用于无条件生成。


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1776556226910-6e25dcd7-4a2e-44ec-b660-5b5fd94031b3.png" alt="" width="50%" />
</div>




<h2 id="wG2aD"><font style="color:rgb(0, 0, 0);">DiTFastAttn: Attention Compression for Diffusion Transformer Models</font></h2>

[https://arxiv.org/abs/2406.08552v2](https://arxiv.org/abs/2406.08552v2)



<h1 id="GzOtT">2405</h1>

<h2 id="GAmC4"><font style="color:rgb(0, 0, 0);">Hunyuan-DiT: A Powerful Multi-Resolution Diffusion Transformer with Fine-Grained Chinese Understanding</font></h2>

[https://arxiv.org/abs/2405.08748](https://arxiv.org/abs/2405.08748)

<h2 id="ME4DV">PeRFlow: Piecewise Rectified Flow as Universal Plug-and-Play Accelerator  </h2>

[https://arxiv.org/pdf/2405.07510](https://arxiv.org/pdf/2405.07510)



<h2 id="b5e6h"><font style="color:rgb(0, 0, 0);">EMD:EM Distillation for One-step Diffusion Models (NeurIPS2024)</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1759753706185-eda40669-ea1c-4d12-84a8-e82300aefdb0.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2405.16852](https://arxiv.org/abs/2405.16852)

<h2 id="HEoQa"></h2>

<h1 id="HLX8P">2403</h1>

<h2 id="mooIB"><font style="color:#117CEE;">SD3</font><font style="color:rgb(0, 0, 0);">：Scaling Rectified Flow Transformers for High-Resolution Image Synthesis</font></h2>

arxiv: [https://arxiv.org/pdf/2403.03206](https://arxiv.org/pdf/2403.03206)

<h2 id="pVJJ6"><font style="color:rgb(0, 0, 0);">CogView3: Finer and Faster Text-to-Image Generation via Relay Diffusion</font></h2>

[https://arxiv.org/abs/2403.05121](https://arxiv.org/abs/2403.05121)



<h2 id="CCnb9"><font style="color:rgb(0, 0, 0);">PixArt-Σ: Weak-to-Strong Training of Diffusion Transformer for 4K Text-to-Image Generation</font></h2>

[https://arxiv.org/abs/2403.04692](https://arxiv.org/abs/2403.04692)



<h2 id="RbyjX">SD3-Turbo: <font style="color:rgb(0, 0, 0);">Fast High-Resolution Image Synthesis with Latent Adversarial Diffusion Distillation</font></h2>

[https://arxiv.org/abs/2403.12015](https://arxiv.org/abs/2403.12015)



<h2 id="dJ6bi"><font style="color:rgb(0, 0, 0);">SemanticDraw: Towards Real-Time Interactive Content Creation from Image Diffusion Models</font></h2>

[https://arxiv.org/abs/2403.09055v3](https://arxiv.org/abs/2403.09055v3)



<h1 id="t9szT">2402</h1>

<h2 id="zCkjP"><font style="color:rgb(0, 0, 0);">DistriFusion: Distributed Parallel Inference for High-Resolution Diffusion Models</font></h2>

[https://arxiv.org/abs/2402.19481](https://arxiv.org/abs/2402.19481)

<h2 id="AJqbj"><font style="color:rgb(0, 0, 0);">InstanceDiffusion: Instance-level Control for Image Generation</font></h2>

[https://arxiv.org/abs/2402.03290](https://arxiv.org/abs/2402.03290)



<h2 id="MskEp">ContextDiff: <font style="color:rgb(0, 0, 0);">Contextualized Diffusion Models for Text-Guided Image and Video Generation</font></h2>

[https://arxiv.org/abs/2402.16627v3](https://arxiv.org/abs/2402.16627v3)

<h1 id="zX0qa">2401</h1>

<h2 id="vzGq7"><font style="color:rgb(0, 0, 0);">SiT: Exploring Flow and Diffusion-based Generative Models with Scalable Interpolant Transformers(ECCV 2024)</font></h2>

[https://arxiv.org/abs/2401.08740v2](https://arxiv.org/abs/2401.08740v2)



<h2 id="jEWgw">RPG: <font style="color:rgb(0, 0, 0);">Mastering Text-to-Image Diffusion: Recaptioning, Planning, and Generating with Multimodal LLMs</font></h2>

[https://arxiv.org/abs/2401.11708](https://arxiv.org/abs/2401.11708)



<h2 id="xBu1y">ConPreDiff: <font style="color:rgb(0, 0, 0);">Improving Diffusion-Based Image Synthesis with Context Prediction</font></h2>

[https://arxiv.org/abs/2401.02015](https://arxiv.org/abs/2401.02015)



<h2 id="ssUip"><font style="color:rgb(0, 0, 0);">PIXART-δ: Fast and Controllable Image Generation with Latent Consistency Models</font></h2>

[https://arxiv.org/abs/2401.05252](https://arxiv.org/abs/2401.05252)



<h1 id="DuJRt">2312</h1>

<h2 id="poH58"><font style="color:rgb(0, 0, 0);">EDM2: Analyzing and Improving the Training Dynamics of Diffusion Models (</font><font style="color:rgb(31, 35, 40);">CVPR 2024 oral)</font></h2>

[https://arxiv.org/abs/2312.02696](https://arxiv.org/abs/2312.02696)







<h1 id="D9QeT">2311</h1>

<h2 id="QJbe8"><font style="color:rgb(0, 0, 0);">Ranni: Taming Text-to-Image Diffusion for Accurate Instruction Following</font></h2>

[https://arxiv.org/abs/2311.17002](https://arxiv.org/abs/2311.17002)



<h2 id="UdlKU"><font style="color:rgb(0, 0, 0);">ElasticDiffusion: Training-free Arbitrary Size Image Generation through Global-Local Content Separation</font></h2>

[https://arxiv.org/abs/2311.18822](https://arxiv.org/abs/2311.18822)



<h2 id="FYZFm"><font style="color:rgb(0, 0, 0);">DMD:One-step Diffusion with Distribution Matching Distillation （CVPR 2024)</font></h2>

[https://arxiv.org/abs/2311.18828](https://arxiv.org/abs/2311.18828)


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767755132059-c801db58-9cbf-4854-9fd2-4be24ceca98a.png" alt="" width="50%" />
</div>


如何计算KL散度损失？首先我们可以推导出评价真实分布和学生分布之间KL的计算公式


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767756821648-ef9c05b6-e9bc-48c1-a7d1-c005d5f748a8.png" alt="" width="50%" />
</div>


然后我们需要去计算这一项的梯度，推导如下：


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767756871045-156b66fe-0656-43dc-91f2-56a7214bf65f.png" alt="" width="50%" />
</div>


想一下这一项能算吗？可以使用下面的两个公式来计算score function，而他们需要的x_0则有我们的G_\thata来提供
<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767757098486-4bb70358-5238-45f3-98f7-9a66582311e4.png" alt="" width="10%" />
</div>



<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767757007241-d4b7e1db-0033-44b2-99f8-501829c1d828.png" alt="" width="50%" />
</div>


所以最终KL损失变换为


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767757187385-90927c9d-ac1f-4def-a7b3-f0c3ecf45c52.png" alt="" width="50%" />
</div>


这里的真实score对应的网络不进行更新，而fake网络的更新则与正常的去噪网络一样


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767757272935-558dcd36-c06e-434d-9260-7bdaf58c191b.png" alt="" width="50%" />
</div>




整体算法框架如下


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767757313359-33aa17fa-4f24-4abe-8dfa-e37ff76e8fc7.png" alt="" width="50%" />
</div>


其中生成器对网络参数的求导通过实现的损失函数来定义，参考如下代码：


<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2026/png/26304400/1767770761253-4f72a985-cc9d-4060-9964-b655c4f73f33.png" alt="" width="50%" />
</div>


<h1 id="X16Ze">2310</h1>

<h2 id="IVHSV"><font style="color:rgb(0, 0, 0);">PixArt-</font><font style="color:rgb(0, 0, 0);">α</font><font style="color:rgb(0, 0, 0);">: Fast Training of Diffusion Transformer for Photorealistic Text-to-Image Synthesis</font></h2>

[https://arxiv.org/abs/2310.00426](https://arxiv.org/abs/2310.00426)

<h1 id="UzOsN">2308</h1>

<h2 id="CkwZr"><font style="color:rgb(0, 0, 0);">IP-Adapter: Text Compatible Image Prompt Adapter for Text-to-Image Diffusion Models</font></h2>

[https://arxiv.org/abs/2308.06721](https://arxiv.org/abs/2308.06721)



<h1 id="xRkhX">2307</h1>

<h2 id="MCICe"><font style="color:rgb(0, 0, 0);">SDXL: Improving Latent Diffusion Models for High-Resolution Image Synthesis</font></h2>

[https://arxiv.org/abs/2307.01952](https://arxiv.org/abs/2307.01952)

<h2 id="Yzxpc"><font style="color:rgb(0, 0, 0);">BoxDiff: Text-to-Image Synthesis with Training-Free Box-Constrained Diffusion</font></h2>

[https://arxiv.org/abs/2307.10816](https://arxiv.org/abs/2307.10816)



<h2 id="kp8b7"><font style="color:rgb(0, 0, 0);">AnyDoor: Zero-shot Object-level Image Customization</font></h2>

[https://arxiv.org/abs/2307.09481](https://arxiv.org/abs/2307.09481)



<h1 id="dxVYA">2306</h1>

<h2 id="NnQKo"><font style="color:rgb(0, 0, 0);">Wuerstchen: An Efficient Architecture for Large-Scale Text-to-Image Diffusion Models</font></h2>

[https://arxiv.org/abs/2306.00637](https://arxiv.org/abs/2306.00637)



<h2 id="ng4ed"><font style="color:rgb(0, 0, 0);">DragDiffusion: Harnessing Diffusion Models for Interactive Point-based Image Editing</font></h2>

[https://arxiv.org/abs/2306.14435](https://arxiv.org/abs/2306.14435)



<h2 id="Rq2Yk">ZestGuide: <font style="color:rgb(0, 0, 0);">Zero-shot spatial layout conditioning for text-to-image diffusion models</font></h2>

[https://arxiv.org/abs/2306.13754](https://arxiv.org/abs/2306.13754)

<h1 id="S3yVm">2303</h1>

<h2 id="sRD3O">Stochastic Interpolants: A Unifying Framework for Flows and Diffusions</h2>

[https://arxiv.org/pdf/2303.08797v3](https://arxiv.org/pdf/2303.08797v3)

<h2 id="SvgD5">UniDiffuser: <font style="color:rgb(0, 0, 0);">One Transformer Fits All Distributions in Multi-Modal Diffusion at Scale</font></h2>

[https://arxiv.org/abs/2303.06555](https://arxiv.org/abs/2303.06555)

<h2 id="ur3e6"><font style="color:rgb(0, 0, 0);">SVDiff: Compact Parameter Space for Diffusion Fine-Tuning</font></h2>

[https://arxiv.org/abs/2303.11305](https://arxiv.org/abs/2303.11305)

<h1 id="L0b0A">2302</h1>

<h2 id="ChqfO">ControlNet: <font style="color:rgb(0, 0, 0);">Adding Conditional Control to Text-to-Image Diffusion Models</font></h2>

[https://arxiv.org/abs/2302.05543](https://arxiv.org/abs/2302.05543)



<h2 id="vzfFL">Specialist Diffusion: Plug-and-Play Sample-Efficient Fine-Tuning of Text-to-Image Diffusion Models to Learn Any Unseen Style  </h2>

[https://openaccess.thecvf.com/content/CVPR2023/papers/Lu_Specialist_Diffusion_Plug-and-Play_Sample-Efficient_Fine-Tuning_of_Text-to-Image_Diffusion_Models_To_CVPR_2023_paper.pdf](https://openaccess.thecvf.com/content/CVPR2023/papers/Lu_Specialist_Diffusion_Plug-and-Play_Sample-Efficient_Fine-Tuning_of_Text-to-Image_Diffusion_Models_To_CVPR_2023_paper.pdf)



<h1 id="MOFy4">2301</h1>

<h2 id="VXUjm"><font style="color:rgb(0, 0, 0);">GLIGEN: Open-Set Grounded Text-to-Image Generation</font></h2>

[https://arxiv.org/abs/2301.07093](https://arxiv.org/abs/2301.07093)

<h1 id="eZ98D">2212</h1>

<h2 id="nuoay"><font style="color:rgb(0, 0, 0);">Multi-Concept Customization of Text-to-Image Diffusion</font></h2>

[https://arxiv.org/abs/2212.04488](https://arxiv.org/abs/2212.04488)



<h2 id="eign2">DIT:  Scalable Diffusion Models with Transformers  </h2>

[https://arxiv.org/pdf/2212.09748](https://arxiv.org/pdf/2212.09748)

<h1 id="YqTou">2211</h1>

<h2 id="LIBxf"><font style="color:rgb(0, 0, 0);">Versatile Diffusion: Text, Images and Variations All in One Diffusion Model</font></h2>

[https://arxiv.org/abs/2211.08332](https://arxiv.org/abs/2211.08332)

<h2 id="SoM1p">Corgi: <font style="color:rgb(0, 0, 0);">Shifted Diffusion for Text-to-image Generation</font></h2>

[https://arxiv.org/abs/2211.15388](https://arxiv.org/abs/2211.15388)



<h2 id="nrH4w"></h2>

<h1 id="z2Vyj">2210</h1>

<h2 id="QIMn1"><font style="color:rgb(0, 0, 0);">ERNIE-ViLG 2.0: Improving Text-to-Image Diffusion Model with Knowledge-Enhanced Mixture-of-Denoising-Experts</font></h2>

[https://arxiv.org/abs/2210.15257](https://arxiv.org/abs/2210.15257)



<h1 id="fcOtc"></h1>

<h1 id="g5rtn">2208</h1>

<h2 id="c9sns"><font style="color:rgb(0, 0, 0);">DreamBooth: Fine Tuning Text-to-Image Diffusion Models for Subject-Driven Generation</font></h2>

[https://arxiv.org/abs/2208.12242](https://arxiv.org/abs/2208.12242)



<h2 id="FDS6O">CFG：Classifier-free diffusion guidance</h2>

[https://arxiv.org/pdf/2207.12598v1](https://arxiv.org/pdf/2207.12598v1)

<h1 id="VkyPR">2206</h1>

<h2 id="J81zk"><font style="color:rgb(0, 0, 0);">EDM:Elucidating the Design Space of Diffusion-Based Generative Models</font></h2>

<div align="center">
  <img src="https://cdn.nlark.com/yuque/0/2025/png/26304400/1757245110444-de330b31-18ac-4be4-b8c6-a670b93ee221.png" alt="" width="50%" />
</div>


[https://arxiv.org/abs/2206.00364](https://arxiv.org/abs/2206.00364)



<h1 id="ba3Lf">2205</h1>

<h2 id="nOPOl"><font style="color:#117CEE;">Imagen</font>：<font style="color:rgb(0, 0, 0);">Photorealistic Text-to-Image Diffusion Models with Deep Language Understanding</font></h2>

[https://arxiv.org/abs/2205.11487](https://arxiv.org/abs/2205.11487)



<h1 id="qPb4y">2204</h1>

<h2 id="AaINy"><font style="color:rgb(79, 79, 79);">DALLE-3: Improving </font><font style="color:rgb(78, 161, 219) !important;">Image</font><font style="color:rgb(79, 79, 79);"> Generation with Better Captions</font></h2>

[https://cdn.openai.com/papers/dall-e-3.pdf](https://cdn.openai.com/papers/dall-e-3.pdf)

<h2 id="YY9Um">DALLE-2 : <font style="color:rgb(0, 0, 0);">Hierarchical Text-Conditional Image Generation with CLIP Latents</font></h2>

[https://arxiv.org/abs/2204.06125](https://arxiv.org/abs/2204.06125)

<h1 id="aBNBm">2112</h1>

<h2 id="K2I3r"><font style="color:#117CEE;">GLIDE</font><font style="color:rgb(0, 0, 0);">: Towards Photorealistic Image Generation and Editing with Text-Guided Diffusion Models</font></h2>

[https://arxiv.org/abs/2112.10741](https://arxiv.org/abs/2112.10741)

<h2 id="GZqTg"><font style="color:rgb(0, 0, 0);">LDM:High-Resolution Image Synthesis with Latent Diffusion Models</font></h2>

[https://arxiv.org/abs/2112.10752](https://arxiv.org/abs/2112.10752)

<h2 id="32514622"></h2>

<h1 id="Vh0ge">2111</h1>

<h2 id="gjIC4"><font style="color:#117CEE;">VQ-Diffusion</font><font style="color:rgb(0, 0, 0);">:</font><font style="color:rgb(0, 0, 0);">Vector Quantized Diffusion Model for Text-to-Image Synthesis</font></h2>

arxiv: [https://arxiv.org/pdf/2111.14822](https://arxiv.org/pdf/2111.14822)



<h2 id="XYzli">Blended Diffusion: <font style="color:rgb(0, 0, 0);">Blended Diffusion for Text-driven Editing of Natural Images</font></h2>

[https://arxiv.org/abs/2111.14818](https://arxiv.org/abs/2111.14818)

<h1 id="B45fn">2105</h1>

<h2 id="RUzkZ"><font style="color:#117CEE;">ADM</font>：Diffusion Models Beat GANs on Image Synthesis  </h2>

arxiv: [https://arxiv.org/pdf/2105.05233v4](https://arxiv.org/pdf/2105.05233v4)

