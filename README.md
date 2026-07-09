# Awesome Post-Training for Multimodal Large Language Models

> A rigorous and systematically organized survey repository on post-training methodologies for **Multimodal Large Language Models (MLLMs)**, covering instruction tuning, alignment learning, reasoning enhancement, domain adaptation, scalable training, and multimodal evaluation.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
![Topic](https://img.shields.io/badge/Topic-Multimodal%20LLMs-0f766e)
![Survey](https://img.shields.io/badge/Survey-Post--training-b31b1b)
![Format](https://img.shields.io/badge/Format-Markdown-1f6feb)
![Scope](https://img.shields.io/badge/Scope-Research%20Papers-7c3aed)

This repository accompanies the survey **A Survey on Post-training of Multimodal Large Language Models** and provides a curated, extensible, and research-oriented index of representative literature. The central perspective of the survey is to interpret MLLM post-training as a process of multimodal behavior shaping: after large-scale pre-training establishes broad cross-modal representations, post-training further calibrates model behavior through instruction data, preference feedback, reward signals, reasoning traces, domain-specific supervision, and scalable optimization recipes.

The repository is intended to serve as a practical academic map for researchers working on reliable and general-purpose multimodal intelligence. It organizes papers by methodological role, highlights the relationship between major post-training paradigms, and provides direct access to papers, code repositories, project pages, and model resources whenever available.

<p align="center">
  <img src="framework.png" width="92%" alt="Post-training framework for multimodal large language models">
</p>

<p align="center"><em>Structural overview of multimodal behavior-shaping post-training for MLLMs.</em></p>

---

## &#128204; Contents

| Section | Subsection |
| --- | --- |
| [&#129302; Multimodal Instruction Tuning](#multimodal-instruction-tuning) | [Representative Papers](#multimodal-instruction-tuning-papers) |
| [&#127942; Multimodal Alignment Learning](#multimodal-alignment-learning) | [Multimodal RLHF](#multimodal-rlhf), [Multimodal RLAIF](#multimodal-rlaif), [Multimodal Direct Preference Optimization](#multimodal-direct-preference-optimization) |
| [&#128640; Multimodal Reasoning Enhancement](#multimodal-reasoning-enhancement) | [R1-based Multimodal Reasoning](#r1-based-multimodal-reasoning), [Thinking with Images](#thinking-with-images), [Multimodal Self-Evolving](#multimodal-self-evolving), [Multimodal Distillation](#multimodal-distillation) |
| [&#129517; Multimodal Domain Adaptation](#multimodal-domain-adaptation) | Domain-oriented post-training for specialized multimodal scenarios |
| [&#9881;&#65039; Multimodal Scalable Training](#multimodal-scalable-training) | [LoRA-based Methods](#lora-based-methods), [MoE-based Methods](#moe-based-methods), [Compute-efficient Methods](#compute-efficient-methods) |
| [&#128202; Multimodal Benchmarks](#multimodal-benchmarks) | Benchmarks, evaluation protocols, and capability taxonomies |

---

# &#128214; Papers

## &#129302; Multimodal Instruction Tuning

Multimodal instruction tuning constitutes one of the earliest and most fundamental post-training paradigms for MLLMs. Its primary objective is to transform broad visual-language representations into instruction-following behavior by training on multimodal instruction-response data. This paradigm establishes the interface between user intent, multimodal input, and model output, thereby enabling MLLMs to respond to image-, video-, audio-, or interleaved multimodal prompts in a task-oriented manner.

The development of this line of research begins with representative systems such as LLaVA, MiniGPT-4, InstructBLIP, and mPLUG-Owl, which demonstrate the effectiveness of combining a visual encoder, a large language model, and curated instruction data. Subsequent studies extend this recipe toward higher-resolution perception, multi-image and video understanding, mobile deployment, visual prompt comprehension, data selection, mixture-of-experts adaptation, and generalized multimodal task transfer.

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

## &#127942; Multimodal Alignment Learning

Multimodal alignment learning aims to make MLLM outputs consistent with human preferences, factual evidence, safety requirements, and cross-modal semantic constraints. Compared with text-only alignment, multimodal alignment must additionally address visual hallucination, fine-grained localization errors, temporal inconsistency in videos, modality conflicts, and heterogeneous feedback granularity. The literature can be organized into three major paradigms: reinforcement learning from human feedback, reinforcement learning from AI feedback, and direct preference optimization.

### Multimodal RLHF

Multimodal RLHF introduces human feedback or human-derived reward signals to guide MLLMs toward more factual, helpful, and preference-aligned behavior. Existing methods construct reward models at different levels of granularity, including pair-level, span-level, step-level, and mixed-level feedback. Optimization procedures such as PPO, DDPO, process reward modeling, best-of-N sampling, reject sampling, and multi-objective reinforcement learning are used to improve alignment over image and video contexts.

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

Multimodal RLAIF reduces the cost and scalability limitations of human feedback by using stronger models, automatic evaluators, or structured AI feedback as supervisory signals. This paradigm is particularly valuable for video understanding, large-scale preference construction, and iterative alignment settings. Representative work explores context-aware reward modeling, open-source AI feedback, preference distillation, and iterative refinement for improving trustworthiness and alignment quality.

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Tuning Large Multimodal Models for Videos using Reinforcement Learning from AI Feedback](https://arxiv.org/pdf/2402.03746) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2402.03746) / [Code](https://github.com/yonseivnl/vlm-rlaif) / [Project](https://dcahn12.github.io/projects/vlm-rlaif/) |
| 2 | [RLAIF-V: Open-Source AI Feedback Leads to Super GPT-4V Trustworthiness](https://arxiv.org/pdf/2405.17220) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2405.17220) / [Code](https://github.com/RLHF-V/RLAIF-V) |
| 3 | [SILKIE: Preference Distillation for Large Visual Language Models](https://arxiv.org/pdf/2312.10665) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2312.10665) / [Code](https://github.com/vlf-silkie/VLFeedback) / [Project](https://vlf-silkie.github.io/) |

### Multimodal Direct Preference Optimization

Multimodal Direct Preference Optimization directly optimizes model policies from preference data without relying on an explicitly trained reward model. This family of methods is especially useful for mitigating multimodal hallucination, object-level inconsistency, modality-level conflict, and response-level preference errors. Recent work further extends DPO toward conditional preference objectives, vision-guided preference construction, difficulty-aware sampling, uncertainty-aware exploration, and on-policy data generation.

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

## &#128640; Multimodal Reasoning Enhancement

Multimodal reasoning enhancement focuses on strengthening the ability of MLLMs to solve complex tasks that require visual evidence, symbolic reasoning, spatial-temporal understanding, tool use, grounding, and multi-step inference. This research direction has rapidly expanded with the emergence of R1-style reinforcement learning, visually grounded reasoning, self-evolving training loops, and distillation-based capability transfer.

### R1-based Multimodal Reasoning

R1-based multimodal reasoning adapts reinforcement learning strategies inspired by R1-style reasoning models to vision-language and omni-modal settings. These methods typically optimize verifiable objectives such as answer correctness, reasoning format, visual grounding, or process-level reward. By reducing dependence on manually annotated reasoning traces, they provide a scalable route for improving mathematical reasoning, chart understanding, video reasoning, retrieval, and general multimodal problem solving.

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

Thinking with Images emphasizes explicit use of visual evidence during the reasoning process. Instead of compressing images into implicit context alone, these methods encourage models to reason over regions, points, crops, visual tools, latent visual structures, or grounded intermediate representations. This paradigm is crucial for tasks that require localization, visual planning, fine-grained perception, and tool-augmented multimodal reasoning.

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

Multimodal self-evolving methods study how MLLMs can improve through iterative loops of self-generated data, self-correction, critique, reflection, or unsupervised post-training. Rather than relying exclusively on static supervised datasets, these methods treat the model as both a learner and a data or feedback generator. This closed-loop formulation is particularly relevant for data-scarce, dynamically changing, or open-ended multimodal tasks.

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [VIGC: Visual Instruction Generation and Correction](https://arxiv.org/abs/2308.12714) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2308.12714) / [Code](https://github.com/opendatalab/VIGC) / [Project](https://opendatalab.github.io/VIGC) |
| 2 | [MindGYM: Enhancing Vision-Language Models via Synthetic Self-Challenging Questions](https://arxiv.org/abs/2503.09499) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2503.09499) / [Code](https://github.com/modelscope/data-juicer/tree/MindGYM) |
| 3 | [SRPO: Enhancing Multimodal LLM Reasoning via Reflection-Aware Reinforcement Learning](https://arxiv.org/abs/2506.01713) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2506.01713) / [Code](https://github.com/SUSTechBruce/SRPO_MLLMs) / [Project](https://srpo.pages.dev/) |
| 4 | [LLaVA-Critic: Learning to Evaluate Multimodal Models](https://arxiv.org/pdf/2410.02712) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/pdf/2410.02712) / [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-10-03-llava-critic/) |
| 5 | [MM-UPT: Unsupervised Post-Training for Multi-Modal LLM Reasoning via GRPO](https://arxiv.org/abs/2505.22453) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2505.22453) / [Code](https://github.com/waltonfuture/MM-UPT) / [HF](https://huggingface.co/WaltonFuture/Qwen2.5-VL-7B-MM-UPT-MMR1) |
| 6 | [LLaVA-Critic-R1: Your Critic Model is Secretly a Strong Policy Model](https://arxiv.org/abs/2509.00676) | Article | arXiv ![arXiv](https://img.shields.io/badge/arXiv-Paper-red) | [Paper](https://arxiv.org/abs/2509.00676) / [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) |

### Multimodal Distillation

Multimodal distillation transfers capabilities from stronger teacher models, preference models, or on-policy trajectories into smaller, more efficient, or more specialized student models. Beyond conventional compression, this paradigm also supports capability alignment: the student model is expected to preserve fine-grained visual perception, temporal grounding, multimodal reasoning, and cross-modal response quality. Recent work highlights on-policy distillation as an important mechanism for combining efficiency with robust multimodal capability transfer.

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

## &#129517; Multimodal Domain Adaptation

This section is reserved for domain-oriented post-training methods that adapt MLLMs to specialized multimodal scenarios, including medical reasoning, legal and financial analysis, education, graphical user interfaces, embodied intelligence, autonomous driving, scientific discovery, and other high-stakes application domains.

---

## &#9881;&#65039; Multimodal Scalable Training

This section organizes scalable post-training strategies that improve efficiency, modularity, and computational feasibility when adapting MLLMs across model scales, modalities, data regimes, and deployment constraints.

### LoRA-based Methods

This subsection covers parameter-efficient adaptation strategies based on LoRA, QLoRA, mixture-of-LoRA, conditional low-rank routing, and related low-rank update mechanisms for multimodal post-training.

### MoE-based Methods

This subsection covers mixture-of-experts architectures, expert routing, sparse activation, modular specialization, and expert-level knowledge transfer in scalable multimodal post-training.

### Compute-efficient Methods

This subsection covers efficient visual processing, visual token compression, long-context optimization, high-resolution perception, and training or inference strategies designed to reduce computational overhead while preserving multimodal capability.

---

## &#128202; Multimodal Benchmarks

This section organizes benchmarks, evaluation protocols, and capability taxonomies for assessing post-trained MLLMs. Relevant evaluation dimensions include instruction following, hallucination, safety, reasoning, grounding, OCR, chart understanding, multi-image interaction, video understanding, agentic behavior, embodied tasks, and domain-specific reliability.

---

## &#129309; Contributing

Contributions are welcome. Please feel free to submit pull requests that add new papers, code repositories, project pages, model checkpoints, datasets, or benchmark resources. To maintain consistency, each entry should include the paper title, paper link, resource links, venue information, and the most appropriate methodological category.

## &#128204; Citation

If this repository or the associated survey is useful for your research, please consider citing the original survey paper and acknowledging this curated paper list.

```bibtex
@article{zhang2026survey,
  title={A Survey on Post-training of Multimodal Large Language Models},
  author={Zhang, Haonan and Cao, Libin and Lai, Wenrui and Yu, Zhaoshu and Zhang, Sihan},
  year={2026}
}
```

## &#128196; License

This repository is intended for academic research and open-source literature organization. Copyright of the listed papers, codebases, datasets, and models belongs to their respective authors and publishers. Please follow the license terms of each linked resource.

