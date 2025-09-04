[![Maintenance](https://img.shields.io/badge/Maintained%3F-yes-brightgreen.svg)](https://GitHub.com/Naereen/StrapDown.js/graphs/commit-activity)
[![PR's Welcome](https://img.shields.io/badge/PRs-welcome-orange.svg?style=flat)](http://makeapullrequest.com)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)



# 📝 A Systematic Survey and Meta-Analysis of the Segment Anything Model in Remote Sensing Image Processing: Challenges, Advances, Applications, and Opportunities

> **The First Comprehensive and Systematic Review of the recent advancements of SAM in RS.** Zhipeng Wan, Sheng Wang, Wei Han, *et al.* [[paper]()] [[homepage](https://github.com/WanZhan-lucky/WanSAM4RS-Tracker)][[中文解读]()] 

> **<p align="justify"> Abstract:** *In recent years, artificial intelligence (AI) technology has profoundly revolutionized the domain of remote sensing (RS), bringing transformative changes from data collection to analysis. Traditional remote sensing image interpretation (RSII) relies on manual interpretation and task-specific models, which suffer from low efficiency, high costs, and poor generalization, making them inadequate for large-scale data processing and complex tasks. With the emergence of foundational models (FMs) (i.e., large pre-trained AI models), not only has efficiency and accuracy been significantly improved, but diverse tasks can also be executed efficiently. Notably, the segment anything model (SAM) has challenged traditional visual paradigms, sparking widespread interest in task-agnostic visual FMs. Its exceptional zero-shot generalization capability has demonstrated outstanding performance in natural scenes, offering new perspectives and methodologies for the automation and intelligence of RSII. However, there are significant differences in spatial characteristics and data structures between RS images and natural images, meaning the application potential of SAM in RSII has yet to be comprehensively evaluated. Although existing studies have demonstrated SAM's adaptability in RSII, the current literature lacks systematic and in-depth reviews. To fill this gap, this study conducts a comprehensive review and meta-analysis for the first time, focusing on the challenges, advances, applications, and potential of SAM in RSII. The paper first reviews SAM’s advances in RS and compiles relevant research findings. It then analyzes the inherent challenges of RS and explores the bottlenecks of SAM in RS, including semantic information loss, discrepancies between training and target domains, prompt dependency and design complexity, and insufficient robustness. Next, it outlines the details of the meta-analysis conducted to reveal the research status of SAM in RS. Following that, the paper delves into the adaptation methods of SAM in RS image processing and evaluates its performance in both general and specific RS tasks. Finally, future research directions are summarized. Additionally, to support the continued development of this field, a dedicated repository has been created and maintained [here](https://github.com/WanZhan-lucky/WanSAM4RS-Tracker).* </p>

## 📌 Contributions
**🚩 1.**   To our knowledge, this work conducts the first comprehensive and systematic review of the recent advancements of SAM in RS, fills gaps &emsp; &emsp;&nbsp;in current studies and offers a reference for the latest developments in this domain. 
 
**🚩 2.**   Starting from the inherent challenges of the RS domain, this study identifies the bottlenecks of SAM in RSII tasks, explores its adaptation &emsp; &emsp; strategies, systematically evaluates its performance in both general and specific tasks, and proposes future research directions to expand &emsp; &emsp; its application scope and advance the field.

**🚩 3.**   The meta-analysis synthesizes SAM research in RS, quantifies adaptation strategies, task distributions, and application patterns, and &nbsp;&nbsp;&emsp;&emsp;highlights   fine-tuning dominance, change detection focus, and agricultural and environmental applications, providing empirical support  &nbsp;&nbsp;&emsp;&emsp;for capability evaluation and future development.


## 🔗Citation

If you find our work useful in your research, please consider citing:
```
```

## :fire: Highlights
```
 - We will continue to follow SAM’s latest progress in RS and update related research accordingly.
 - We also encourage and welcome researchers to actively contribute.
 - You can add paper information by submitting a Pull Request!
```

## 🧩 Main contents [![Last Commited](https://img.shields.io/github/last-commit/WanZhan-lucky/WanSAM4RS-Tracker?label=Last%20Updated&color=purple)](https://github.com/WanZhan-lucky/WanSAM4RS-Tracker/commits)
- [1、Segment Anything Model](#SAM)
- [2、Literature Reviews on SAM Since Its Release](#sam-reviews)
- [3、A brief timeline of SAM’s development in RSII tasks](#introduction)
- [4、Overview of SAM-Based Adaptation Methods in RSII](#adaptation)
- [5、Summary of SAM-Based Methods for Routine Remote Sensing Tasks](#sam-rs-tasks)
- [6、Summary of SAM-Based Methods for Specific Remote Sensing Applications](#sam-summary)
- [7、A Chronological List of SAM-Based Model Papers for Remote Sensing Research](#sam-paper-list)
  - [2023](#2023) | [2024](#2024) | [2025](#2025) | [2025.09 (To be supplemented)](#supplement)
- [8、0thers](#other)
  
## ✨Latest Updates & 📢 Related Content！ [![Last Updated](https://img.shields.io/github/last-commit/WanZhan-lucky/WanSAM4RS-Tracker?label=Last%20Updated&color=blue)](https://github.com/WanZhan-lucky/WanSAM4RS-Tracker/commits)

  + [x] https://github.com/AkashahS/segRS
  relate
  + [ ] [2025.05.09] Few-Shot Semantic Segmentation on Remote Sensing Images With Learnable Prototype [[paper](https://ieeexplore.ieee.org/abstract/document/10994816)]
  + [ ] 

## ✅ Segment Anything Model <div id="SAM"></div>
&nbsp;&nbsp;&nbsp;&nbsp;Meta AI introduced the foundational vision model Segment Anything Model ([SAM](https://segment-anything.com/)), which adopts a prompt-driven image segmentation paradigm to generate precise object masks automatically or interactively. SAM demonstrates remarkable performance in natural image processing tasks. Its core architecture comprises three main components: an image encoder based on the Vision Transformer (ViT) architecture , a prompt encoder, and a mask decoder.
![image](https://github.com/WanZhan-lucky/WanSAM4RS-Tracker/blob/main/SAMRSI.jpg)
&nbsp;&nbsp;&nbsp;&nbsp;In late July 2024, Meta followed up with the release of [SAM2](https://github.com/facebookresearch/segment-anything) and [SAM2.1](https://github.com/facebookresearch/sam2), which build upon the original SAM by introducing a streaming memory architecture and refining the prompt mechanism. SAM2 aims to unify image and video segmentation by integrating spatial and temporal information for seamless transitions between static and dynamic content, while SAM2.1 further enhances occlusion handling through data augmentation and improved positional encoding, thereby broadening its application scope. For instance, [MemorySAM](https://github.com/Chenfei-Liao/MemorySAM) introduces modality-agnostic memory and semantic prototypes for cross-modal enhancement; [SAM2.1++](https://ieeexplore.ieee.org/document/11094917) incorporates distractor-aware memory and introspective updates to improve tracking robustness.

## ⏳A brief timeline of SAM’s development in RSII tasks <div id="introduction"></div>
![image](https://github.com/WanZhan-lucky/WanSAM4RS-Tracker/blob/main/SAMTimeWan-analysis-bigrevised.png)

- [2023.04] **SAM** : "Segment anything" [[paper](https://arxiv.org/abs/2304.02643)][[homepage](https://segment-anything.com)]
- [2023.04] **Text2Seg** : "Text2seg: Remote sensing image semantic segmentation via text-guided visual foundation models" [[paper](https://arxiv.org/abs/2304.10597)][[github](https://github.com/Douglas2Code/Text2Seg)][[Chinese explanation](https://zhuanlan.zhihu.com/p/672832552)]
- [2023.05] **SAMRS** : "Samrs: Scaling-up remote sensing segmentation dataset with segment anything model" [[paper](https://proceedings.neurips.cc/paper_files/paper/2023/hash/1be3843e534ee06d3a70c7f62b983b31-Abstract-Datasets_and_Benchmarks.html)][[github](https://github.com/ViTAE-Transformer/SAMRS)]
- [2023.04] **Semantic-SAM** : "Semantic-SAM: Segment and Recognize Anything at Any Granularity" [[paper](https://arxiv.org/abs/2307.04767)]
  [[github](https://github.com/UX-Decoder/Semantic-SAM)][[Chinese explanation](https://zhuanlan.zhihu.com/p/643692158)]
- [2023.11] **RingMo-SAM** : "RingMo-SAM: A foundation model for segment anything in multimodal remote-sensing images" [[paper](https://ieeexplore.ieee.org/abstract/document/10315957)]
- [2023.11] **GeoSAM** : "GeoSAM: Fine-tuning SAM with sparse and dense visual prompting for automated segmentation of mobility infrastructure" [[paper](https://arxiv.org/abs/2311.11319)][[github](https://github.com/rafiibnsultan/GeoSAM)][[chinese explanation](https://zhuanlan.zhihu.com/p/672686023)]
- [2023.12] **STC** : "Segment-then-Classify: Few-shot instance segmentation for environmental remote sensing" [[paper](https://s3.us-east-1.amazonaws.com/climate-change-ai/papers/neurips2023/53/paper.pdf)]
  [[homepage](https://neurips.cc/virtual/2023/76884#:~:text=The%20proposed%20Segment-then-Classify%20%28STC%29%20strategy%20leverages%20the%20zero-shot,Transformer%20%28ViT%29%20to%20identify%20objects%20of%20interest%20thereafter.)]
- [2024.01] **RSPrompt** : "RSPrompter: Learning to prompt for remote sensing instance segmentation based on visual foundation model" [[paper](https://ieeexplore.ieee.org/abstract/document/10409216)]
  [[github](https://github.com/KyanChen/RSPrompter)][[Chinese explanation](https://zhuanlan.zhihu.com/p/640989466)]
- [2024.02] **RSAM-Seg** : "RSAM-Seg: A SAM-based Approach with Prior Knowledge Integration for Remote Sensing Image Semantic Segmentation" [[paper](https://www.mdpi.com/2072-4292/17/4/590)][[github](https://github.com/Chief-byte/RSAM-Seg)]
  [[chinese explanation](https://zhuanlan.zhihu.com/p/684939858)][[Blog](https://blog.csdn.net/m0_64106140/article/details/136447074)]
- [2024.03] **UV-SAM** : "Uv-sam: Adapting segment anything model for urban village identification" [[paper](https://arxiv.org/abs/2401.08083)][[github](https://github.com/tsinghua-fib-lab/UV-SAM)][[chinese explanation](https://zhuanlan.zhihu.com/p/678607517)][[Blog](https://hub.baai.ac.cn/view/34556)] [[github](https://github.com/tsinghua-fib-lab/UV-SAM)][[chinese explanation](https://zhuanlan.zhihu.com/p/678607517)][[homepage](https://ojs.aaai.org/index.php/AAAI/article/view/30260)]
- [2024.03] **SAM-Road** : "Segment Anything Model for Road Network Graph Extraction" [[paper](https://ieeexplore.ieee.org/document/10678570)][[github](https://github.com/htcr/sam_road)][[chinese explanation](https://zhuanlan.zhihu.com/p/689738891)][[homepage](https://openaccess.thecvf.com/content/CVPR2024W/SG2RL/html/Hetang_Segment_Anything_Model_for_Road_Network_Graph_Extraction_CVPRW_2024_paper.html)]
- [2024.04] **CocoaNet** : "Weakly Supervised Semantic Segmentation with Consistency-Constrained Multi-Class Attention for Remote Sensing Scenes" [[paper](https://ieeexplore.ieee.org/abstract/document/10507065)]
- [2024.05] **MeSAM** : "MeSAM: Multiscale Enhanced Segment Anything Model for Optical Remote Sensing Images" [[paper](https://ieeexplore.ieee.org/abstract/document/10522788)][[github](https://github.com/Magic-lem/MeSAM)]
- [2024.06] **MAF-SAM** : "A multispectral remote sensing crop segmentation method based on Segment Anything Model using Multi-stage Adaptation Fine-tuning" [[paper](https://ieeexplore.ieee.org/abstract/document/10551868)][[chinese explanation](https://blog.csdn.net/JishuFengyang/article/details/140374521)]
- [2024.06] **ALPS** : "ALPS: An Auto-Labeling and Pre-training Scheme for Remote Sensing Segmentation With Segment Anything Model" [[paper](https://ieeexplore.ieee.org/abstract/document/10949707)][[github](https://github.com/StriveZs/ALPS)][[chinese explanation](https://blog.csdn.net/JishuFengyang/article/details/140353352)]
- [2024.07] **Road-SAM** : "Road-sam: Adapting the segment anything model to road extraction from large very-high-resolution optical remote sensing images" [[paper](https://ieeexplore.ieee.org/document/10613866)]
- [2024.07] **SAM2** : "SAM 2: Segment Anything in Images and Video" [[paper](https://arxiv.org/abs/2408.00714)][[github](https://github.com/facebookresearch/sam2)][[chinese explanation](https://zhuanlan.zhihu.com/p/718534459)][[homepage](https://sam2-online.com/)]
- [2024.08] **MM-SAM** : "Segment Anything with Multiple Modalities" [[paper](https://arxiv.org/abs/2408.09085)][[github](https://github.com/weihao1115/mm-sam)][[chinese explanation](https://zhuanlan.zhihu.com/p/4785555526)][[homepage](https://xiaoaoran.github.io/projects/MM-SAM)]
- [2024.08] **SSRS** : "Sam-assisted remote sensing imagery semantic segmentation with object and boundary constraints" [[paper](https://ieeexplore.ieee.org/abstract/document/10636322)][[github](https://github.com/sstary/SSRS)] [[chinese explanation](https://zhuanlan.zhihu.com/p/673735215)] [[Blog](https://blog.csdn.net/m0_64106140/article/details/135693435)]
- [2024.09] **SAM-RSIS** : "SAM-RSIS: progressively adapting SAM with box prompting to remote sensing image instance segmentation" [[paper](https://ieeexplore.ieee.org/abstract/document/10680168)]
- [2024.09] **Point-SAM** : "PointSAM: Pointly-Supervised Segment Anything Model for Remote Sensing Images" [[paper](https://ieeexplore.ieee.org/abstract/document/10839471)][[github](https://github.com/Lans1ng/PointSAM)][[chinese explanation](https://wxredian.com/art?id=e26bd8fbad5feab3bc864e380b47dc6c)]
- [2024.09] **SCM** : "Segment change model (scm) for unsupervised change detection in vhr remote sensing images: a case study of buildings" [[paper](https://ieeexplore.ieee.org/abstract/document/10642429)][[github](https://github.com/StephenApX/UCD-SCM)][[chinese explanation](https://zhuanlan.zhihu.com/p/675815166)]
- [2024.09] **BF-SAM** : "BF-SAM: enhancing SAM through multi-modal fusion for fine-grained building function identification" [[homepage](https://www.tandfonline.com/doi/abs/10.1080/13658816.2024.2399142)]
- [2024.09] **TFNet** : "Integrating Segment Anything Model derived boundary prior and high-level semantics for cropland extraction from high-resolution remote sensing images" [[paper](https://ieeexplore.ieee.org/abstract/document/10664585)][[github](https://github.com/long123524/TFNet)]
- [2024.10] **RSPS-SAM** : "RSPS-SAM: A Remote Sensing Image Panoptic Segmentation Method Based on SAM" [[paper](https://www.mdpi.com/2072-4292/16/21/4002)]
- [2024.10] **SolarSAM** : "SolarSAM: Building-scale Photovoltaic Potential Assessment Based on Segment Anything Model (SAM) and Remote Sensing for Emerging City" [[paper](https://www.sciencedirect.com/science/article/pii/S0960148124016288)][[github](https://github.com/REAILAB/SolarSAM?tab=readme-ov-file)]
- [2024.11] **MANet** : "MANet: Fine-Tuning Segment Anything Model for Multimodal Remote Sensing Semantic Segmentation" [[paper](https://arxiv.org/abs/2410.11160)][[github](https://github.com/sstary/SSRS)]
- [2024.11] **DED-SAM** : "DED-SAM: Adapting Segment Anything Model 2 for Dual Encoder-Decoder Change Detection" [[paper](https://ieeexplore.ieee.org/abstract/document/10741350)]
- [2024.12] **SEMPNet** : "SEMPNet: enhancing few-shot remote sensing image semantic segmentation through the integration of the segment anything model" [[paper](https://www.tandfonline.com/doi/epdf/10.1080/15481603.2024.2426589?needAccess=true)][[github](https://github.com/TinyAway/SEMPNet)][[homepage](https://www.tandfonline.com/doi/full/10.1080/15481603.2024.2426589)]
- [2024.12] **RS-SAM** : "RS-SAM: Integrating Multi-scale Information for Enhanced Remote Sensing Image Segmentation" [[paper](https://openaccess.thecvf.com/content/ACCV2024/papers/Zhang_RS-SAM_Integrating_Multi-Scale_Information_for_Enhanced_Remote_Sensing_Image_Segmentation_ACCV_2024_paper.pdf)][[homepage](https://openaccess.thecvf.com/content/ACCV2024/html/Zhang_RS-SAM_Integrating_Multi-Scale_Information_for_Enhanced_Remote_Sensing_Image_Segmentation_ACCV_2024_paper.html)]
- [2025.01] **CWSAM** : "ClassWise-SAM-adapter: Parameter efficient fine-tuning adapts segment anything to SAR domain for semantic segmentation" [[paper](https://ieeexplore.ieee.org/abstract/document/10849617)][[github](https://github.com/xypu98/CWSAM)][[chinese explanation](https://zhuanlan.zhihu.com/p/690725962)][[Blog](https://blog.csdn.net/m0_64106140/article/details/135729375)]
- [2025.01] **PSP-SAM** : "Progressive Self-Prompting Segment Anything Model for Salient Object Detection in Optical Remote Sensing Images" [[paper](https://www.mdpi.com/2072-4292/17/2/342)]
- [2025.01] **ASS-CD** : "ASS-CD: Adapting Segment Anything Model and Swin-Transformer for Change Detection in Remote Sensing Images" [[paper](https://www.mdpi.com/2072-4292/17/3/369)]
- [2025.01] **MSA-SAM** : "Multi-scale Adapter Based on SAM for Remote Sensing Semantic Segmentation" [[paper](https://ieeexplore.ieee.org/abstract/document/10824913)][[github](https://github.com/mint0126/Mult-scale-SAM)][[Blog](https://blog.csdn.net/m0_54239393/article/details/147773066)]
- [2025.02] **UrbanSAM** : "Urbansam: Learning invariance-inspired adapters for segment anything models in urban construction" [[paper](https://arxiv.org/abs/2502.15199)][[github](https://github.com/danfenghong)][[chinese explanation](https://developer.volcengine.com/articles/7480397554527109129)]
- [2025.03] **ROS-SAM** : "ROS-SAM: High-Quality Interactive Segmentation for Remote Sensing Moving Object" [[paper](https://openaccess.thecvf.com/content/CVPR2025/papers/Shan_ROS-SAM_High-Quality_Interactive_Segmentation_for_Remote_Sensing_Moving_Object_CVPR_2025_paper.pdf)][[github](https://github.com/ShanZard/ROS-SAM)][[chinese explanation](https://zhuanlan.zhihu.com/p/1893242456016928919)][[explanation2](https://developer.volcengine.com/articles/7501164018351112201)][[homepage](https://openaccess.thecvf.com/content/CVPR2025/html/Shan_ROS-SAM_High-Quality_Interactive_Segmentation_for_Remote_Sensing_Moving_Object_CVPR_2025_paper.html)]
- [2025.03] **RS2-SAM2** : "Customized SAM 2 for Referring Remote Sensing Image Segmentation" [[paper](https://arxiv.org/abs/2503.07266)]
- [2025.03] **DirectSAM-RS** : "Prompting DirectSAM for Semantic Contour Extraction in Remote Sensing Images" [[paper](https://ieeexplore.ieee.org/abstract/document/10889192)][[github](https://github.com/StevenMsy/DirectSAM-RS)]

*If you find any incomplete parts in the compilation, especially missing GitHub links for papers, please feel free to let me know by submitting an issue on GitHub. I will update and improve it in a timely manner.*

## 🤖 Overview of SAM-Based Adaptation Methods in RSII <div id="adaptation"></div>
| **Name** | **Title** | **Link** |
|:----------:|:-----------:|:----------:|
|CWSAM | |  [[paper]()][[chinese explanation]()][[github]()]|
|Water-Adapter		| | [[paper]()][[chinese explanation]()][[github]()]|
|RSAM-Seg		| | [[paper]()][[chinese explanation]()][[github]()]|
|MC-SAM	SEG	| | [[paper]()][[chinese explanation](https://zhuanlan.zhihu.com/p/715411620)][[github]()]|
|MSA-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|RS-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|UrbanSAM		|A Unified Framework with Multimodal Fine-tuning for Remote Sensing Semantic Segmentation | [[paper](https://ieeexplore.ieee.org/document/11063320)][[chinese explanation] (https://zhuanlan.zhihu.com/p/1924856324799324614)][[github](https://github.com/sstary/SSRS)]|
|Road-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|MANet		| | [[paper]()][[chinese explanation]()][[github]()]|
|Conv-LoRA		| | [[paper]()][[chinese explanation]()][[github]()]|
|SAM_MLoRA		| | [[paper]()][[chinese explanation]()][[github]()]|
|MAF-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|ROS-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|AFFE-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|MoPEFT		| | [[paper]()][[chinese explanation]()][[github]()]|
|Few-shot SLVM		| | [[paper]()][[chinese explanation]()][[github]()]|
|SAM-RSIS		| | [[paper]()][[chinese explanation]()][[github]()]|
|RSPrompter		| | [[paper]()][[chinese explanation]()][[github]()]|
|GeoSAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|UV-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|PointSAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|PSP-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|MeSAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|BSDSNet		| | [[paper]()][[chinese explanation]()][[github]()]|
|SAM-CFFNet		| | [[paper]()][[chinese explanation]()][[github]()]|
|Text2Seg		| | [[paper]()][[chinese explanation]()][[github]()]|
|RS2-SAM2		| | [[paper]()][[chinese explanation]()][[github]()]|
|RSRefSeg		| | [[paper]()][[chinese explanation]()][[github]()]|
|DirectSAM-RS		| | [[paper]()][[chinese explanation]()][[github]()]|
|E2SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|RingMoSAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|MM-SAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|AerOSeg		| | [[paper]()][[chinese explanation]()][[github]()]|
|InstructSAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|PerSAM		| | [[paper]()][[chinese explanation]()][[github]()]|
|Few-Shot SLVM		| | [[paper]()][[chinese explanation]()][[github]()]|
|SEMPNET		| | [[paper]()][[chinese explanation]()][[github]()]|
|SSRS		| | [[paper]()][[chinese explanation]()][[github]()]|
|TFNet | | [[paper]()][[chinese explanation]()][[github]()]|

## 🧬 Summary of SAM-Based Methods for Routine RS Tasks <div id="sam-rs-tasks"></div>
| **Name** | **Title** | **Link** |
|:--------:|:---------:|:--------:|
| DF4LCZ | | |[[paper]()][[chinese explanation]()][[github]()]|
| BSDSNet | | |[[paper]()][[chinese explanation]()][[github]()]|
| CocoaNet | | |[[paper]()][[chinese explanation]()][[github]()]|
| RS-TextWS-Seg | | |[[paper]()][[chinese explanation]()][[github]()]|
| CSNet | | |[[paper]()][[chinese explanation]()][[github]()]|
| STC | | |[[paper]()][[chinese explanation]()][[github]()]|
| RSPS-SAM | | |[[paper]()][[chinese explanation]()][[github]()]|
| FSAMDA | | |[[paper]()][[chinese explanation]()][[github]()]|
| SPFS | | |[[paper]()][[chinese explanation]()][[github]()]|
| SAM-CD |  Adapting Segment Anything Model for Change Detection in VHR Remote Sensing Images |[[paper](https://ieeexplore.ieee.org/document/10443350)][[chinese explanation]()][[github](https://github.com/DingLei14/SAM-CD)]|
| ASS-CD | | |[[paper]()][[chinese explanation]()][[github]()]|
| TTP | | |[[paper]()][[chinese explanation]()][[github]()]|
| SCDM | | |[[paper]()][[chinese explanation]()][[github]()]|
| CS-WSCDNet | | |[[paper]()][[chinese explanation]()][[github]()]|
| <u>SAM-CD</u> | | |[[paper]()][[chinese explanation]()][[github]()]|
| SCD-SAM |SCD-SAM: Adapting Segment Anything Model for Semantic Change Detection in Remote Sensing Imagery |[[paper](https://ieeexplore.ieee.org/abstract/document/10543161)][[chinese explanation]()][[github]()] |
| DED-SAM | | |[[paper]()][[chinese explanation]()][[github]()]|
| TS-SAM | | |[[paper]()][[chinese explanation]()][[github]()]|
| HSACNet | | |[[paper]()][[chinese explanation]()][[github]()]|
| SCM | | |[[paper]()][[chinese explanation]()][[github]()]|

## 🛠️ Summary of SAM-Based Methods for Specific RS Applications <div id="sam-summary"></div>
| **Name** | **Title** | **Link** |
|:--------:|:---------:|:--------:|
| SAM-OBC | | [[paper]()][[chinese explanation]()][[github]()]|
| LandslideNet | | [[paper]()][[chinese explanation]()][[github]()]|
| SAMLS | | [[paper]()][[chinese explanation]()][[github]()]|
| SinkSAM | | [[paper]()][[chinese explanation]()][[github]()]|
| SAM-Road | | [[paper]()][[chinese explanation]()][[github]()]|
| BF-SAM | | [[paper]()][[chinese explanation]()][[github]()]|
| UV-SAM | | [[paper]()][[chinese explanation]()][[github]()]|
| G2LDIE | | [[paper]()][[chinese explanation]()][[github]()]|
| SAMPolyBuild | | [[paper]()][[chinese explanation]()][[github]()]|
| SolarSAM | | [[paper]()][[chinese explanation]()][[github]()]|
| FMARS | | [[paper]()][[chinese explanation]()][[github]()]|
| USDA-SAM | | [[paper]()][[chinese explanation]()][[github]()]|
| fabSAM | | [[paper]()][[chinese explanation]()][[github]()]|
| FieldSeg | | [[paper]()][[chinese explanation]()][[github]()]|
| TFNet | | [[paper]()][[chinese explanation]()][[github]()]|
| MAF-SAM | | [[paper]()][[chinese explanation]()][[github]()]|
| Tree-GPT | | [[paper]()][[chinese explanation]()][[github]()]|
| 3D-GILBE | | [[paper]()][[chinese explanation]()][[github]()]|

## 🌐 Literature Reviews on SAM Since Its Release <div id="sam-reviews"></div>

| **Date** | **Title** | **Link** |
|:--------:|:----------:|:--------:|
| 2023.05 | A Comprehensive Survey on Segment Anything Model for Vision and Beyond | [[paper]()][[chinese explanation]()][[github]()]|
| 2023.05 | A Survey on Segment Anything Model (SAM): Vision Foundation Model Meets Prompt Engineering | [[paper]()][[chinese explanation]()][[github]()]|
| 2023.09 | Research on Derived Tasks and Realistic Applications of Segment Anything Model: A Literature Review | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.01 | Segment Anything Model (SAM) for Medical Image Segmentation: A Preliminary Review | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.02 | Segment anything model for medical image segmentation: Current Status and Future Directions | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.04 | Segment Anything Is Not Always Perfect: An Investigation of SAM on Different Real-world Application Scenarios | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.06 | An Empirical Study on the Robustness of the Segment Anything Model (SAM) | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.07 | Segment Anything for Videos: A Systematic Survey | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.08 | Unleashing the Potential of SAM2 for Biomedical Images and Videos: A Survey | [[paper]()][[chinese explanation]()][[github]()]|
| 2024.10 | On Efficient Variants of Segment Anything Model: A Survey | [[paper]()][[chinese explanation]()][[github]()]|

> 📄 **Supplementary entry notice**:

The following is a supplementary review on SAM, and researchers are welcome to contribute additional related surveys.
| **Date** | **Title** | **Link** |
|:--------:|:----------:|:--------:|
|2024.03 *(Supplementary)*  |Principles, applications, and advancements of the Segment Anything Model| [homepage](https://direct.ewa.pub/proceedings/ace/article/view/10924)|
| 2024.06 *(Supplementary)* | 分割一切模型SAM的潜力与展望：综述|[[paper]()][[chinese explanation]()][[github]()]|
| ...| ... |...|
 
## 📚 A Chronological List of SAM-Based Model Papers for Remote Sensing  <div id="sam-paper-list"></div> 

### 📘2023  <div id="2023"></div> 


#### April
- **SAM** – Segment Anything Model  
- **SATIR** – Learning to "Segment Anything" in Thermal Infrared Images Through Knowledge Distillation  
- **Text2seg** – Text2seg: Remote Sensing Image Semantic Segmentation via Text-Guided Visual Foundation Models  

#### May
- **Samrs** – Scaling-up Remote Sensing Segmentation Dataset with Segment Anything Model  
- **SAM-VQA** – SAM-VQA: Supervised Attention-Based Visual Question Answering Model for Post-Disaster Damage Assessment  

#### June
- **(Unnamed)** – On Aligning SAM to Remote Sensing Data  

#### September
- **GroupPrompter** – A Prompting Method for Semantic Segmentation Based on SAM  
- **Enhancing USDA NASS** – Enhancing USDA NASS Cropland Data Layer with Segment Anything Model  

#### October
- **Zero-Shot Refinement** – Zero-Shot Refinement of Buildings' Segmentation Models using SAM  
- **Tree-GPT** – Modular Large Language Model Expert System for Forest Remote Sensing Image Understanding  

#### November
- **GeoSAM** – Fine-Tuning SAM with Sparse and Dense Visual Prompting for Automated Segmentation of Mobility Infrastructure  
- **RingMo-SAM** – A Foundation Model for Segment Anything in Multimodal Remote-Sensing Images  

#### December
- **AI-SAM** – Automatic and Interactive Segment Anything Model  
- **SAM-Adapter** – Adapting Segment Anything in Underperformed Scenes  
- **STC** – Segment-then-Classify: Few-Shot Instance Segmentation for Environmental Remote Sensing  

---

### 📙2024  <div id="2024"></div> 
#### January
#### February
#### March
#### April
- **SAM-CD** – Segment Anything Model Guided Semantic Knowledge Learning for Remote Sensing Change Detection  
- **CocoaNet** – Weakly Supervised Semantic Segmentation with Consistency-Constrained Multi-Class Attention for Remote Sensing  

#### May
- **MeSAM** – Multiscale Enhanced Segment Anything Model for Optical Remote Sensing Images  
- **SCD-SAM** – Adapting SAM for Semantic Change Detection in Remote Sensing Imagery  
- **FMARS** – Annotating Remote Sensing Images for Disaster Management Using Foundation Models  

#### June
- **ALPS** – An Auto-Labeling and Pre-Training Scheme for Remote Sensing Segmentation with SAM  
- **SAM-CFFNet** – SAM-Based Cross-Feature Fusion Network for Intelligent Identification of Landslides  
- **DF4LCZ** – A SAM-Empowered Data Fusion Framework for Scene-Level Local Climate Zone Classification  

#### July
- **Road-SAM** – Adapting SAM to Road Extraction from Large Very-High-Resolution Optical Remote Sensing Images  
- **CSNet** – Context-Aggregated and SAM-Guided Network for ViT-Based Instance Segmentation in Remote Sensing Images  
- **SAM4Refugee** – Leveraging SAM in Identifying Buildings within Refugee Camps for Humanitarian Operations  

#### August
- **MC-SAM SEG** – Tuning a SAM-Based Model with Multi-Cognitive Visual Adapter to Remote Sensing Instance Segmentation  
- **SAM_MLoRAF** – Multi-LoRA Fine-Tuned SAM for Urban Man-Made Object Extraction  
- **MM-SAM** – Segment Anything with Multiple Modalities  
- **SSRS** – SAM-Assisted Remote Sensing Imagery Semantic Segmentation with Object and Boundary Constraints  

#### September
- **SAM-RSIS** – Progressively Adapting SAM with Box Prompting to Remote Sensing Image Instance Segmentation  
- **RegDA** – Local Region Homogenizing for Cross-Domain Remote Sensing Image Segmentation  
- **PointSAM** – Pointly-Supervised SAM for Remote Sensing Images  
- **SAM-Road** – Segment Anything Model for Road Network Graph Extraction  
- **TFNet** – Integrating SAM Derived Boundary Prior and High-Level Semantics for Cropland Extraction  

#### October
- **RS-TextWS-Seg** – Context-Aggregated and SAM-Guided Network for ViT-Based Instance Segmentation in Remote Sensing Images  
- **SinkSAM** – SinkSAM: A Monocular Depth-Guided SAM Framework for Automatic Sinkhole Segmentation  
- **SAMPolyBuild** – SAMPolyBuild: Adapting the Segment Anything Model for Polygonal Building Extraction  
- **SolarSAM** – SolarSAM: Building-Scale Photovoltaic Potential Assessment Based on SAM and Remote Sensing  

#### November
#### December

---

### 📗2025  <div id="2025"></div> 
#### January
 - **/** – SAM Enhanced Semantic Segmentation for Remote Sensing Imagery Without Additional Training  – [[paper](https://ieeexplore.ieee.org/document/10857947)][[chinese explanation]()][[github](https://github.com/qycools/SESSRS )]  
#### February
#### March
#### April
#### May
#### June
#### July
#### August
#### 🗓️ September <div id="supplement"></div> 
- **Waiting for replenishment** ......
## Other: 【Remote Sensing Image Processing or SAM-related, for reference only.】 <div id="other"></div> 
 + [ ] https://github.com/AkashahS/segRS
 + [ ] [2025.05.09] Few-Shot Semantic Segmentation on Remote Sensing Images With Learnable Prototype [[paper](https://ieeexplore.ieee.org/abstract/document/10994816)]

## 📦 License
This project is licensed under the [MIT License](./LICENSE.txt).  
You are free to use, modify, and distribute this software with proper attribution.

