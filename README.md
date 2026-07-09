# Awesome Post-Training for Multimodal Large Language Models

> 多模态大模型后训练研究论文综述合集，系统整理 **Multimodal Instruction Tuning**、**Multimodal Alignment Learning**、**Multimodal Reasoning Enhancement** 等方向的代表性工作。

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![Topic](https://img.shields.io/badge/Topic-Multimodal%20LLMs-0f766e)
![Survey](https://img.shields.io/badge/Survey-Post--training-b31b1b)
![Format](https://img.shields.io/badge/Format-Markdown-1f6feb)

本项目围绕论文 **A Survey on Post-training of Multimodal Large Language Models** 展开，旨在为多模态大模型后训练研究提供一份结构化、可持续维护的开源论文索引。综述将 MLLMs post-training 视为面向行为塑造的关键阶段：在预训练获得基础跨模态表征之后，通过指令数据、偏好反馈、奖励信号、推理轨迹、领域数据与可扩展训练机制，使模型进一步具备更可靠的指令遵循、偏好对齐、复杂推理、场景适配与规模化学习能力。

当前版本重点整理 `论文合集.xlsx` 中已经统计完成的 **Table 1-3**：多模态指令微调、多模态对齐学习和多模态推理增强。后续将继续补充 Table 4-9 对应的领域适配、可扩展训练与基准评测内容。欢迎 Star、Fork 与 Pull Request，共同维护这一方向的最新进展。

<p align="center">
  <img src="framework.png" width="92%" alt="Post-training framework for multimodal large language models">
</p>

<p align="center"><em>Framework overview of multimodal behavior-shaping post-training.</em></p>

---

## Contents

| Section | Subsection |
| --- | --- |
| [Multimodal Instruction Tuning](#multimodal-instruction-tuning) | [Representative Papers](#multimodal-instruction-tuning-papers) |
| [Multimodal Alignment Learning](#multimodal-alignment-learning) | [Multimodal RLHF](#multimodal-rlhf), [Multimodal RLAIF](#multimodal-rlaif), [Multimodal Direct Preference Optimization](#multimodal-direct-preference-optimization) |
| [Multimodal Reasoning Enhancement](#multimodal-reasoning-enhancement) | [R1-based Multimodal Reasoning](#r1-based-multimodal-reasoning), [Thinking with Images](#thinking-with-images), [Multimodal Self-Evolving](#multimodal-self-evolving), [Multimodal Distillation](#multimodal-distillation) |
| [Multimodal Domain Adaptation](#multimodal-domain-adaptation) | Table 4, to be updated |
| [Multimodal scalable training](#multimodal-scalable-training) | [LoRA-based methods](#lora-based-methods), [MoE-based methods](#moe-based-methods), [compute-efficient methods](#compute-efficient-methods) |
| [Multimodal Benchmarks](#multimodal-benchmarks) | Table 8-9, to be updated |

---

# Papers

## Multimodal Instruction Tuning

多模态指令微调是 MLLM 后训练中最基础且最早形成体系的方向。其核心目标是利用图文、视频文本、音频文本或更复杂的多模态指令-回答数据，将预训练阶段获得的跨模态表征转化为面向任务与用户意图的指令遵循能力。早期代表工作如 LLaVA、MiniGPT-4 与 InstructBLIP 证明了“视觉编码器 + 大语言模型 + 指令数据”的有效范式；后续研究进一步扩展到高分辨率感知、多图与视频理解、移动端轻量部署、通用视觉任务迁移、视觉提示理解、数据选择和混合专家式微调等问题。

从 Table 1 的发展脉络看，该方向的研究重点逐渐从“能否让 LLM 看懂图像并回答问题”，演进为“如何构建更高质量、更细粒度、更具泛化性的多模态交互接口”。模型规模、视觉编码器、训练数据规模、模态覆盖范围和指令数据组织方式共同决定了最终的多模态指令遵循能力。

### Multimodal Instruction Tuning Papers

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Visual Instruction Tuning](https://arxiv.org/pdf/2304.08485) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2304.08485) / [Code](https://github.com/haotian-liu/LLaVA) / [Project](https://llava-vl.github.io/) |
| 2 | [MiniGPT-4: Enhancing Vision-Language Understanding with Advanced Large Language Models](https://arxiv.org/pdf/2304.10592) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2304.10592) / [Code](https://github.com/Vision-CAIR/MiniGPT-4) / [Project](https://minigpt-4.github.io/) |
| 3 | [InstructBLIP: Towards General-purpose Vision-Language Models with Instruction Tuning](https://arxiv.org/pdf/2305.06500) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2305.06500) / [Code](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip) |
| 4 | [mPLUG-Owl: Modularization Empowers Large Language Models with Multimodality](https://arxiv.org/pdf/2304.14178) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2304.14178) / [Code](https://github.com/X-PLUG/mPLUG-Owl) |
| 5 | [LLaMA-Adapter V2: Parameter-Efficient Visual Instruction Model](https://arxiv.org/pdf/2304.15010) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2304.15010) / [Code](https://github.com/OpenGVLab/LLaMA-Adapter) |
| 6 | [Improved Baselines with Visual Instruction Tuning](https://arxiv.org/pdf/2310.03744) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2310.03744) / [Code](https://github.com/haotian-liu/LLaVA) / [Project](https://llava-vl.github.io/) |
| 7 | [Qwen-VL: A Versatile Vision-Language Model for Understanding, Localization, Text Reading, and Beyond](https://arxiv.org/pdf/2308.12966) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2308.12966) / [Code](https://github.com/QwenLM/Qwen-VL) |
| 8 | [CogVLM: Visual Expert for Pretrained Language Models](https://arxiv.org/pdf/2311.03079) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2311.03079) / [Code](https://github.com/THUDM/CogVLM) |
| 9 | [How Far Are We to GPT-4V? Closing the Gap to Commercial Multimodal Models with Open-Source Suites](https://arxiv.org/pdf/2404.16821) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2404.16821) / [Code](https://github.com/OpenGVLab/InternVL) |
| 10 | LLaVA-NeXT: Improved reasoning, OCR, and world knowledge | Model | - | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-01-30-llava-next/) |
| 11 | [What matters when building vision-language models?](https://arxiv.org/pdf/2405.02246) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2405.02246) / [HF](https://huggingface.co/blog/idefics2) |
| 12 | [Qwen2-VL: Enhancing Vision-Language Model's Perception of the World at Any Resolution](https://arxiv.org/pdf/2409.12191) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2409.12191) / [Code](https://github.com/QwenLM/Qwen2-VL) |
| 13 | [LLaVA-OneVision: Easy Visual Task Transfer](https://arxiv.org/pdf/2408.03326) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2408.03326) / [Code](https://github.com/LLaVA-VL/LLaVA-NeXT/blob/main/docs/LLaVA_OneVision.md) / [Project](https://llava-vl.github.io/blog/2024-08-05-llava-onevision/) |
| 14 | [Expanding Performance Boundaries of Open-Source Multimodal Models with Model, Data, and Test-Time Scaling](https://arxiv.org/pdf/2412.05271) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2412.05271) / [Code](https://github.com/OpenGVLab/InternVL) / [Project](https://internvl.github.io/blog/2024-12-05-InternVL-2.5/) |
| 15 | [Qwen2.5-VL Technical Report](https://arxiv.org/pdf/2502.13923) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2502.13923) / [Code](https://github.com/QwenLM/Qwen2.5-VL) |
| 16 | [VILA: On Pre-training for Visual Language Models](https://arxiv.org/pdf/2312.07533) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.07533) / [Code](https://github.com/NVlpdf/VILA) |
| 17 | [MobileVLM : A Fast, Strong and Open Vision Language Assistant for Mobile Devices](https://arxiv.org/pdf/2312.16886) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.16886) / [Code](https://github.com/Meituan-AutoML/MobileVLM) |
| 18 | [DeepSeek-VL: Towards Real-World Vision-Language Understanding](https://arxiv.org/pdf/2403.05525) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2403.05525) / [Code](https://github.com/deepseek-ai/DeepSeek-VL) |
| 19 | [Yi: Open Foundation Models by 01.AI](https://arxiv.org/pdf/2403.04652) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2403.04652) / [Code](https://github.com/01-ai/Yi) / [HF](https://huggingface.co/01-ai/Yi-VL-6B) |
| 20 | [Cambrian-1: A Fully Open, Vision-Centric Exploration of Multimodal LLMs](https://arxiv.org/pdf/2406.16860) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2406.16860) / [Code](https://github.com/cambrian-mllm/cambrian) / [Project](https://cambrian-mllm.github.io/) |
| 21 | [MiniCPM-V: A GPT-4V Level MLLM on Your Phone](https://arxiv.org/pdf/2408.01800) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2408.01800) / [Code](https://github.com/OpenBMB/MiniCPM-V) / [Project](https://huggingface.co/openbmb/MiniCPM-V-2_6) |
| 22 | [Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone](https://arxiv.org/pdf/2404.14219) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2404.14219) / [HF](https://huggingface.co/microsoft/Phi-3.5-vision-instruct) |
| 23 | Llama-3.2-Vision-Instruct | Model | - | [HF](https://huggingface.co/meta-llama/Llama-3.2-11B-Vision-Instruct) |
| 24 | [Molmo and PixMo: Open Weights and Open Data for State-of-the-Art Vision-Language Models](https://arxiv.org/pdf/2409.17146) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2409.17146) / [Code](https://github.com/allenai/molmo) / [Project](https://molmo.allenai.org/) |
| 25 | [Pixtral-12B](https://arxiv.org/pdf/2410.07073) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2410.07073) / [Project](https://mistral.ai/news/pixtral-12b) |
| 26 | [Aria: An Open Multimodal Native Mixture-of-Experts Model](https://arxiv.org/pdf/2410.05993) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2410.05993) / [Code](https://github.com/rhymes-ai/Aria) |
| 27 | [PaliGemma: A versatile 3B VLM for transfer](https://arxiv.org/pdf/2407.07726) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2407.07726) / [HF](https://huggingface.co/google/paligemma-3b-mix-224) |
| 28 | [Otter: A Multi-Modal Model with In-Context Instruction Tuning](https://arxiv.org/pdf/2305.03726) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2305.03726) / [Code](https://github.com/Luodian/Otter) |
| 29 | [LLaMA-Adapter: Efficient Fine-tuning of Language Models with Zero-init Attention](https://arxiv.org/pdf/2303.16199) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2303.16199) / [Code](https://github.com/OpenGVLab/LLaMA-Adapter) |
| 30 | [Cheap and Quick: Efficient Vision-Language Instruction Tuning for Large Language Models](https://arxiv.org/pdf/2305.15023) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2305.15023) / [Code](https://github.com/luogen1996/LaVIN) |
| 31 | [Valley: Video Assistant with Large Language model Enhanced abilitY](https://arxiv.org/pdf/2306.07207) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2306.07207) / [Code](https://github.com/RupertLuo/Valley) |
| 32 | [NExT-GPT: Any-to-Any Multimodal LLM](https://arxiv.org/pdf/2309.05519) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2309.05519) / [Code](https://github.com/NExT-GPT/NExT-GPT) / [Project](https://next-gpt.github.io/) |
| 33 | [InternVL: Scaling up Vision Foundation Models and Aligning for Generic Visual-Linguistic Tasks](https://arxiv.org/pdf/2312.14238) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.14238) / [Code](https://github.com/OpenGVLab/InternVL) |
| 34 | [Parrot: Multilingual Visual Instruction Tuning](https://arxiv.org/pdf/2406.02539) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2406.02539) / [Code](https://github.com/AIDC-AI/Parrot) |
| 35 | [Generative Visual Instruction Tuning](https://arxiv.org/pdf/2406.11262) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2406.11262) / [Code](https://github.com/jeffhernandez1995/GenLlaVA) |
| 36 | [PPLLaVA: Varied Video Sequence Understanding With Prompt Guidance](https://arxiv.org/pdf/2411.02327) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2411.02327) |
| 37 | [MLAN: Language-Based Instruction Tuning Preserves and Transfers Knowledge in Multimodal Language Models](https://arxiv.org/pdf/2411.10557) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2411.10557) |
| 38 | [INST-IT: Boosting Instance Understanding via Explicit Visual Prompt Instruction Tuning](https://arxiv.org/pdf/2412.03565) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2412.03565) / [Code](https://github.com/inst-it/inst-it) / [Project](https://inst-it.github.io/) |
| 39 | [Comparison Visual Instruction Tuning](https://arxiv.org/pdf/2406.09240) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2406.09240) / [Code](https://github.com/wlin-at/CaD-VI) / [Project](https://wlin-at.github.io/cad_vi) / [HF](https://huggingface.co/datasets/wlin21at/CaD-Inst) |
| 40 | [Multimodal Instruction Tuning with Conditional Mixture of LoRA](https://arxiv.org/pdf/2402.15896) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2402.15896) / [Code](https://github.com/PLUM-Lab/MixLoRA) |
| 41 | [Do we Really Need Visual Instructions? Towards Visual Instruction-Free Fine-tuning for Large Vision-Language Models](https://arxiv.org/pdf/2502.11427) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2502.11427) |
| 42 | [Re-Imagining Multimodal Instruction Tuning: A Representation View](https://arxiv.org/pdf/2503.00723) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2503.00723) |
| 43 | [Learning to Instruct for Visual Instruction Tuning](https://arxiv.org/pdf/2503.22215) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2503.22215) / [Code](https://github.com/Feng-Hong/L2T) |
| 44 | [Visual Compositional Tuning](https://arxiv.org/pdf/2504.21850) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2504.21850) / [Code](https://github.com/princetonvisualai/compact) / [Project](https://princetonvisualai.github.io/compact/) |
| 45 | [Visual Instruction Bottleneck Tuning](https://arxiv.org/pdf/2505.13946) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2505.13946) / [Code](https://github.com/deeplearning-wisc/vittle) |
| 46 | [LLaDA-V: Large Language Diffusion Models with Visual Instruction Tuning](https://arxiv.org/pdf/2505.16933) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2505.16933) / [Code](https://ml-gsai.github.io/LLaDA-V-demo/) / [Project](https://ml-gsai.github.io/LLaDA-V-demo/) |
| 47 | [MINT: Multimodal Instruction Tuning with Multimodal Interaction Grouping](https://arxiv.org/pdf/2506.02308) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2506.02308) / [Code](https://github.com/sxj1215/MINT) |
| 48 | [CoIDO: Efficient Data Selection for Visual Instruction Tuning via Coupled Importance-Diversity Optimization](https://arxiv.org/pdf/2510.17847) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2510.17847) / [Code](https://github.com/SuDIS-ZJU/CoIDO) |
| 49 | Data Selection Matters: Towards Robust Instruction Tuning of Large Multimodal Models | Model | - | [Code](https://github.com/xyang583/ARDS) / [Project](https://papers.neurips.cc/paper_files/paper/2025/hash/0d77ccb50a558035f19089096f933e8e-Abstract-Conference.html) |
| 50 | [SAME: Stabilized Mixture-of-Experts for Multimodal Continual Instruction Tuning](https://arxiv.org/pdf/2602.01990) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2602.01990) / [Code](https://github.com/LAMDA-CL/Prism) |
| 51 | [Less Data, Faster Convergence: Goal-Driven Data Optimization for Multimodal Instruction Tuning](https://arxiv.org/pdf/2603.12478) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2603.12478) / [Code](https://github.com/rujiewu/GDO) |
| 52 | [LLaVA-NeXT-Interleave: Tackling Multi-image, Video, and 3D in Large Multimodal Models](https://arxiv.org/pdf/2407.07895) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2407.07895) / [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-06-16-llava-next-interleave/) |
| 53 | [MAVIS: Mathematical Visual Instruction Tuning with an Automatic Data Engine](https://arxiv.org/pdf/2407.08739) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2407.08739) / [Code](https://github.com/ZrrSkywalker/MAVIS) |
| 54 | [MANTIS: Interleaved Multi-Image Instruction Tuning](https://arxiv.org/pdf/2405.01483) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2405.01483) / [Code](https://github.com/OpenGVLab/LLaMA-Adapter/tree/main/imagebind_LLM) / [Project](https://tiger-ai-lab.github.io/Mantis/) |
| 55 | [ImageBind-LLM: Multi-modality Instruction Tuning](https://arxiv.org/pdf/2309.03905) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2309.03905) / [Code](https://github.com/OpenGVLab/LLaMA-Adapter/tree/main/imagebind_LLM) |
| 56 | [ShareGPT4V: Improving Large Multi-Modal Models with Better Captions](https://arxiv.org/pdf/2311.12793) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2311.12793) / [Code](https://github.com/ShareGPT4Omni/ShareGPT4V) / [Project](https://sharegpt4v.github.io/) |
| 57 | [MiniGPT-v2: large language model as a unified interface for vision-language multi-task learning](https://arxiv.org/pdf/2310.09478) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2310.09478) / [Code](https://github.com/Vision-CAIR/MiniGPT-4) / [Project](https://minigpt-v2.github.io/) |
| 58 | [ViP-LLaVA: Making Large Multimodal Models Understand Arbitrary Visual Prompts](https://arxiv.org/pdf/2312.00784) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.00784) / [Code](https://github.com/WisconsinAIVision/ViP-LLaVA) / [Project](https://vip-llava.github.io/) |
| 59 | [LLaVA-UHD: an LMMPerceiving Any Aspect Ratio and High-Resolution Images](https://arxiv.org/pdf/2403.11703) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2403.11703) / [Code](https://github.com/thunlp/LLaVA-UHD) |
| 60 | [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/pdf/2312.08914) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.08914) / [Code](https://github.com/zai-org/CogAgent) |
| 61 | [Monkey :ImageResolutionandText Label Are Important Things for Large Multi-modal Models](https://arxiv.org/pdf/2311.06607) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2311.06607) / [Code](https://github.com/Yuliang-Liu/Monkey) |
| 62 | [Mini-Gemini: Mining the Potential of Multi-modality Vision Language Models](https://arxiv.org/pdf/2403.18814v1) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2403.18814v1) / [Code](https://github.com/JIA-Lab-research/MGM) |
| 63 | [Feast Your Eyes: Mixture-of-Resolution Adaptation for Multimodal Large Language Models](https://arxiv.org/pdf/2403.03003) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2403.03003) / [Code](https://github.com/luogen1996/LLaVA-HR) |
| 64 | [SPHINX: The Joint Mixing of Weights, Tasks, and Visual Embeddings for Multi-modal Large Language Models](https://arxiv.org/pdf/2311.07575) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2311.07575) / [Code](https://github.com/Alpha-VLLM/LLaMA2-Accessory) |
| 65 | [MoAI: Mixture of All Intelligence for Large Language and Vision Models](https://arxiv.org/pdf/2403.07508) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2403.07508) / [Code](https://github.com/ByungKwanLee/MoAI) |

---

## Multimodal Alignment Learning

多模态对齐学习关注模型输出是否符合人类偏好、事实一致性、安全性与跨模态语义约束。与纯文本 LLM 对齐相比，MLLM 对齐还需要处理视觉幻觉、区域级错误、视频时序理解偏差、模态不一致和复杂反馈粒度等问题。因此，Table 2 将相关工作组织为三类：基于人工反馈的 RLHF、基于 AI 反馈的 RLAIF，以及直接从偏好数据中优化策略的 DPO 系列方法。

### Multimodal RLHF

Multimodal RLHF 通过人工反馈或人工构造的奖励信号，将模型行为从普通指令遵循进一步推向事实可靠、细粒度可纠错和偏好一致。该类方法通常围绕 pair-level、span-level、step-level 或 mixed-level 反馈构建奖励模型，并结合 PPO、DDPO、PRM、Best-of-N、reject sampling 或多目标强化学习等机制优化 MLLM。代表性工作从 LLaVA-RLHF、RLHF-V 到 VisualPRM、Seed1.5-VL 和 MiMo-VL，体现了反馈粒度从回答级扩展到过程级、从图像问答扩展到图像/视频综合场景的趋势。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF](https://arxiv.org/pdf/2309.14525) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2309.14525) / [Code](https://github.com/llava-rlhf/LLaVA-RLHF) / [Project](https://llava-rlhf.github.io/) |
| 2 | [RLHF-V: Towards Trustworthy MLLMs via Behavior Alignment from Fine-grained Correctional Human Feedback](https://arxiv.org/pdf/2312.00849) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.00849) / [Code](https://github.com/RLHF-V/RLHF-V) / [Project](https://rlhf-v.github.io/) |
| 3 | [VisualPRM: An Effective Process Reward Model for Multimodal Reasoning](https://arxiv.org/pdf/2503.10291) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2503.10291) / [Project](https://internvl.github.io/blog/2025-03-13-VisualPRM/) |
| 4 | [Gemini: A Family of Highly Capable Multimodal Models](https://arxiv.org/pdf/2312.11805) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.11805) / [Project](https://deepmind.google/technologies/gemini/) |
| 5 | [MM-RLHF: The Next Step Forward in Multimodal LLM Alignment](https://arxiv.org/pdf/2502.10391) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2502.10391) / [Code](https://github.com/Kwai-YuanQi/MM-RLHF) / [Project](https://mm-rlhf.github.io/) |
| 6 | [Seed1.5-VL Technical Report](https://arxiv.org/pdf/2505.07062) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2505.07062) / [Code](https://github.com/ByteDance-Seed/Seed1.5-VL) / [Project](https://seed.bytedance.com/en/tech/seed1_5_vl) |
| 7 | [MiMo-VL Technical Report](https://arxiv.org/pdf/2506.03569) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2506.03569) / [Code](https://github.com/XiaomiMiMo/MiMo-VL) |

### Multimodal RLAIF

Multimodal RLAIF 旨在降低人工反馈成本，利用更强的模型、规则化评审器或开放式 AI feedback 生成偏好信号。该方向尤其适合视频、多轮交互和大规模偏好数据构造场景，能够在可扩展性与反馈质量之间取得更好的折中。VLM-RLAIF、RLAIF-V 与 Silkie 等工作展示了 AI 反馈在上下文感知奖励建模、迭代偏好优化和偏好蒸馏中的价值。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Tuning Large Multimodal Models for Videos using Reinforcement Learning from AI Feedback](https://arxiv.org/pdf/2402.03746) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2402.03746) / [Code](https://github.com/yonseivnl/vlm-rlaif) / [Project](https://dcahn12.github.io/projects/vlm-rlaif/) |
| 2 | [RLAIF-V: Open-Source AI Feedback Leads to Super GPT-4V Trustworthiness](https://arxiv.org/pdf/2405.17220) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2405.17220) / [Code](https://github.com/RLHF-V/RLAIF-V) |
| 3 | [SILKIE: Preference Distillation for Large Visual Language Models](https://arxiv.org/pdf/2312.10665) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.10665) / [Code](https://github.com/vlf-silkie/VLFeedback) / [Project](https://vlf-silkie.github.io/) |

### Multimodal Direct Preference Optimization

Multimodal Direct Preference Optimization 避免显式训练复杂奖励模型，直接基于偏好对或更细粒度的偏好信号更新策略。该方向在降低训练复杂度的同时，特别适合处理多模态幻觉、对象级错误、视频回答偏差和模态间不一致等问题。Table 2 中的相关方法覆盖 response-level、object-level、modality-level、pair-level 与 token-level 偏好建模，并逐渐从离线偏好优化走向 on-policy 数据构造、难度感知采样与不确定性感知探索。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Direct Preference Optimization of Video Large Multimodal Models from Language Model Reward](https://arxiv.org/pdf/2404.01258) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2404.01258) / [Code](https://github.com/RifleZhang/LLaVA-Hound-DPO) |
| 2 | [ISR-DPO: Aligning Large Multimodal Models for Videos by Iterative Self-Retrospective DPO](https://arxiv.org/pdf/2406.11280) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2406.11280) / [Code](https://github.com/snumprlab/isr-dpo) / [Project](https://dcahn12.github.io/projects/isr-dpo/) |
| 3 | [Beyond Hallucinations: Enhancing LVLMs through Hallucination-Aware Direct Preference Optimization](https://arxiv.org/pdf/2311.16839) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2311.16839) / [Code](https://github.com/opendatalab/HA-DPO) / [Project](https://opendatalab.github.io/HA-DPO/) |
| 4 | [Mitigating Hallucination in Multimodal Large Language Model via Hallucination-targeted Direct Preference Optimization](https://arxiv.org/pdf/2411.10436) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2411.10436) |
| 5 | [V-DPO: Mitigating Hallucination in Large Vision Language Models via Vision-Guided Direct Preference Optimization](https://arxiv.org/pdf/2411.02712) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2411.02712) / [Code](https://github.com/YuxiXie/V-DPO) |
| 6 | [CLIP-DPO: Vision-Language Models as a Source of Preference for Fixing Hallucinations in LVLMs](https://arxiv.org/pdf/2408.10433) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2408.10433) |
| 7 | [Mitigating Hallucinations in Multimodal LLMs via Object-aware Preference Optimization](https://arxiv.org/pdf/2508.20181) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2508.20181) / [Code](https://github.com/aimagelab/CHAIR-DPO) |
| 8 | [MDPO: Conditional Preference Optimization for Multimodal Large Language Models](https://arxiv.org/pdf/2406.11839) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2406.11839) / [Code](https://github.com/luka-group/mDPO) / [Project](https://feiwang96.github.io/mDPO/) |
| 9 | PEA-DPO: Perception-Enhanced Alignment Direct Preference Optimization for MLLMs Alignment | Model | - | [Project](https://openreview.net/forum?id=uZ5AmOJKqV) |
| 10 | [MoD-DPO: Towards Mitigating Cross-modal Hallucinations in Omni LLMs using Modality Decoupled Preference Optimization](https://arxiv.org/pdf/2603.03192) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2603.03192) / [Project](https://mod-dpo.github.io/) |
| 11 | [OMNI DPO: A Preference Optimization Framework to Address Omni-Modal Hallucination](https://arxiv.org/pdf/2509.00723) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2509.00723) |
| 12 | [DA-DPO: Cost-efficient Difficulty-aware Preference Optimization for Reducing MLLM Hallucinations](https://arxiv.org/pdf/2601.00623) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2601.00623) / [Code](https://github.com/Artanic30/DA-DPO) / [Project](https://artanic30.github.io/project_pages/DA-DPO/) |
| 13 | [Uncertainty-Aware Exploratory Direct Preference Optimization for Multimodal Large Language Models](https://arxiv.org/pdf/2605.04874) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2605.04874) |
| 14 | [Mitigating Hallucinations in Large Vision-Language Models via DPO: On-Policy Data Hold the Key](https://arxiv.org/pdf/2501.09695) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2501.09695) / [Code](https://github.com/zhyang2226/OPA-DPO) / [Project](https://opa-dpo.github.io/) |
| 15 | [LPOI: Listwise Preference Optimization for Vision Language Models](https://arxiv.org/pdf/2505.21061) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2505.21061) / [Code](https://github.com/fatemehpesaran310/lpoi) |

---

## Multimodal Reasoning Enhancement

多模态推理增强聚焦 MLLM 在复杂视觉问答、数学图形推理、视频时空理解、工具使用、视觉定位与跨模态检索等任务上的深层推理能力。Table 3 显示，该方向在 2025 年后快速发展：一方面，DeepSeek-R1 式强化学习范式推动了基于规则奖励和 GRPO/PPO 的多模态推理训练；另一方面，“Thinking with Images”、自进化和蒸馏方法则试图让模型不仅输出答案，还能形成可验证、可迭代、可迁移的视觉推理过程。

### R1-based Multimodal Reasoning

R1-based Multimodal Reasoning 将 R1-style 的强化学习思想引入视觉语言模型，通常利用结果正确性、格式约束、过程奖励或组相对策略优化来激励长链路推理。该类方法的重要特点是减少对人工标注推理轨迹的依赖，通过可验证答案、规则奖励或视觉过程奖励来提升模型在数学、图表、视频和检索等场景中的推理表现。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [VLM-R1: A Stable and Generalizable R1-style Large Vision-Language Model](https://arxiv.org/abs/2504.07615) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2504.07615) / [Code](https://github.com/om-ai-lab/VLM-R1) |
| 2 | [Visual-RFT: Visual Reinforcement Fine-Tuning](https://arxiv.org/abs/2503.01785) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.01785) / [Code](https://github.com/Liuziyu77/Visual-RFT) |
| 3 | [Vision-R1: Incentivizing Reasoning Capability in Multimodal Large Language Models](https://arxiv.org/abs/2503.06749) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.06749) / [Code](https://github.com/Osilly/Vision-R1) |
| 4 | [VideoChat-R1: Enhancing Spatio-Temporal Perception via Reinforcement Fine-Tuning](https://arxiv.org/abs/2504.06958) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2504.06958) / [Code](https://github.com/OpenGVLab/VideoChat-R1) |
| 5 | [Video-R1: Reinforcing Video Reasoning in MLLMs](https://arxiv.org/abs/2503.21776) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.21776) / [Code](https://github.com/tulerfeng/Video-R1) |
| 6 | [VisualPRM: An Effective Process Reward Model for Multimodal Reasoning](https://arxiv.org/abs/2503.10291) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.10291) / [Code](https://github.com/OpenGVLab/InternVL) / [Project](https://internvl.github.io/blog/2025-03-13-VisualPRM/) / [HF](https://huggingface.co/OpenGVLab/VisualPRM-8B) |
| 7 | [R1-VL: Learning to Reason with Multimodal Large Language Models via Step-wise Group Relative Policy Optimization](https://arxiv.org/abs/2503.12937) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.12937) |
| 8 | [R1-Zero's "Aha Moment" in Visual Reasoning on a 2B Non-SFT Model](https://arxiv.org/abs/2503.05132) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.05132) / [Code](https://github.com/turningpoint-ai/VisualThinker-R1-Zero) |
| 9 | [MM-Eureka: Exploring the Frontiers of Multimodal Reasoning with Rule-based Reinforcement Learning](https://arxiv.org/abs/2503.07365) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.07365) / [Code](https://github.com/ModalMinds/MM-EUREKA) / [HF](https://huggingface.co/FanqingM/MM-Eureka-8B) |
| 10 | [R1-Onevision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization](https://arxiv.org/abs/2503.10615) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.10615) / [Code](https://github.com/Fancy-MLLM/R1-onevision) |
| 11 | [R1-Omni: Explainable Omni-Multimodal Emotion Recognition with Reinforcement Learning](https://arxiv.org/abs/2503.05379) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.05379) / [Code](https://github.com/HumanMLLM/R1-Omni) |
| 12 | [Retrv-R1: A Reasoning-Driven MLLM Framework for Universal and Efficient Multimodal Retrieval](https://arxiv.org/abs/2510.02745) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2510.02745) / [Code](https://lanyunzhu.site/RetrvR1/) / [Project](https://lanyunzhu.site/RetrvR1/) |

### Thinking with Images

Thinking with Images 强调模型在推理过程中显式使用图像、视觉区域、视觉工具或中间视觉结构，而不是仅将图像压缩为隐式上下文后直接生成文本答案。该方向使推理过程更贴近视觉证据链，适用于需要定位、裁剪、点选、视觉规划和工具调用的任务。相关工作探索了 grounded reasoning、视觉工具强化学习、统一感知推理以及潜在视觉结构推理等路线。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [GRIT: Teaching MLLMs to Think with Images](https://arxiv.org/abs/2505.15879) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.15879) / [Code](https://github.com/eric-ai-lab/GRIT) / [Project](https://grounded-reasoning.github.io/) |
| 2 | [Point-RFT: Improving Multimodal Reasoning with Visually Grounded Reinforcement Finetuning](https://arxiv.org/abs/2505.19702) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.19702) |
| 3 | [OpenThinkIMG: Learning to Think with Images via Visual Tool Reinforcement Learning](https://arxiv.org/abs/2505.08617) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.08617) / [Code](https://github.com/OpenThinkIMG/OpenThinkIMG) / [HF](https://huggingface.co/collections/Warrieryes/openthinkimg) |
| 4 | [VisionReasoner: Unified Reasoning-Integrated Visual Perception via Reinforcement Learning](https://arxiv.org/abs/2505.12081) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.12081) / [Code](https://github.com/dvlab-research/VisionReasoner) |
| 5 | [DeepEyes: Incentivizing "Thinking with Images" via Reinforcement Learning](https://arxiv.org/abs/2505.14362) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.14362) / [Code](https://github.com/Visual-Agent/DeepEyes) / [HF](https://huggingface.co/ChenShawn/DeepEyes-7B) |
| 6 | [VTool-R1: VLMs Learn to Think with Images via Reinforcement Learning on Multimodal Tool Use](https://arxiv.org/abs/2505.19255) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.19255) / [Code](https://github.com/VTOOL-R1/vtool-r1) / [Project](https://vtool-r1.github.io/) |
| 7 | [Visual Planning: Let's Think Only with Images](https://arxiv.org/abs/2505.11409) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.11409) / [Code](https://github.com/yix8/VisualPlanning) |
| 8 | [LanteRn: Latent Visual Structured Reasoning](https://arxiv.org/abs/2603.25629) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2603.25629) / [Code](https://github.com/GuilhermeViveiros/LantErn) / [HF](https://huggingface.co/AGViveiros/LanteRn-3B-RL) |

### Multimodal Self-Evolving

Multimodal Self-Evolving 关注模型如何通过自生成问题、自我纠错、批判模型、无监督后训练或反思式强化学习持续提升自身能力。相比一次性监督微调，该类方法更强调闭环迭代：模型既可以生成新的多模态训练样本，也可以评估和修正自身输出，从而在数据稀缺或任务持续变化的情况下获得更强的适应性。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [VIGC: Visual Instruction Generation and Correction](https://arxiv.org/abs/2308.12714) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2308.12714) / [Code](https://github.com/opendatalab/VIGC) / [Project](https://opendatalab.github.io/VIGC) |
| 2 | [MindGYM: Enhancing Vision-Language Models via Synthetic Self-Challenging Questions](https://arxiv.org/abs/2503.09499) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.09499) / [Code](https://github.com/modelscope/data-juicer/tree/MindGYM) |
| 3 | [SRPO: Enhancing Multimodal LLM Reasoning via Reflection-Aware Reinforcement Learning](https://arxiv.org/abs/2506.01713) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2506.01713) / [Code](https://github.com/SUSTechBruce/SRPO_MLLMs) / [Project](https://srpo.pages.dev/) |
| 4 | [LLaVA-Critic: Learning to Evaluate Multimodal Models](https://arxiv.org/pdf/2410.02712) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2410.02712) / [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-10-03-llava-critic/) |
| 5 | [MM-UPT: Unsupervised Post-Training for Multi-Modal LLM Reasoning via GRPO](https://arxiv.org/abs/2505.22453) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.22453) / [Code](https://github.com/waltonfuture/MM-UPT) / [HF](https://huggingface.co/WaltonFuture/Qwen2.5-VL-7B-MM-UPT-MMR1) |
| 6 | [LLaVA-Critic-R1: Your Critic Model is Secretly a Strong Policy Model](https://arxiv.org/abs/2509.00676) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2509.00676) / [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) |

### Multimodal Distillation

Multimodal Distillation 通过教师模型、偏好数据、MoE 路由或 on-policy 轨迹，将强模型的视觉语言能力迁移到更小、更高效或更专门化的学生模型中。该方向不仅服务于模型压缩，也服务于能力对齐：学生模型需要继承教师在细粒度视觉感知、时序视频定位、跨模态语音理解和推理过程选择中的关键能力。Table 3 中的工作显示，on-policy distillation 正在成为多模态后训练中兼顾效率与性能的重要范式。

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [LLaVA-KD: A Framework of Distilling Multimodal Large Language Models](https://arxiv.org/abs/2410.16236) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2410.16236) / [Code](https://github.com/Fantasyele/LLaVA-KD) |
| 2 | [LLAVADI: What Matters For Multimodal Large Language Models Distillation](https://arxiv.org/abs/2407.19409) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2407.19409) |
| 3 | [Silkie: Preference Distillation for Large Visual Language Models](https://arxiv.org/abs/2312.10665) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2312.10665) / [Code](https://github.com/vlf-silkie/VLFeedback) / [Project](https://vlf-silkie.github.io/) / [HF](https://huggingface.co/MMInstruction/Silkie) |
| 4 | [LLaVA-MoD: Making LLaVA Tiny via MoE Knowledge Distillation](https://arxiv.org/abs/2408.15881) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2408.15881) / [Code](https://github.com/shufangxun/LLaVA-MoD) |
| 5 | [Video-OPD: Efficient Post-Training of Multimodal Large Language Models for Temporal Video Grounding via On-Policy Distillation](https://arxiv.org/abs/2602.02994) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2602.02994) |
| 6 | [X-OPD: Cross-Modal On-Policy Distillation for Capability Alignment in Speech LLMs](https://arxiv.org/abs/2603.24596) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2603.24596) |
| 7 | [Uni-OPD: Unifying On-Policy Distillation with a Dual-Perspective Recipe](https://arxiv.org/abs/2605.03677) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2605.03677) / [Code](https://github.com/WenjinHou/Uni-OPD) |
| 8 | [Vision-OPD: Learning to See Fine Details for Multimodal LLMs via On-Policy Self-Distillation](https://arxiv.org/abs/2605.18740) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2605.18740) / [Code](https://github.com/VisionOPD/Vision-OPD) |
| 9 | [VA-OPD: Visual-Advantage On-Policy Distillation for Vision-Language Models](https://arxiv.org/abs/2605.21924) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2605.21924) |

---

## Multimodal Domain Adaptation

> 对应综述论文 Table 4。本模块预留用于后续整理面向医疗、法律、金融、教育、GUI、具身智能、自动驾驶等专业场景的多模态领域适配方法。

---

## Multimodal scalable training

> 对应综述论文 Table 5、Table 6、Table 7。本模块预留用于后续整理面向可扩展后训练的参数高效、结构高效与计算高效方法。

### LoRA-based methods

> To be updated.

### MoE-based methods

> To be updated.

### compute-efficient methods

> To be updated.

---

## Multimodal Benchmarks

> 对应综述论文 Table 8、Table 9。本模块预留用于后续整理 MLLM 后训练相关基准、能力维度、评测协议与数据集资源。

---

## Contributing

欢迎补充新的论文、代码、项目主页、模型权重或数据集链接。建议提交 PR 时保持以下格式统一：论文标题、Paper 链接、代码仓库、项目主页、Hugging Face 资源，以及所属研究方向。

## Citation

如果本项目对你的研究有帮助，欢迎引用原始 survey，并在使用本仓库整理内容时注明来源。BibTeX 信息将在后续版本中随论文正式发布信息进一步完善。

## License

本仓库仅用于学术研究与开源论文索引整理。论文版权归原作者及出版方所有，代码与数据资源请遵循各自仓库或项目页面的许可证。


