<div align="center">
<img src="assets/banner-2.png" alt="MMPoT"/>

[![Paper Preprint](https://img.shields.io/badge/Paper-Preprint-b31b1b.svg?logo=arXiv)]()
[![Website](https://img.shields.io/badge/Website-blue.svg?logo=googlechrome&logoColor=white)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

**Watch this repository for the latest updates**

**Feel free to raise pull requests if you find some interesting papers!** 🌟

</div>

## <img src="assets/icon1.png" height="30" align="top"/> News
[2026/07/19] 🎉 We release our curation list of MLLMs Post-Training methods！<br>

---

## <img src="assets/icon2.png" height="30" align="top"/> Introduction
Multimodal Large Language Models (MLLMs) have reshaped AI by enabling perception, reasoning, and interaction across digital and physical environments. While multimodal pretraining establishes broad perceptual capabilities, translating them into behaviors aligned with human intent and real-world demands remains challenging. Multimodal Post-Training (MMPoT) addresses this gap by refining pretrained MLLMs toward reliable, task-oriented behavior. This survey reviews MMPoT from a behavior-shaping perspective and organizes existing methods into five families: instruction following, preference calibration, reasoning enhancement, domain adaptation, and scalable training. We further examine benchmarks and evaluation protocols, identify current limitations, and outline future directions toward general and reliable multimodal intelligence.

<p align="center">
  <img src="assets/framework-z.png" width="100%" alt="Post-training framework for MLLMs">
  <span><b>Figure 1. Overview of multimodal behavior shaping for MLLMs post-training.</b> Post-training algorithms can be viewed as behavior-shaping mechanisms that steer pretrained MLLMs toward desired behaviors, while multimodal data and benchmarks provide learning signals and evaluative feedback for iterative refinement.</span>
</p>

---

## <img src="assets/icon3.png" height="30" align="top"/> Contents

- [Multimodal Instruction Tuning](#multimodal-instruction-tuning)

- [Multimodal Alignment Learning](#multimodal-alignment-learning)
  - [Multimodal RLHF](#multimodal-rlhf)
  - [Multimodal RLAIF](#multimodal-rlaif)
  - [Multimodal Direct Preference Optimization](#multimodal-direct-preference-optimization)

- [Multimodal Reasoning Enhancement](#multimodal-reasoning-enhancement)
  - [R1-based Multimodal Reasoning](#r1-based-multimodal-reasoning)
  - [Thinking with Images](#thinking-with-images)
  - [Multimodal Self-Evolving](#multimodal-self-evolving)
  - [Multimodal Distillation](#multimodal-distillation)

- [Multimodal Domain Adaptation](#multimodal-domain-adaptation)
  - [Domain-oriented Post-Training for Specialized Multimodal Scenarios](#multimodal-domain-adaptation)

- [Multimodal Scalable Training](#multimodal-scalable-training)
  - [LoRA-based Methods](#lora-based-methods)
  - [MoE-based Methods](#moe-based-methods)
  - [Compute-efficient Methods](#compute-efficient-methods)

- [Multimodal Benchmarks](#multimodal-benchmarks)
  - [Instruction Tuning Benchmarks](#instruction-tuning-benchmarks)
  - [Alignment Learning Benchmarks](#alignment-learning-benchmarks)
  - [Reasoning Enhancement Benchmarks](#reasoning-enhancement-benchmarks)
  - [Domain Adaptation Benchmarks](#domain-adaptation-benchmarks)

<p align="center">
  <img src="assets/timelinev4_01.png" width="100%" alt="timeline">
  <span><b>Figure 2. A timeline of MLLMs post-training research.</b></span>
</p>

---

## <img src="assets/icon4.png" height="30" align="top"/> Multimodal Instruction Tuning

* **Visual Instruction Tuning** [NeurIPS 2023] [[Paper](https://arxiv.org/pdf/2304.08485)] [[Code](https://github.com/haotian-liu/LLaVA)] [[Homepage](https://llava-vl.github.io/)] <br>
University of Wisconsin–Madison, Microsoft Research, Columbia University

* **MiniGPT-4: Enhancing Vision-Language Understanding with Advanced Large Language Models** [ICLR 2024] [[Paper](https://arxiv.org/pdf/2304.10592)] [[Code](https://github.com/Vision-CAIR/MiniGPT-4)] [[Homepage](https://minigpt-4.github.io/)] <br>
King Abdullah University of Science and Technology

* **InstructBLIP: Towards General-purpose Vision-Language Models with Instruction Tuning** [NeurIPS 2023] [[Paper](https://arxiv.org/pdf/2305.06500)] [[Code](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip)] <br>
Salesforce Research, Hong Kong University of Science and Technology, Nanyang Technological University, Singapore

* **mPLUG-Owl: Modularization Empowers Large Language Models with Multimodality** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2304.14178)] [[Code](https://github.com/X-PLUG/mPLUG-Owl)] <br>
DAMO Academy, Alibaba Group

* **LLaMA-Adapter V2: Parameter-Efficient Visual Instruction Model** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2304.15010)] [[Code](https://github.com/OpenGVLab/LLaMA-Adapter)] <br>
Shanghai Artificial Intelligence Laboratory, CUHK MMLab, Rutgers University

* **Improved Baselines with Visual Instruction Tuning** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2310.03744)] [[Code](https://github.com/haotian-liu/LLaVA)] [[Homepage](https://llava-vl.github.io/)] <br>
University of Wisconsin–Madison, Microsoft Research, Redmond

* **Qwen-VL: A Versatile Vision-Language Model for Understanding, Localization, Text Reading, and Beyond** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2308.12966)] [[Code](https://github.com/QwenLM/Qwen-VL)] <br>
Alibaba Group

* **CogVLM: Visual Expert for Pretrained Language Models** [NeurIPS 2024] [[Paper](https://arxiv.org/pdf/2311.03079)] [[Code](https://github.com/THUDM/CogVLM)] <br>
Tsinghua University, Zhipu AI

* **InternVL: Scaling up Vision Foundation Models and Aligning for Generic Visual-Linguistic Tasks** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2312.14238)] [[Code](https://github.com/OpenGVLab/InternVL)] <br>
OpenGVLab, Shanghai AI Laboratory, Nanjing University, The University of Hong Kong, The Chinese University of Hong Kong, Tsinghua University, University of Science and Technology of China, SenseTime Research

* **LLaVA-NeXT: Improved Reasoning, OCR, and World Knowledge** [arXiv 2024] [[Code](https://github.com/LLaVA-VL/LLaVA-NeXT)] [[Homepage](https://llava-vl.github.io/blog/2024-01-30-llava-next/)] <br>
University of Wisconsin-Madison, Microsoft Research

* **What matters when building vision-language models?** [NeurIPS 2024] [[Paper](https://arxiv.org/pdf/2405.02246)] [[HF](https://huggingface.co/blog/idefics2)] <br>
Hugging Face, Sorbonne Université

* **Qwen2-VL: Enhancing Vision-Language Model's Perception of the World at Any Resolution** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2409.12191)] [[Code](https://github.com/QwenLM/Qwen2-VL)] <br>
ByteDance, S-Lab, NTU, CUHK, HKUST

* **LLaVA-OneVision: Easy Visual Task Transfer** [TMLR 2025] [[Paper](https://arxiv.org/pdf/2408.03326)] [[Code](https://github.com/LLaVA-VL/LLaVA-NeXT/blob/main/docs/LLaVA_OneVision.md)] [[Homepage](https://llava-vl.github.io/blog/2024-08-05-llava-onevision/)] <br>
ByteDance, S-Lab, NTU, CUHK, HKUST

* **Expanding Performance Boundaries of Open-Source Multimodal Models with Model, Data, and Test-Time Scaling** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2412.05271)] [[Code](https://github.com/OpenGVLab/InternVL)] [[Homepage](https://internvl.github.io/blog/2024-12-05-InternVL-2.5/)] <br>
Shanghai AI Laboratory, SenseTime Research, Tsinghua University, Nanjing University, Fudan University, The Chinese University of Hong Kong, Shanghai Jiao Tong University

* **Qwen2.5-VL Technical Report** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2502.13923)] [[Code](https://github.com/QwenLM/Qwen2.5-VL)] <br>
Alibaba Group

* **VILA: On Pre-training for Visual Language Models** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2312.07533)] [[Code](https://github.com/NVlpdf/VILA)] <br>
NVIDIA, MIT

* **MobileVLM : A Fast, Strong and Open Vision Language Assistant for Mobile Devices** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2312.16886)] [[Code](https://github.com/Meituan-AutoML/MobileVLM)] <br>
Meituan Inc., Zhejiang University, China, Dalian University of Technology, China

* **DeepSeek-VL: Towards Real-World Vision-Language Understanding** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2403.05525)] [[Code](https://github.com/deepseek-ai/DeepSeek-VL)] <br>
DeepSeek-AI

* **Yi: Open Foundation Models by 01.AI** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2403.04652)] [[Code](https://github.com/01-ai/Yi)] [[HF](https://huggingface.co/01-ai/Yi-VL-6B)] <br>
01.AI

* **Cambrian-1: A Fully Open, Vision-Centric Exploration of Multimodal LLMs** [NeurIPS 2024] [[Paper](https://arxiv.org/pdf/2406.16860)] [[Code](https://github.com/cambrian-mllm/cambrian)] [[Homepage](https://cambrian-mllm.github.io/)] <br>
New York University

* **MiniCPM-V: A GPT-4V Level MLLM on Your Phone** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2408.01800)] [[Code](https://github.com/OpenBMB/MiniCPM-V)] [[Homepage](https://huggingface.co/openbmb/MiniCPM-V-2_6)] <br>
OpenBMB

* **Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2404.14219)] [[HF](https://huggingface.co/microsoft/Phi-3.5-vision-instruct)] <br>
Microsoft

* **Llama-3.2-Vision-Instruct** [arXiv 2024] [[HF](https://huggingface.co/meta-llama/Llama-3.2-11B-Vision-Instruct)] [[Homepage](https://www.llama.com/)] <br>
Meta

* **Molmo and PixMo: Open Weights and Open Data for State-of-the-Art Vision-Language Models** [CVPR 2025] [[Paper](https://arxiv.org/pdf/2409.17146)] [[Code](https://github.com/allenai/molmo)] [[Homepage](https://molmo.allenai.org/)] <br>
Allen Institute for AI, University of Washington

* **Pixtral-12B** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2410.07073)] [[Homepage](https://mistral.ai/news/pixtral-12b)] <br>
Mistral AI

* **Comparison Visual Instruction Tuning** [CVPR 2025 Workshop] [[Paper](https://arxiv.org/pdf/2406.09240)] [[Code](https://github.com/wlin-at/CaD-VI)] [[Homepage](https://wlin-at.github.io/cad_vi)] [[HF](https://huggingface.co/datasets/wlin21at/CaD-Inst)] <br>
ELLIS Unit, LIT AI Lab, Institute for Machine Learning, JKU Linz, Austria, TU Graz ICG, Austria, IBM Research, Israel, Weizmann Institute of Science, Israel, Tel-Aviv University, Israel, NXAI GmbH, Austria, MIT-IBM Watson AI Lab, USA

* **PaliGemma: A versatile 3B VLM for transfer** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2407.07726)] [[HF](https://huggingface.co/google/paligemma-3b-mix-224)] <br>
Google DeepMind

* **Otter: A Multi-Modal Model with In-Context Instruction Tuning** [TPAMI 2025] [[Paper](https://arxiv.org/pdf/2305.03726)] [[Code](https://github.com/Luodian/Otter)] <br>
S-Lab, Nanyang Technological University, Microsoft Research

* **LLaMA-Adapter: Efficient Fine-tuning of Language Models with Zero-init Attention** [ICLR 2024] [[Paper](https://arxiv.org/pdf/2303.16199)] [[Code](https://github.com/OpenGVLab/LLaMA-Adapter)] <br>
Shanghai Artificial Intelligence Laboratory, CUHK MMLab, University of California, Los Angeles, CPII of InnoHK

* **Cheap and Quick: Efficient Vision-Language Instruction Tuning for Large Language Models** [NeurIPS 2023] [[Paper](https://arxiv.org/pdf/2305.15023)] [[Code](https://github.com/luogen1996/LaVIN)] <br>
Key Laboratory of Multimedia Trusted Perception and Efficient Computing, Ministry of Education of China, School of Informatics, Xiamen University, 361005, P.R. China., Institute of Artificial Intelligence, Xiamen University, 361005, P.R. China., Peng Cheng Laboratory, Shenzhen, 518000, China.

* **Valley: Video Assistant with Large Language model Enhanced abilitY** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2306.07207)] [[Code](https://github.com/RupertLuo/Valley)] <br>
ByteDance Inc., Fudan University, East China Normal University

* **NExT-GPT: Any-to-Any Multimodal LLM** [ICML 2024] [[Paper](https://arxiv.org/pdf/2309.05519)] [[Code](https://github.com/NExT-GPT/NExT-GPT)] [[Homepage](https://next-gpt.github.io/)] <br>
National University of Singapore

* **InternVL: Scaling up Vision Foundation Models and Aligning for Generic Visual-Linguistic Tasks** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2312.14238)] [[Code](https://github.com/OpenGVLab/InternVL)] <br>
OpenGVLab, Shanghai AI Laboratory, Nanjing University, The University of Hong Kong, The Chinese University of Hong Kong, Tsinghua University, University of Science and Technology of China, SenseTime Research

* **Generative Visual Instruction Tuning** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2406.11262)] [[Code](https://github.com/jeffhernandez1995/GenLlaVA)] <br>
Rice University, Google DeepMind

* **MLAN: Language-Based Instruction Tuning Preserves and Transfers Knowledge in Multimodal Language Models** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2411.10557)] <br>
Washington University in St. Louis, The University of British Columbia, Google Research, Virginia Tech, University of California, Davis, Sony AI, University of California, Berkeley

* **INST-IT: Boosting Instance Understanding via Explicit Visual Prompt Instruction Tuning** [NeurIPS 2025] [[Paper](https://arxiv.org/pdf/2412.03565)] [[Code](https://github.com/inst-it/inst-it)] [[Homepage](https://inst-it.github.io/)] <br>
Institute of Trustworthy Embodied AI, Fudan University, Shanghai Innovation Institute, Huawei Noah, s Ark Lab

* **Learning to Instruct for Visual Instruction Tuning** [NeurIPS 2025] [[Paper](https://arxiv.org/pdf/2503.22215)] [[Code](https://github.com/Feng-Hong/L2T)] <br>
Cooperative Medianet Innovation Center, Shanghai Jiao Tong University, Microsoft Research Asia, Hong Kong Baptist University, School of Artificial Intelligence, Shanghai Jiao Tong University

* **Visual Compositional Tuning** [ICLR 2026 Workshop] [[Paper](https://arxiv.org/pdf/2504.21850)] [[Code](https://github.com/princetonvisualai/compact)] [[Homepage](https://princetonvisualai.github.io/compact/)] <br>
Princeton University, Meta AI

* **Visual Instruction Bottleneck Tuning** [NeurIPS 2025] [[Paper](https://arxiv.org/pdf/2505.13946)] [[Code](https://github.com/deeplearning-wisc/vittle)] <br>
Department of Computer Sciences, University of Wisconsin–Madison

* **LLaDA-V: Large Language Diffusion Models with Visual Instruction Tuning** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2505.16933)] [[Code](https://ml-gsai.github.io/LLaDA-V-demo/)] [[Homepage](https://ml-gsai.github.io/LLaDA-V-demo/)] <br>
Gaoling School of AI, Renmin University of China, Beijing Key Laboratory of Research on Large Models and Intelligent Governance, Engineering Research Center of Next-Generation Intelligent Search and Recommendation, MOE, Ant Group

* **Less Data, Faster Convergence: Goal-Driven Data Optimization for Multimodal Instruction Tuning** [ECCV 2026] [[Paper](https://arxiv.org/pdf/2603.12478)] [[Code](https://github.com/rujiewu/GDO)] <br>
Peking University, University of Illinois at Urbana-Champaign, National University of Singapore

* **LLaVA-NeXT-Interleave: Tackling Multi-image, Video, and 3D in Large Multimodal Models** [ICLR 2025] [[Paper](https://arxiv.org/pdf/2407.07895)] [[Code](https://github.com/LLaVA-VL/LLaVA-NeXT)] [[Homepage](https://llava-vl.github.io/blog/2024-06-16-llava-next-interleave/)] <br>
ByteDance, HKUST, CUHK, NTU

* **MAVIS: Mathematical Visual Instruction Tuning with an Automatic Data Engine** [ICLR 2025] [[Paper](https://arxiv.org/pdf/2407.08739)] [[Code](https://github.com/ZrrSkywalker/MAVIS)] <br>
CUHK, Peking University, Shanghai AI Laboratory, ByteDance, Oracle

* **MANTIS: Interleaved Multi-Image Instruction Tuning** [TMLR 2024] [[Paper](https://arxiv.org/pdf/2405.01483)] [[Code](https://github.com/OpenGVLab/LLaMA-Adapter/tree/main/imagebind_LLM)] [[Homepage](https://tiger-ai-lab.github.io/Mantis/)] <br>
University of Waterloo, Tsinghua University, Sea AI Lab

* **ImageBind-LLM: Multi-modality Instruction Tuning** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2309.03905)] [[Code](https://github.com/OpenGVLab/LLaMA-Adapter/tree/main/imagebind_LLM)] <br>
Shanghai Artificial Intelligence Laboratory, Shanghai, 200030, China., CUHK MMLab, Hong Kong SAR, 999077, China., vivo AI Lab, Shenzhen, 518000, China.

* **ShareGPT4V: Improving Large Multi-Modal Models with Better Captions** [ECCV 2024] [[Paper](https://arxiv.org/pdf/2311.12793)] [[Code](https://github.com/ShareGPT4Omni/ShareGPT4V)] [[Homepage](https://sharegpt4v.github.io/)] <br>
University of Science and Technology of China, Shanghai AI Laboratory

* **MiniGPT-v2: large language model as a unified interface for vision-language multi-task learning** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2310.09478)] [[Code](https://github.com/Vision-CAIR/MiniGPT-4)] [[Homepage](https://minigpt-v2.github.io/)] <br>
King Abdullah University of Science and Technology (KAUST), Meta AI Research

* **ViP-LLaVA: Making Large Multimodal Models Understand Arbitrary Visual Prompts** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2312.00784)] [[Code](https://github.com/WisconsinAIVision/ViP-LLaVA)] [[Homepage](https://vip-llava.github.io/)] <br>
University of Wisconsin–Madison；Cruise LLC

* **MoAI: Mixture of All Intelligence for Large Language and Vision Models** [ECCV 2024] [[Paper](https://arxiv.org/pdf/2403.07508)] [[Code](https://github.com/ByungKwanLee/MoAI)] <br>
School of Electrical Engineering Korea Advanced Institute of Science and Technology (KAIST)

* **Monkey :ImageResolutionandText Label Are Important Things for Large Multi-modal Models** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2311.06607)] [[Code](https://github.com/Yuliang-Liu/Monkey)] <br>
Huazhong University of Science and Technology, Kingsoft Office

* **Mini-Gemini: Mining the Potential of Multi-modality Vision Language Models** [TPAMI 2026] [[Paper](https://arxiv.org/pdf/2403.18814v1)] [[Code](https://github.com/JIA-Lab-research/MGM)] <br>
The Chinese University of Hong Kong；SmartMore

* **Feast Your Eyes: Mixture-of-Resolution Adaptation for Multimodal Large Language Models** [ICLR 2025] [[Paper](https://arxiv.org/pdf/2403.03003)] [[Code](https://github.com/luogen1996/LLaVA-HR)] <br>
Xiamen University

* **SPHINX: The Joint Mixing of Weights, Tasks, and Visual Embeddings for Multi-modal Large Language Models** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2311.07575)] [[Code](https://github.com/Alpha-VLLM/LLaMA2-Accessory)] <br>
Shanghai AI Laboratory；MMLab, CUHK；ShanghaiTech University

---

## <img src="assets/icon5.png" height="30" align="top"/> Multimodal Preference Calibration

### Multimodal RLHF

* **ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF** [ACL Findings 2024] [[Paper](https://arxiv.org/pdf/2309.14525)] [[Code](https://github.com/llava-rlhf/LLaVA-RLHF)] [[Homepage](https://llava-rlhf.github.io/)] <br>
UC Berkeley, Carnegie Mellon University, University of Illinois Urbana-Champaign, University of Wisconsin-Madison, University of Massachusetts Amherst, Microsoft Research, MIT-IBM Watson AI Lab

* **RLHF-V: Towards Trustworthy MLLMs via Behavior Alignment from Fine-grained Correctional Human Feedback** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2312.00849)] [[Code](https://github.com/RLHF-V/RLHF-V)] [[Homepage](https://rlhf-v.github.io/)] <br>
Tsinghua University, National University of Singapore

* **VisualPRM: An Effective Process Reward Model for Multimodal Reasoning** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2503.10291)] [[Homepage](https://internvl.github.io/blog/2025-03-13-VisualPRM/)] <br>
Shanghai AI Laboratory, SenseTime Research, Zhejiang University

* **Gemini: A Family of Highly Capable Multimodal Models** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2312.11805)] [[Homepage](https://deepmind.google/technologies/gemini/)] <br>
Google

* **Seed1.5-VL Technical Report** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2505.07062)] [[Code](https://github.com/ByteDance-Seed/Seed1.5-VL)] [[Homepage](https://seed.bytedance.com/en/tech/seed1_5_vl)] <br>
ByteDance Seed

* **MiMo-VL Technical Report** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2506.03569)] [[Code](https://github.com/XiaomiMiMo/MiMo-VL)] <br>
LLM-Core Xiaomi

### Multimodal RLAIF

* **Tuning Large Multimodal Models for Videos using Reinforcement Learning from AI Feedback** [ACL 2024] [[Paper](https://arxiv.org/pdf/2402.03746)] [[Code](https://github.com/yonseivnl/vlm-rlaif)] [[Homepage](https://dcahn12.github.io/projects/vlm-rlaif/)] <br>
Yonsei University, University of Minnesota, Seoul National University

* **RLAIF-V: Open-Source AI Feedback Leads to Super GPT-4V Trustworthiness** [CVPR 2025] [[Paper](https://arxiv.org/pdf/2405.17220)] [[Code](https://github.com/RLHF-V/RLAIF-V)] <br>
Tsinghua University, Shanghai Qi Zhi Institute, Harbin Institute of Technology, Taobao & Tmall Group of Alibaba, Peng Cheng Laboratory, National University of Singapore

* **Oracle-RLAIF: An Improved Fine-Tuning Framework for Multi-modal Video Models using Reinforcement Learning from Ranking Feedback** [arXiv 2025] [[Paper](https://arxiv.org/abs/2510.02561)] <br>
Stanford University, xAI, Microsoft

### Multimodal Direct Preference Optimization

* **Silkie: Preference Distillation for Large Visual Language Models** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2312.10665)] [[Code](https://github.com/vlf-silkie/VLFeedback)] [[Homepage](https://vlf-silkie.github.io/)] <br>
University of Hong Kong, The Chinese University of Hong Kong, Shenzhen, Peng Cheng Laboratory

* **Direct Preference Optimization of Video Large Multimodal Models from Language Model Reward** [NAACL 2025] [[Paper](https://arxiv.org/pdf/2404.01258)] [[Code](https://github.com/RifleZhang/LLaVA-Hound-DPO)] <br>
CMULTI, Bytedance, UT Austin, Columbia University, NTU

* **ISR-DPO: Aligning Large Multimodal Models for Videos by Iterative Self-Retrospective DPO** [AAAI 2025] [[Paper](https://arxiv.org/pdf/2406.11280)] [[Code](https://github.com/snumprlab/isr-dpo)] [[Homepage](https://dcahn12.github.io/projects/isr-dpo/)] <br>
Seoul National University, Yonsei University, University of Minnesota

* **Beyond Hallucinations: Enhancing LVLMs through Hallucination-Aware Direct Preference Optimization** [arXiv 2023] [[Paper](https://arxiv.org/pdf/2311.16839)] [[Code](https://github.com/opendatalab/HA-DPO)] [[Homepage](https://opendatalab.github.io/HA-DPO/)] <br>
Shanghai AI Laboratory

* **Mitigating Hallucination in Multimodal Large Language Model via Hallucination-targeted Direct Preference Optimization** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2411.10436)] <br>
Key Lab of DEKE, Renmin University of China, Machine Learning Platform Department, Tencent

* **V-DPO: Mitigating Hallucination in Large Vision Language Models via Vision-Guided Direct Preference Optimization** [EMNLP 2024] [[Paper](https://arxiv.org/pdf/2411.02712)] [[Code](https://github.com/YuxiXie/V-DPO)] <br>
National University of Singapore

* **CLIP-DPO: Vision-Language Models as a Source of Preference for Fixing Hallucinations in LVLMs** [ECCV 2024] [[Paper](https://arxiv.org/pdf/2408.10433)] <br>
Samsung AI Center Cambridge, UK, Technical University of Iasi, Romania, Queen Mary University of London, UK

* **Mitigating Hallucinations in Multimodal LLMs via Object-aware Preference Optimization** [BMVC 2025] [[Paper](https://arxiv.org/pdf/2508.20181)] [[Code](https://github.com/aimagelab/CHAIR-DPO)] <br>
University of Modena and Reggio Emilia

* **MDPO: Conditional Preference Optimization for Multimodal Large Language Models** [EMNLP 2024] [[Paper](https://arxiv.org/pdf/2406.11839)] [[Code](https://github.com/luka-group/mDPO)] [[Homepage](https://feiwang96.github.io/mDPO/)] <br>
University of Southern California, Microsoft Research, University of California, Davis

* **PEA-DPO: Perception-Enhanced Alignment Direct Preference Optimization for MLLMs Alignment** [OpenReview 2026] [[Homepage](https://openreview.net/forum?id=uZ5AmOJKqV)] <br>
University of Science and Technology of China

* **MoD-DPO: Towards Mitigating Cross-modal Hallucinations in Omni LLMs using Modality Decoupled Preference Optimization** [CVPR 2026] [[Paper](https://arxiv.org/pdf/2603.03192)] [[Homepage](https://mod-dpo.github.io/)] <br>
University of Southern California

* **OMNI DPO: A Preference Optimization Framework to Address Omni-Modal Hallucination** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2509.00723)] <br>
Tsinghua University, Hong Kong University of Science and Technology (Guangzhou), OpenRL, Chongqing University

* **DA-DPO: Cost-efficient Difficulty-aware Preference Optimization for Reducing MLLM Hallucinations** [TMLR 2025] [[Paper](https://arxiv.org/pdf/2601.00623)] [[Code](https://github.com/Artanic30/DA-DPO)] [[Homepage](https://artanic30.github.io/project_pages/DA-DPO/)] <br>
ShanghaiTech University, Lingang Laboratory, Shanghai Engineering Research Center of Intelligent Vision and Imaging

* **Uncertainty-Aware Exploratory Direct Preference Optimization for Multimodal Large Language Models** [arXiv 2026] [[Paper](https://arxiv.org/pdf/2605.04874)] <br>
University of Science and Technology of China

* **Mitigating Hallucinations in Large Vision-Language Models via DPO: On-Policy Data Hold the Key** [CVPR 2025] [[Paper](https://arxiv.org/pdf/2501.09695)] [[Code](https://github.com/zhyang2226/OPA-DPO)] [[Homepage](https://opa-dpo.github.io/)] <br>
The Chinese University of Hong Kong, Microsoft Research Asia, The Chinese University of Hong Kong, Shenzhen Research Institute

* **LPOI: Listwise Preference Optimization for Vision Language Models** [ACL 2025] [[Paper](https://arxiv.org/pdf/2505.21061)] [[Code](https://github.com/fatemehpesaran310/lpoi)] <br>
Seoul National University

---

## <img src="assets/icon6.png" height="30" align="top"/> Multimodal Reason Enhancement

### R1-based Multimodal Reasoning

* **LMM-R1: Empowering 3B LMMs with Strong Reasoning Abilities Through Two-Stage Rule-Based RL** [arXiv 2025] [[Paper](https://arxiv.org/abs/2503.07536)] [[Code](https://github.com/GlowLED/lmm-r1-ascend)] [[Homepage](https://forjadeforest.github.io/LMM-R1-ProjectPage/)] <br>
Southeast University, The Chinese University of Hong Kong, Fudan University, Ant Group

* **VLM-R1: A Stable and Generalizable R1-style Large Vision-Language Model** [arXiv 2025] [[Paper](https://arxiv.org/abs/2504.07615)] [[Code](https://github.com/om-ai-lab/VLM-R1)] <br>
OM AI Lab

* **Visual-RFT: Visual Reinforcement Fine-Tuning** [ICCV 2025] [[Paper](https://arxiv.org/abs/2503.01785)] [[Code](https://github.com/Liuziyu77/Visual-RFT)] <br>
Shanghai AI Laboratory, The Chinese University of Hong Kong (CUHK)

* **Vision-R1: Incentivizing Reasoning Capability in Multimodal Large Language Models** [ICLR 2026] [[Paper](https://arxiv.org/abs/2503.06749)] [[Code](https://github.com/Osilly/Vision-R1)] <br>
East China Normal University, Xiaohongshu Inc.

* **VideoChat-R1: Enhancing Spatio-Temporal Perception via Reinforcement Fine-Tuning** [arXiv 2025] [[Paper](https://arxiv.org/abs/2504.06958)] [[Code](https://github.com/OpenGVLab/VideoChat-R1)] <br>
Nanjing University, Shanghai AI Laboratory, The Chinese University of Hong Kong, Shenzhen

* **Video-R1: Reinforcing Video Reasoning in MLLMs** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2503.21776)] [[Code](https://github.com/tulerfeng/Video-R1)] <br>
MMLab, The Chinese University of Hong Kong (CUHK), DataWhale, The Chinese University of Hong Kong, Shenzhen

* **VisualPRM: An Effective Process Reward Model for Multimodal Reasoning** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2503.10291)] [[Homepage](https://internvl.github.io/blog/2025-03-13-VisualPRM/)] <br>
Shanghai AI Laboratory, SenseTime Research, Zhejiang University

* **R1-VL: Learning to Reason with Multimodal Large Language Models via Step-wise Group Relative Policy Optimization** [ICCV 2025] [[Paper](https://arxiv.org/abs/2503.12937)] <br>
Nanyang Technological University (NTU), Nankai University, JD Explore Academy

* **R1-Zero's "Aha Moment" in Visual Reasoning on a 2B Non-SFT Model** [arXiv 2025] [[Paper](https://arxiv.org/abs/2503.05132)] [[Code](https://github.com/turningpoint-ai/VisualThinker-R1-Zero)] <br>
University of California, Los Angeles (UCLA), TurningPoint AI

* **MM-Eureka: Exploring the Frontiers of Multimodal Reasoning with Rule-based Reinforcement Learning** [arXiv 2025] [[Paper](https://arxiv.org/abs/2503.07365)] [[Code](https://github.com/ModalMinds/MM-EUREKA)] [[HF](https://huggingface.co/FanqingM/MM-Eureka-8B)] <br>
Shanghai AI Laboratory, SenseTime, The University of Hong Kong

* **R1-Onevision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization** [arXiv 2025] [[Paper](https://arxiv.org/abs/2503.10615)] [[Code](https://github.com/Fancy-MLLM/R1-onevision)] <br>
Alibaba Group

* **R1-Omni: Explainable Omni-Multimodal Emotion Recognition with Reinforcement Learning** [arXiv 2025] [[Paper](https://arxiv.org/abs/2503.05379)] [[Code](https://github.com/HumanMLLM/R1-Omni)] <br>
Alibaba Group, Tongji University

* **Retrv-R1: A Reasoning-Driven MLLM Framework for Universal and Efficient Multimodal Retrieval** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2510.02745)] [[Code](https://lanyunzhu.site/RetrvR1/)] [[Homepage](https://lanyunzhu.site/RetrvR1/)] <br>
City University of Hong Kong

### Thinking with Images

* **GRIT: Teaching MLLMs to Think with Images** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2505.15879)] [[Code](https://github.com/eric-ai-lab/GRIT)] [[Homepage](https://grounded-reasoning.github.io/)] <br>
University of California, Santa Cruz (UCSC)

* **Point-RFT: Improving Multimodal Reasoning with Visually Grounded Reinforcement Finetuning** [arXiv 2025] [[Paper](https://arxiv.org/abs/2505.19702)] <br>
Harbin Institute of Technology, Microsoft Research

* **OpenThinkIMG: Learning to Think with Images via Visual Tool Reinforcement Learning** [arXiv 2025] [[Paper](https://arxiv.org/abs/2505.08617)] [[Code](https://github.com/OpenThinkIMG/OpenThinkIMG)] [[HF](https://huggingface.co/collections/Warrieryes/openthinkimg)] <br>
Shanghai Jiao Tong University, Microsoft Research, The Chinese University of Hong Kong (CUHK)

* **VisionReasoner: Unified Reasoning-Integrated Visual Perception via Reinforcement Learning** [arXiv 2025] [[Paper](https://arxiv.org/abs/2505.12081)] [[Code](https://github.com/dvlab-research/VisionReasoner)] <br>
The Chinese University of Hong Kong (CUHK), SmartMore

* **DeepEyes: Incentivizing "Thinking with Images" via Reinforcement Learning** [ICLR 2026] [[Paper](https://arxiv.org/abs/2505.14362)] [[Code](https://github.com/Visual-Agent/DeepEyes)] [[HF](https://huggingface.co/ChenShawn/DeepEyes-7B)] <br>
Visual Agent

* **VTool-R1: VLMs Learn to Think with Images via Reinforcement Learning on Multimodal Tool Use** [ICLR 2026] [[Paper](https://arxiv.org/abs/2505.19255)] [[Code](https://github.com/VTOOL-R1/vtool-r1)] [[Homepage](https://vtool-r1.github.io/)] <br>
University of Illinois Urbana-Champaign (UIUC), University of Michigan

* **Visual Planning: Let's Think Only with Images** [ICLR 2026] [[Paper](https://arxiv.org/abs/2505.11409)] [[Code](https://github.com/yix8/VisualPlanning)] <br>
University of Cambridge

* **LanteRn: Latent Visual Structured Reasoning** [arXiv 2026] [[Paper](https://arxiv.org/abs/2603.25629)] [[Code](https://github.com/GuilhermeViveiros/LantErn)] [[HF](https://huggingface.co/AGViveiros/LanteRn-3B-RL)] <br>
Instituto Superior Técnico, TU Darmstadt

### Multimodal Self-Evolving

* **VIGC: Visual Instruction Generation and Correction** [AAAI 2024] [[Paper](https://arxiv.org/abs/2308.12714)] [[Code](https://github.com/opendatalab/VIGC)] [[Homepage](https://opendatalab.github.io/VIGC)] <br>
Shanghai AI Laboratory, SenseTime

* **MindGYM: Enhancing Vision-Language Models via Synthetic Self-Challenging Questions** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2503.09499)] [[Code](https://github.com/modelscope/data-juicer/tree/MindGYM)] <br>
Sun Yat-sen University, Alibaba Group

* **SRPO: Enhancing Multimodal LLM Reasoning via Reflection-Aware Reinforcement Learning** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2506.01713)] [[Code](https://github.com/SUSTechBruce/SRPO_MLLMs)] [[Homepage](https://srpo.pages.dev/)] <br>
ByteDance Seed

* **LLaVA-Critic: Learning to Evaluate Multimodal Models** [CVPR 2025] [[Paper](https://arxiv.org/pdf/2410.02712)] [[Code](https://github.com/LLaVA-VL/LLaVA-NeXT)] [[Homepage](https://llava-vl.github.io/blog/2024-10-03-llava-critic/)] <br>
University of Maryland, ByteDance

* **MM-UPT: Unsupervised Post-Training for Multi-Modal LLM Reasoning via GRPO** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2505.22453)] [[Code](https://github.com/waltonfuture/MM-UPT)] [[HF](https://huggingface.co/WaltonFuture/Qwen2.5-VL-7B-MM-UPT-MMR1)] <br>
Shanghai Jiao Tong University, Lehigh University

* **LLaVA-Critic-R1: Your Critic Model is Secretly a Strong Policy Model** [arXiv 2025] [[Paper](https://arxiv.org/abs/2509.00676)] [[Code](https://github.com/LLaVA-VL/LLaVA-NeXT)] <br>
University of Maryland, Microsoft Research

### Multimodal Distillation

* **LLaVA-KD: A Framework of Distilling Multimodal Large Language Models** [ICCV 2025] [[Paper](https://arxiv.org/abs/2410.16236)] [[Code](https://github.com/Fantasyele/LLaVA-KD)] <br>
Huazhong University of Science and Technology, Tencent Youtu Lab

* **LLAVADI: What Matters For Multimodal Large Language Models Distillation** [arXiv 2024] [[Paper](https://arxiv.org/abs/2407.19409)] <br>
Peking University, Nanyang Technological University, University of California, Merced

* **LLaVA-MoD: Making LLaVA Tiny via MoE Knowledge Distillation** [arXiv 2024] [[Paper](https://arxiv.org/abs/2408.15881)] [[Code](https://github.com/shufangxun/LLaVA-MoD)] <br>
MBZUAI, Alibaba Group, The Chinese University of Hong Kong (CUHK)

* **Video-OPD: Efficient Post-Training of Multimodal Large Language Models for Temporal Video Grounding via On-Policy Distillation** [arXiv 2026] [[Paper](https://arxiv.org/abs/2602.02994)] <br>
Tencent AI Lab

* **X-OPD: Cross-Modal On-Policy Distillation for Capability Alignment in Speech LLMs** [arXiv 2026] [[Paper](https://arxiv.org/abs/2603.24596)] <br>
Kuaishou, Microsoft Research Asia

* **Uni-OPD: Unifying On-Policy Distillation with a Dual-Perspective Recipe** [arXiv 2026] [[Paper](https://arxiv.org/abs/2605.03677)] [[Code](https://github.com/WenjinHou/Uni-OPD)] <br>
Zhejiang University, Alibaba Group

* **Vision-OPD: Learning to See Fine Details for Multimodal LLMs via On-Policy Self-Distillation** [arXiv 2026] [[Paper](https://arxiv.org/abs/2605.18740)] [[Code](https://github.com/VisionOPD/Vision-OPD)] <br>
Institute of Software, Chinese Academy of Sciences

* **VA-OPD: Visual-Advantage On-Policy Distillation for Vision-Language Models** [arXiv 2026] [[Paper](https://arxiv.org/abs/2605.21924)] <br>
Institute of Automation, Chinese Academy of Sciences, Meituan

---

## Multimodal Domain Adaptation

* **Mobile-Agent: Autonomous Multi-Modal Mobile Device Agent with Visual Perception** [ICLR 2024 Workshop] [[Paper](https://arxiv.org/pdf/2401.16158)] [[Code](https://github.com/X-PLUG/MobileAgent)] <br>
Beijing Jiaotong University, Alibaba Group

* **GUI-R1: A Generalist R1-Style Vision-Language Action Model For GUI Agents** [arXiv 2025] [[Paper](https://arxiv.org/abs/2504.10458)] [[Code](https://github.com/ritzz-ai/GUI-R1)] <br>
National University of Singapore, Chinese Academy of Sciences, University of Chinese Academy of Sciences

* **mPLUG-DocOwl 1.5: Unified Structure Learning for OCR-free Document Understanding** [EMNLP 2024] [[Paper](https://arxiv.org/abs/2403.12895)] [[Code](https://github.com/X-PLUG/mPLUG-DocOwl)] <br>
Alibaba Group

* **LLaVA-UHD: an LMMPerceiving Any Aspect Ratio and High-Resolution Images** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2403.11703)] [[Code](https://github.com/thunlp/LLaVA-UHD)] <br>
Ruyi Xu, Yuan Yao, Zonghao Guo, Junbo Cui, Zanlin Ni, Chunjiang Ge, Tat-Seng Chua, Zhiyuan Liu, Maosong Sun, Gao Huang

* **Advancing Multimodal Medical Capabilities of Gemini** [arXiv 2024] [[Paper](https://arxiv.org/abs/2405.03162)] [[Homepage](https://research.google/blog/advancing-medical-ai-with-med-gemini/)] <br>
Google Research, Google DeepMind, Verily Life Sciences, Apollo Radiology International, Northwestern Medicine, EyePACS, DeepHealth/RadNet

* **On Domain-Specific Post-Training for Multimodal Large Language Models** [EMNLP 2025 Findings] [[Paper](https://arxiv.org/abs/2411.19930)] [[Code](https://github.com/thunlp/AdaMLLM)] [[Homepage](https://adamllm.github.io/)] <br>
BIGAI, Beihang University, Tsinghua University, Beijing Institute of Technology, Renmin University of China

---

## Multimodal Scalable Training

### LoRA-based Methods

* **LLaVA-MoLE: Sparse Mixture of LoRA Experts for Mitigating Data Conflicts in Instruction Finetuning MLLMs** [arXiv 2024] [[Paper](https://arxiv.org/abs/2401.16160)] [[Code](https://github.com/forwchen/LLaVA-MoLE)] <br>
Meituan Inc.

* **MixLoRA: Enhancing Large Language Models Fine-Tuning with LoRA-based Mixture of Experts** [arXiv 2024] [[Paper](https://arxiv.org/abs/2404.15159)] [[Code](https://github.com/TUDB-Labs/MixLoRA)] <br>
Sichuan University, Purdue University, Nanyang Technological University, Emory University

* **MoKA: Mixture of Kronecker Adapters** [arXiv 2025] [[Paper](https://arxiv.org/abs/2506.05191)] [[Code](https://github.com/GeWu-Lab/MokA)] [[Homepage](https://gewu-lab.github.io/MokA/)] <br>
Renmin University of China, Beijing Key Laboratory of Research on Large Models and Intelligent Governance, Engineering Research Center of Next-Generation Intelligent Search and Recommendation, Shanghai AI Laboratory

* **LoRA in LoRA: Towards Parameter-Efficient Architecture Expansion for Continual Visual Instruction Tuning** [AAAI 2026] [[Paper](https://arxiv.org/abs/2508.06202)] [[Code](https://github.com/chanceche/LiLoRA)] <br>
Hefei University of Technology, University of Amsterdam, Tsinghua University

### MoE-based Methods

* **MoE-LLaVA: Mixture of Experts for Large Vision-Language Models** [TMM 2025] [[Paper](https://arxiv.org/abs/2401.15947)] [[Code](https://github.com/PKU-YuanGroup/MoE-LLaVA)] <br>
Peking University

* **MoE-LLaVA-7B** [TMM 2025] [[Paper](https://arxiv.org/abs/2401.15947)] [[Code](https://github.com/PKU-YuanGroup/MoE-LLaVA)] <br>
Peking University

* **MoExtend: Tuning New Experts for Modality and Task Extension** [ACL SRW 2024] [[Paper](https://arxiv.org/abs/2408.03511)] [[Code](https://github.com/zhongshsh/MoExtend)] <br>
Sun Yat-sen University, Harvard University, Singapore Management University

* **Qwen2-VL: Enhancing Vision-Language Model's Perception of the World at Any Resolution** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2409.12191)] [[Code](https://github.com/deepseek-ai/DeepSeek-VL2)] <br>
ByteDance, S-Lab, NTU, CUHK, HKUST

* **Qwen3-Omni Technical Report** [arXiv 2025] [[Paper](https://arxiv.org/abs/2509.17765)] [[Code](https://github.com/QwenLM/Qwen3-Omni)] <br>
Qwen Team, Alibaba Cloud

* **Qwen3-VL Technical Report** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2511.21631)] [[Code](https://github.com/QwenLM/Qwen3-VL)] <br>
Qwen Team, Alibaba Cloud

* **MiniMax-01: Scaling Foundation Models with Lightning Attention** [arXiv 2025] [[Paper](https://arxiv.org/abs/2501.08313)] [[Code](https://github.com/MiniMax-AI/MiniMax-01)] <br>
MiniMax

* **Seed1.5-VL Technical Report** [arXiv 2025] [[Paper](https://arxiv.org/pdf/2505.07062)] [[Code](https://github.com/ByteDance-Seed/Seed1.5-VL)] [[Homepage](https://seed.bytedance.com/en/tech/seed1_5_vl)] <br>
ByteDance Seed

### Compute-efficient Methods

#### Efficient Visual Processing (EVP)

* **LLaVA-UHD: an LMMPerceiving Any Aspect Ratio and High-Resolution Images** [arXiv 2024] [[Paper](https://arxiv.org/pdf/2403.11703)] [[Code](https://github.com/thunlp/LLaVA-UHD)] <br>
Ruyi Xu, Yuan Yao, Zonghao Guo, Junbo Cui, Zanlin Ni, Chunjiang Ge, Tat-Seng Chua, Zhiyuan Liu, Maosong Sun, Gao Huang

* **Learning to Inference Adaptively for Multimodal Large Language Models** [ICCV 2025] [[Paper](https://arxiv.org/abs/2503.10905)] [[Code](https://github.com/zhuoyan-xu/AdaLLaVA)] [[Homepage](https://zhuoyan-xu.github.io/ada-llava/)] <br>
University of Wisconsin-Madison, Purdue University, The University of Hong Kong

* **InternVL2: Better than the Best-Expanding Performance Boundaries of Open-Source Multimodal Models with the Progressive Scaling Strategy** [arXiv 2024] [[Code](https://github.com/OpenGVLab/InternVL)] [[Homepage](https://internvl.github.io/blog/2024-07-02-InternVL-2.0/)] <br>
OpenGVLab, Shanghai AI Laboratory

* **UReader: Universal OCR-free Visually-situated Language Understanding with Multimodal Large Language Model** [EMNLP 2023] [[Paper](https://arxiv.org/abs/2310.05126)] [[Code](https://github.com/LukcyYuan/UReader)] <br>
Alibaba Group

* **Monkey:ImageResolutionandText Label Are Important Things for Large Multi-modal Models** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2311.06607)] [[Code](https://github.com/Yuliang-Liu/Monkey)] <br>
Huazhong University of Science and Technology, Kingsoft Office

#### Token Compression (TC)

* **An Image is Worth 1/2 Tokens After Layer 2: Plug-and-Play Inference Acceleration for Large Vision-Language Models** [ECCV 2024] [[Paper](https://arxiv.org/pdf/2403.06764)] [[Code](https://github.com/pkuliyi2015/FastV)] <br>
National Key Laboratory for Multimedia Information Processing, Peking University, Alibaba Group

* **VisionZip: Longer is Better but Not Necessary in Vision Language Models** [CVPR 2025] [[Paper](https://arxiv.org/abs/2412.04467)] [[Code](https://github.com/dvlab-research/VisionZip)] <br>
The Chinese University of Hong Kong, The Hong Kong University of Science and Technology, Harbin Institute of Technology, Shenzhen

* **SparseVLM: Visual Token Sparsification for Efficient Vision-Language Model Inference** [ICML 2025] [[Paper](https://arxiv.org/abs/2410.04417)] [[Code](https://github.com/Gumpest/SparseVLMs)] [[Homepage](https://leofan90.github.io/SparseVLMs.github.io/)] <br>
Peking University, Fudan University, University of California Berkeley, Panasonic Holdings Corporation

* **TokenPacker: Efficient Visual Projector for Multimodal LLM** [IJCV 2025] [[Paper](https://arxiv.org/abs/2407.02392)] [[Code](https://github.com/CircleRadon/TokenPacker)] <br>
Zhejiang University, Ant Group, Nanjing University of Aeronautics and Astronautics, The Hong Kong Polytechnic University

#### Long-Context Optimization (LCO)

* **BIOSCAN-5M: A Multimodal Dataset for Insect Biodiversity** [NeurIPS 2024] [[Paper](https://arxiv.org/pdf/2406.12723)] [[Code](https://github.com/long-vu/LongVU)] [[Homepage](https://long-vu.github.io/)] <br>
Centre for Biodiversity Genomics, University of Guelph, University of Waterloo, Simon Fraser University, Vector Institute, Institute (Amii), Aalborg University and Pioneer Centre for AI

* **LongVILA: Scaling Long-Context Visual Language Models for Long Videos** [ICLR 2025] [[Paper](https://arxiv.org/abs/2408.10188)] [[Code](https://github.com/NVlabs/LongVILA)] <br>
NVIDIA, MIT

* **Long Context Transfer from Language to Vision** [TMLR 2025] [[Paper](https://arxiv.org/abs/2406.16852)] [[Code](https://github.com/EvolvingLMMs-Lab/LongVA)] <br>
LMMs-Lab, S-Lab, Nanyang Technological University, Singapore University of Technology and Design

* **An Image Grid Can Be Worth a Video: Zero-shot Video Question Answering Using a VLM** [IEEE Access 2024] [[Paper](https://arxiv.org/abs/2403.18406)] [[Code](https://github.com/imagegridworth/IG-VLM)] <br>
Seoul National University

* **VideoChat-Flash: Hierarchical Compression for Long-Context Video Modeling** [arXiv 2025] [[Paper](https://arxiv.org/abs/2501.00574)] [[Code](https://github.com/OpenGVLab/VideoChat-Flash)] <br>
Shanghai AI Laboratory, Nanjing University, Shenzhen Institutes of Advanced Technology, Chinese Academy of Sciences, Shanghai Innovation Institute

---

## Multimodal Benchmarks

### Instruction Tuning Benchmarks

* **Visual Instruction Tuning** [NeurIPS 2023] [[Paper](https://arxiv.org/pdf/2304.08485)] [[Code](https://github.com/haotian-liu/LLaVA)] [[Data](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K)] <br>
University of Wisconsin–Madison, Microsoft Research, Columbia University

* **SEED-Bench: Benchmarking Multimodal LLMs with Generative Comprehension** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2307.16125)] [[Code](https://github.com/AILab-CVC/SEED-Bench)] [[Data](https://huggingface.co/datasets/AILab-CVC/SEED-Bench)] <br>
Tencent AI Lab, ARC Lab, Tencent PCG

* **MM-Vet** [ICML 2024] [[Paper](https://arxiv.org/abs/2308.02490)] [[Code](https://github.com/yuweihao/MM-Vet)] [[Data](https://huggingface.co/datasets/zhiqings/MM-Vet)] <br>
National University of Singapore, Microsoft Azure AI

* **MMBench: Is Your Multi-modal Model an All-around Player?** [ECCV 2024] [[Paper](https://arxiv.org/abs/2307.06281)] [[Code](https://github.com/open-compass/MMBench)] [[Data](https://huggingface.co/datasets/lmms-lab/MMBench)] <br>
Shanghai AI Laboratory, Nanyang Technological University, The Chinese University of Hong Kong, National University of Singapore, Zhejiang University

* **ShareGPT4V: Improving Large Multi-Modal Models with Better Captions** [ECCV 2024] [[Paper](https://arxiv.org/pdf/2311.12793)] [[Code](https://github.com/ShareGPT4Omni/ShareGPT4V)] [[Data](https://sharegpt4v.github.io/)] <br>
University of Science and Technology of China, Shanghai AI Laboratory

* **MIA-Bench** [ICLR 2025] [[Paper](https://machinelearning.apple.com/research/towards-better-instruction-following)] [[Code](https://github.com/apple/ml-mia-bench)] [[Data](https://huggingface.co/datasets/apple/MIA-Bench)] <br>
Apple, The Hong Kong University of Science and Technology

* **MM-IFEngine: Towards Multimodal Instruction Following** [ICCV 2025] [[Paper](https://arxiv.org/abs/2504.07957)] [[Code](https://github.com/SYuan03/MM-IFEngine)] [[Data](https://huggingface.co/datasets/ChrisDing1105/MMIF-23k)] [[Homepage](https://syuan03.github.io/MM-IFEngine/)] <br>
Fudan University, Shanghai Innovation Institute

* **MME: A Comprehensive Evaluation Benchmark for Multimodal Large Language Models** [NeurIPS 2025] [[Paper](https://arxiv.org/abs/2306.13394)] [[Code](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models/tree/Evaluation)] [[Data](https://huggingface.co/datasets/lmms-lab/MME)] <br>
Nanjing University, Tencent Youtu Lab, Xiamen University, CASIA

* **Empowering Reliable Visual-Centric Instruction Following in MLLMs** [ACL Findings 2026] [[Paper](https://arxiv.org/abs/2601.03198)] [[Code](https://github.com/KerenWLHe/VC-IFEval)] [[Data](https://huggingface.co/datasets/KerenStone/VCIF-10k)] <br>
The Hong Kong University of Science and Technology, Pennsylvania State University

**Others:** VQAv2, GQA, OK-VQA, TextVQA, VizWiz, Visual7W, BLINK, MME-RealWorld, M3IT, ShareGPT4Video, VideoMME

### Alignment Learning Benchmarks

* **Evaluating Object Hallucination in Large Vision-Language Models** [EMNLP 2023] [[Paper](https://arxiv.org/pdf/2305.10355)] [[Code](https://github.com/RUCAIBox/POPE)] [[Data](https://huggingface.co/datasets/rucaibox/pope)] <br>
Gaoling School of Artificial Intelligence, Renmin University of China, School of Information, Renmin University of China, Beijing Key Laboratory of Big Data Management and Analysis Methods, Meituan Group

* **ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF** [ACL Findings 2024] [[Paper](https://arxiv.org/pdf/2309.14525)] [[Code](https://github.com/Shengcao-Cao/MMHal-Bench)] [[Data](https://huggingface.co/datasets/Shengcao/MMHal-Bench)] <br>
UC Berkeley, Carnegie Mellon University, University of Illinois Urbana-Champaign, University of Wisconsin-Madison, University of Massachusetts Amherst, Microsoft Research, MIT-IBM Watson AI Lab

* **AMBER: An LLM-free Multi-dimensional Benchmark for MLLMs Hallucination Evaluation** [arXiv 2023] [[Paper](https://arxiv.org/abs/2311.07397)] [[Code](https://github.com/junyangwang0410/AMBER)] [[Data](https://huggingface.co/datasets/junyangwang0410/AMBER)] <br>
Beijing Jiaotong University, Alibaba Group, Peng Cheng Laboratory

* **HallusionBench: An Advanced Diagnostic Suite for Entangled Language Hallucination and Visual Illusion in Large Vision-Language Models** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2310.14566)] [[Code](https://github.com/tianyi-lab/HallusionBench)] [[Data](https://huggingface.co/datasets/tianyi-lab/HallusionBench)] <br>
University of Maryland, College Park

* **ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF** [ACL Findings 2024] [[Paper](https://arxiv.org/pdf/2309.14525)] [[Code](https://github.com/llava-rlhf/LLaVA-RLHF)] [[Data](https://huggingface.co/datasets/zhiqings/LLaVA-RLHF-Data)] <br>
UC Berkeley, Carnegie Mellon University, University of Illinois Urbana-Champaign, University of Wisconsin-Madison, University of Massachusetts Amherst, Microsoft Research, MIT-IBM Watson AI Lab

* **RLHF-V: Towards Trustworthy MLLMs via Behavior Alignment from Fine-grained Correctional Human Feedback** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2312.00849)] [[Code](https://github.com/RLHF-V/RLHF-V)] [[Data](https://huggingface.co/datasets/OpenGVLab/RLHF-V-Dataset)] <br>
Tsinghua University, National University of Singapore

* **Safety Fine-Tuning at (Almost) No Cost: A Baseline for Vision Large Language Models** [ICML 2024] [[Paper](https://arxiv.org/abs/2402.02207)] [[Code](https://github.com/ys-zong/VLGuard)] [[Data](https://huggingface.co/datasets/ys-zong/VLGuard)] [[Homepage](https://ys-zong.github.io/VLGuard/)] <br>
University of Edinburgh, EPFL

* **SPA-VL: A Comprehensive Safety Preference Alignment Dataset for Vision Language Models** [CVPR 2025] [[Paper](https://arxiv.org/abs/2406.12030)] [[Code](https://github.com/echosechen/spa-vl-rlhf)] [[Data](https://huggingface.co/datasets/sqrti/SPA-VL)] <br>
University of Science and Technology of China, Shanghai AI Laboratory

* **Lingua-SafetyBench: A Benchmark for Safety Evaluation of Multilingual Vision-Language Models** [arXiv 2026] [[Paper](https://arxiv.org/abs/2601.22737)] [[Code](https://github.com/zsxr15/Lingua-SafetyBench)] [[Data](https://huggingface.co/datasets/yuhuayustc/Lingua-SafetyBench)] <br>
Nanjing University of Science and Technology, University of Wisconsin-Madison, University of Chinese Academy of Sciences, National University of Singapore

**Others:** CHAIR, M-HalDetect, HaELM, MM-SafetyBench, FigStep, JailBreakV-28K, RTVLM

### Reasoning Enhancement Benchmarks

* **Learn to Explain: Multimodal Reasoning via Thought Chains for Science Question Answering** [NeurIPS 2022] [[Paper](https://arxiv.org/pdf/2209.09513)] [[Code](https://github.com/lupantech/ScienceQA)] [[Data](https://huggingface.co/datasets/derek-thomas/ScienceQA)] <br>
University of California, Los Angeles, Arizona State University, Allen Institute for AI

* **GQA** [CVPR 2019] [[Paper](https://arxiv.org/pdf/1902.09506)] [[Code](https://github.com/stanfordnlp/GQA)] [[Data](https://cs.stanford.edu/people/dorarad/gqa/about.html)] <br>
Stanford University

* **MMMU: A Massive Multi-discipline Multimodal Understanding and Reasoning Benchmark for Expert AGI** [CVPR 2024] [[Paper](https://arxiv.org/pdf/2311.16502)] [[Code](https://github.com/MMMU-Benchmark/MMMU)] [[Data](https://huggingface.co/datasets/MMMU/MMMU)] <br>
IN.AI Research, University of Waterloo, The Ohio State University, Carnegie Mellon University, University of Victoria, Princeton University

* **MathVista: Evaluating Mathematical Reasoning of Foundation Models in Visual Contexts** [ICLR 2024] [[Paper](https://arxiv.org/pdf/2310.02255)] [[Code](https://github.com/lupantech/MathVista)] [[Data](https://huggingface.co/datasets/AI4Math/MathVista)] <br>
UCLA, University of Washington, Microsoft Research, Redmond

* **PuzzleBench: A Fully Dynamic Evaluation Framework for Large Multimodal Models on Puzzle Solving** [arXiv 2025] [[Paper](https://arxiv.org/abs/2504.10885)] <br>
Shanghai Jiao Tong University

* **MME-CoT: Benchmarking Chain-of-Thought in Large Multimodal Models for Reasoning Quality, Robustness, and Efficiency** [arXiv 2025] [[Paper](https://arxiv.org/abs/2502.09621)] [[Code](https://github.com/MME-Benchmarks/MME-CoT)] [[Data](https://huggingface.co/datasets/CaraJ/MME-CoT)] [[Homepage](https://mmecot.github.io/)] <br>
The Chinese University of Hong Kong, ByteDance, Northeastern University

* **MME-Reasoning: A Comprehensive Benchmark for Logical Reasoning in MLLMs** [arXiv 2025] [[Paper](https://arxiv.org/abs/2505.21327)] [[Code](https://github.com/InternScience/MME-Reasoning)] [[Data](https://huggingface.co/datasets/InternScience/MME-Reasoning)] [[Homepage](https://alpha-innovator.github.io/mmereasoning.github.io/)] <br>
Fudan University, The Chinese University of Hong Kong, Shanghai AI Laboratory

* **A Diagram Is Worth A Dozen Images** [ECCV 2016] [[Paper](https://arxiv.org/pdf/1603.07396)] [[Code](https://github.com/allenai/ai2d)] [[Data](https://prior.allenai.org/projects/diagram-understanding)] <br>
Allen Institute for Artificial Intelligence, University of Washington

**Others:** CLEVR, OlympiadBench, MathVision, MMMU-Pro, PuzzleVQA, GPQA

### Domain Adaptation Benchmarks

* **DocVQA: A Dataset for VQA on Document Images** [WACV 2021] [[Paper](https://arxiv.org/pdf/2007.00398)] [[Code](https://github.com/answer-extraction/DocVQA)] [[Data](https://rrc.cvc.uab.es/?ch=17)] <br>
CVIT, IIIT Hyderabad, India, Computer Vision Center, UAB, Spain

* **ChartX & ChartVLM: A Versatile Benchmark and Foundation Model for Complicated Chart Reasoning** [TIP 2025] [[Paper](https://arxiv.org/abs/2402.12185)] [[Code](https://github.com/InternScience/ChartVLM)] [[Data](https://huggingface.co/datasets/SharkAI/ChartX)] <br>
Shanghai AI Laboratory, Shanghai Jiao Tong University

* **OCRBench: On the Hidden Mystery of OCR in Large Multimodal Models** [Science China Information Sciences 2024] [[Paper](https://arxiv.org/abs/2305.07895)] [[Code](https://github.com/Yuliang-Liu/MultimodalOCR)] [[Data](https://huggingface.co/datasets/echo840/OCRBench)] <br>
Shanghai AI Laboratory

* **SeeClick: Harnessing GUI Grounding for Advanced Visual GUI Agents** [ACL 2024] [[Paper](https://arxiv.org/abs/2401.10935)] [[Code](https://github.com/njucckevin/SeeClick)] [[Data](https://huggingface.co/datasets/rootsautomation/ScreenSpot)] <br>
The Chinese University of Hong Kong, Shanghai AI Laboratory

* **Mind2Web: Towards a Generalist Agent for the Web** [NeurIPS 2023] [[Paper](https://arxiv.org/pdf/2306.06070)] [[Code](https://github.com/OSU-NLP-Group/Mind2Web)] [[Data](https://huggingface.co/datasets/osunlp/Mind2Web)] <br>
The Ohio State University

* **A Dataset of Clinically Generated Visual Questions and Answers about Radiology Images** [Scientific Data 2018] [[Paper](https://www.nature.com/articles/sdata2018251)] [[Code](https://github.com/Awenbocc/VQA-Med)] [[Data](https://osf.io/89kps/)] <br>
National Library of Medicine, National Institutes of Health

* **PathVQA: 30000+ Questions for Medical Visual Question Answering** [arXiv 2020] [[Paper](https://arxiv.org/abs/2003.10286)] [[Code](https://github.com/UCSD-AI4H/PathVQA)] [[Data](https://github.com/UCSD-AI4H/PathVQA)] <br>
University of California San Diego, Carnegie Mellon University

**Others:** AndroidControl-Low, AndroidControl-High, GUI-Odyssey, ScreenSpot-Pro, GUI-Act-Web, OmniAct-Web, ChartQA, InfoVQA, TextVQA, ST-VQA

---

## &#128204; Citation

If this repository or the associated survey is useful for your research, please consider citing the original survey paper and acknowledging this curated paper list.

```bibtex
@article{zhang2026survey,
  title={A Survey on Post-Training of Multimodal Large Language Models},
  author={Haonan Zhang and Pengpeng Zeng and Libin Cao and Wenrui Lai and
          Jinlong Li and Duo Peng and Yi Bin and Xuanhan Wang and Ji Zhang and
          Jingkuan Song and Nicu Sebe and Yuchuan Wu and Yongbin Li and
          Heng Tao Shen and Jieping Ye},
  year={2026}
}
```
