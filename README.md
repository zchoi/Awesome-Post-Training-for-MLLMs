# Awesome Post-Training for Multimodal Large Language Models

> ?????????????????????? Multimodal Instruction Tuning?Alignment Learning?Reasoning Enhancement ??????????????????

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re) ![Markdown](https://img.shields.io/badge/Format-Markdown-1f6feb) ![Topic](https://img.shields.io/badge/Topic-Multimodal%20LLMs-0f766e)

![Post-training framework for MLLMs](framework.png)

## Contents

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
- [Multimodal scalable training](#multimodal-scalable-training)
  - [LoRA-based methods](#lora-based-methods)
  - [MoE-based methods](#moe-based-methods)
  - [compute-efficient methods](#compute-efficient-methods)
- [Multimodal Benchmarks](#multimodal-benchmarks)

## Overview

????????????????????????????????????Table 1 ??????????Table 2 ??????????Table 3 ????????????????????????????????????

???????????????????? Paper?Type?Venue ? Resources ????? Resources ?????????????????? Hugging Face ???

## Multimodal Instruction Tuning

???????? MLLM ?????????????????????OCR????GUI??????????????????????????????????? LLaVA?MiniGPT-4?InstructBLIP ????????????????????????/???????MoE?????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Visual Instruction Tuning](https://arxiv.org/pdf/2304.08485) | Article | arXiv | [Code](https://github.com/haotian-liu/LLaVA) / [Project](https://llava-vl.github.io/) |
| 2 | [MiniGPT-4: Enhancing Vision-Language Understanding with Advanced Large Language Models](https://arxiv.org/pdf/2304.10592) | Article | arXiv | [Code](https://github.com/Vision-CAIR/MiniGPT-4) / [Project](https://minigpt-4.github.io/) |
| 3 | [InstructBLIP: Towards General-purpose Vision-Language Models with Instruction Tuning](https://arxiv.org/pdf/2305.06500) | Article | arXiv | [Code](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip) |
| 4 | [mPLUG-Owl: Modularization Empowers Large Language Models with Multimodality](https://arxiv.org/pdf/2304.14178) | Article | arXiv | [Code](https://github.com/X-PLUG/mPLUG-Owl) |
| 5 | [LLaMA-Adapter V2: Parameter-Efficient Visual Instruction Model](https://arxiv.org/pdf/2304.15010) | Article | arXiv | [Code](https://github.com/OpenGVLab/LLaMA-Adapter) |
| 6 | [Improved Baselines with Visual Instruction Tuning](https://arxiv.org/pdf/2310.03744) | Article | arXiv | [Code](https://github.com/haotian-liu/LLaVA) / [Project](https://llava-vl.github.io/) |
| 7 | [Qwen-VL: A Versatile Vision-Language Model for Understanding, Localization, Text Reading, and Beyond](https://arxiv.org/pdf/2308.12966) | Article | arXiv | [Code](https://github.com/QwenLM/Qwen-VL) |
| 8 | [CogVLM: Visual Expert for Pretrained Language Models](https://arxiv.org/pdf/2311.03079) | Article | arXiv | [Code](https://github.com/THUDM/CogVLM) |
| 9 | [How Far Are We to GPT-4V? Closing the Gap to Commercial Multimodal Models with Open-Source Suites](https://arxiv.org/pdf/2404.16821) | Article | arXiv | [Code](https://github.com/OpenGVLab/InternVL) |
| 10 | LLaVA-NeXT: Improved reasoning, OCR, and world knowledge | Model | - | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-01-30-llava-next/) |
| 11 | [What matters when building vision-language models?](https://arxiv.org/pdf/2405.02246) | Article | arXiv | [HF](https://huggingface.co/blog/idefics2) |
| 12 | [Qwen2-VL: Enhancing Vision-Language Model's Perception of the World at Any Resolution](https://arxiv.org/pdf/2409.12191) | Article | arXiv | [Code](https://github.com/QwenLM/Qwen2-VL) |
| 13 | [LLaVA-OneVision: Easy Visual Task Transfer](https://arxiv.org/pdf/2408.03326) | Article | arXiv | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT/blob/main/docs/LLaVA_OneVision.md) / [Project](https://llava-vl.github.io/blog/2024-08-05-llava-onevision/) |
| 14 | [Expanding Performance Boundaries of Open-Source Multimodal Models with Model, Data, and Test-Time Scaling](https://arxiv.org/pdf/2412.05271) | Article | arXiv | [Code](https://github.com/OpenGVLab/InternVL) / [Project](https://internvl.github.io/blog/2024-12-05-InternVL-2.5/) |
| 15 | [Qwen2.5-VL Technical Report](https://arxiv.org/pdf/2502.13923) | Article | arXiv | [Code](https://github.com/QwenLM/Qwen2.5-VL) |
| 16 | [VILA: On Pre-training for Visual Language Models](https://arxiv.org/pdf/2312.07533) | Article | arXiv | [Code](https://github.com/NVlpdf/VILA) |
| 17 | [MobileVLM : A Fast, Strong and Open Vision Language Assistant for Mobile Devices](https://arxiv.org/pdf/2312.16886) | Article | arXiv | [Code](https://github.com/Meituan-AutoML/MobileVLM) |
| 18 | [DeepSeek-VL: Towards Real-World Vision-Language Understanding](https://arxiv.org/pdf/2403.05525) | Article | arXiv | [Code](https://github.com/deepseek-ai/DeepSeek-VL) |
| 19 | [Yi: Open Foundation Models by 01.AI](https://arxiv.org/pdf/2403.04652) | Article | arXiv | [Code](https://github.com/01-ai/Yi) / [HF](https://huggingface.co/01-ai/Yi-VL-6B) |
| 20 | [Cambrian-1: A Fully Open, Vision-Centric Exploration of Multimodal LLMs](https://arxiv.org/pdf/2406.16860) | Article | arXiv | [Code](https://github.com/cambrian-mllm/cambrian) / [Project](https://cambrian-mllm.github.io/) |
| 21 | [MiniCPM-V: A GPT-4V Level MLLM on Your Phone](https://arxiv.org/pdf/2408.01800) | Article | arXiv | [Code](https://github.com/OpenBMB/MiniCPM-V) / [Project](https://huggingface.co/openbmb/MiniCPM-V-2_6) |
| 22 | [Phi-3 Technical Report: A Highly Capable Language Model Locally on Your Phone](https://arxiv.org/pdf/2404.14219) | Article | arXiv | [HF](https://huggingface.co/microsoft/Phi-3.5-vision-instruct) |
| 23 | Llama-3.2-Vision-Instruct | Model | - | [HF](https://huggingface.co/meta-llama/Llama-3.2-11B-Vision-Instruct) |
| 24 | [Molmo and PixMo: Open Weights and Open Data for State-of-the-Art Vision-Language Models](https://arxiv.org/pdf/2409.17146) | Article | arXiv | [Code](https://github.com/allenai/molmo) / [Project](https://molmo.allenai.org/) |
| 25 | [Pixtral-12B](https://arxiv.org/pdf/2410.07073) | Article | arXiv | [Project](https://mistral.ai/news/pixtral-12b) |
| 26 | [Aria: An Open Multimodal Native Mixture-of-Experts Model](https://arxiv.org/pdf/2410.05993) | Article | arXiv | [Code](https://github.com/rhymes-ai/Aria) |
| 27 | [PaliGemma: A versatile 3B VLM for transfer](https://arxiv.org/pdf/2407.07726) | Article | arXiv | [HF](https://huggingface.co/google/paligemma-3b-mix-224) |
| 28 | [Otter: A Multi-Modal Model with In-Context Instruction Tuning](https://arxiv.org/pdf/2305.03726) | Article | arXiv | [Code](https://github.com/Luodian/Otter) |
| 29 | [LLaMA-Adapter: Efficient Fine-tuning of Language Models with Zero-init Attention](https://arxiv.org/pdf/2303.16199) | Article | arXiv | [Code](https://github.com/OpenGVLab/LLaMA-Adapter) |
| 30 | [Cheap and Quick: Efficient Vision-Language Instruction Tuning for Large Language Models](https://arxiv.org/pdf/2305.15023) | Article | arXiv | [Code](https://github.com/luogen1996/LaVIN) |
| 31 | [Valley: Video Assistant with Large Language model Enhanced abilitY](https://arxiv.org/pdf/2306.07207) | Article | arXiv | [Code](https://github.com/RupertLuo/Valley) |
| 32 | [NExT-GPT: Any-to-Any Multimodal LLM](https://arxiv.org/pdf/2309.05519) | Article | arXiv | [Code](https://github.com/NExT-GPT/NExT-GPT) / [Project](https://next-gpt.github.io/) |
| 33 | [InternVL: Scaling up Vision Foundation Models and Aligning for Generic Visual-Linguistic Tasks](https://arxiv.org/pdf/2312.14238) | Article | arXiv | [Code](https://github.com/OpenGVLab/InternVL) |
| 34 | [Parrot: Multilingual Visual Instruction Tuning](https://arxiv.org/pdf/2406.02539) | Article | arXiv | [Code](https://github.com/AIDC-AI/Parrot) |
| 35 | [Generative Visual Instruction Tuning](https://arxiv.org/pdf/2406.11262) | Article | arXiv | [Code](https://github.com/jeffhernandez1995/GenLlaVA) |
| 36 | [PPLLaVA: Varied Video Sequence Understanding With Prompt Guidance](https://arxiv.org/pdf/2411.02327) | Article | arXiv | - |
| 37 | [MLAN: Language-Based Instruction Tuning Preserves and Transfers Knowledge in Multimodal Language Models](https://arxiv.org/pdf/2411.10557) | Article | arXiv | - |
| 38 | [INST-IT: Boosting Instance Understanding via Explicit Visual Prompt Instruction Tuning](https://arxiv.org/pdf/2412.03565) | Article | arXiv | [Code](https://github.com/inst-it/inst-it) / [Project](https://inst-it.github.io/) |
| 39 | [Comparison Visual Instruction Tuning](https://arxiv.org/pdf/2406.09240) | Article | arXiv | [Code](https://github.com/wlin-at/CaD-VI) / [Project](https://wlin-at.github.io/cad_vi) / [HF](https://huggingface.co/datasets/wlin21at/CaD-Inst) |
| 40 | [Multimodal Instruction Tuning with Conditional Mixture of LoRA](https://arxiv.org/pdf/2402.15896) | Article | arXiv | [Code](https://github.com/PLUM-Lab/MixLoRA) |
| 41 | [Do we Really Need Visual Instructions? Towards Visual Instruction-Free Fine-tuning for Large Vision-Language Models](https://arxiv.org/pdf/2502.11427) | Article | arXiv | - |
| 42 | [Re-Imagining Multimodal Instruction Tuning: A Representation View](https://arxiv.org/pdf/2503.00723) | Article | arXiv | - |
| 43 | [Learning to Instruct for Visual Instruction Tuning](https://arxiv.org/pdf/2503.22215) | Article | arXiv | [Code](https://github.com/Feng-Hong/L2T) |
| 44 | [Visual Compositional Tuning](https://arxiv.org/pdf/2504.21850) | Article | arXiv | [Code](https://github.com/princetonvisualai/compact) / [Project](https://princetonvisualai.github.io/compact/) |
| 45 | [Visual Instruction Bottleneck Tuning](https://arxiv.org/pdf/2505.13946) | Article | arXiv | [Code](https://github.com/deeplearning-wisc/vittle) |
| 46 | [LLaDA-V: Large Language Diffusion Models with Visual Instruction Tuning](https://arxiv.org/pdf/2505.16933) | Article | arXiv | [Code](https://ml-gsai.github.io/LLaDA-V-demo/) / [Project](https://ml-gsai.github.io/LLaDA-V-demo/) |
| 47 | [MINT: Multimodal Instruction Tuning with Multimodal Interaction Grouping](https://arxiv.org/pdf/2506.02308) | Article | arXiv | [Code](https://github.com/sxj1215/MINT) |
| 48 | [CoIDO: Efficient Data Selection for Visual Instruction Tuning via Coupled Importance-Diversity Optimization](https://arxiv.org/pdf/2510.17847) | Article | arXiv | [Code](https://github.com/SuDIS-ZJU/CoIDO) |
| 49 | Data Selection Matters: Towards Robust Instruction Tuning of Large Multimodal Models | Model | - | [Code](https://github.com/xyang583/ARDS) / [Project](https://papers.neurips.cc/paper_files/paper/2025/hash/0d77ccb50a558035f19089096f933e8e-Abstract-Conference.html) |
| 50 | [SAME: Stabilized Mixture-of-Experts for Multimodal Continual Instruction Tuning](https://arxiv.org/pdf/2602.01990) | Article | arXiv | [Code](https://github.com/LAMDA-CL/Prism) |
| 51 | [Less Data, Faster Convergence: Goal-Driven Data Optimization for Multimodal Instruction Tuning](https://arxiv.org/pdf/2603.12478) | Article | arXiv | [Code](https://github.com/rujiewu/GDO) |
| 52 | [LLaVA-NeXT-Interleave: Tackling Multi-image, Video, and 3D in Large Multimodal Models](https://arxiv.org/pdf/2407.07895) | Article | arXiv | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-06-16-llava-next-interleave/) |
| 53 | [MAVIS: Mathematical Visual Instruction Tuning with an Automatic Data Engine](https://arxiv.org/pdf/2407.08739) | Article | arXiv | [Code](https://github.com/ZrrSkywalker/MAVIS) |
| 54 | [MANTIS: Interleaved Multi-Image Instruction Tuning](https://arxiv.org/pdf/2405.01483) | Article | arXiv | [Code](https://github.com/OpenGVLab/LLaMA-Adapter/tree/main/imagebind_LLM) / [Project](https://tiger-ai-lab.github.io/Mantis/) |
| 55 | [ImageBind-LLM: Multi-modality Instruction Tuning](https://arxiv.org/pdf/2309.03905) | Article | arXiv | [Code](https://github.com/OpenGVLab/LLaMA-Adapter/tree/main/imagebind_LLM) |
| 56 | [ShareGPT4V: Improving Large Multi-Modal Models with Better Captions](https://arxiv.org/pdf/2311.12793) | Article | arXiv | [Code](https://github.com/ShareGPT4Omni/ShareGPT4V) / [Project](https://sharegpt4v.github.io/) |
| 57 | [MiniGPT-v2: large language model as a unified interface for vision-language multi-task learning](https://arxiv.org/pdf/2310.09478) | Article | arXiv | [Code](https://github.com/Vision-CAIR/MiniGPT-4) / [Project](https://minigpt-v2.github.io/) |
| 58 | [ViP-LLaVA: Making Large Multimodal Models Understand Arbitrary Visual Prompts](https://arxiv.org/pdf/2312.00784) | Article | arXiv | [Code](https://github.com/WisconsinAIVision/ViP-LLaVA) / [Project](https://vip-llava.github.io/) |
| 59 | [LLaVA-UHD: an LMMPerceiving Any Aspect Ratio and High-Resolution Images](https://arxiv.org/pdf/2403.11703) | Article | arXiv | [Code](https://github.com/thunlp/LLaVA-UHD) |
| 60 | [CogAgent: A Visual Language Model for GUI Agents](https://arxiv.org/pdf/2312.08914) | Article | arXiv | [Code](https://github.com/zai-org/CogAgent) |
| 61 | [Monkey :ImageResolutionandText Label Are Important Things for Large Multi-modal Models](https://arxiv.org/pdf/2311.06607) | Article | arXiv | [Code](https://github.com/Yuliang-Liu/Monkey) |
| 62 | [Mini-Gemini: Mining the Potential of Multi-modality Vision Language Models](https://arxiv.org/pdf/2403.18814v1) | Article | arXiv | [Code](https://github.com/JIA-Lab-research/MGM) |
| 63 | [Feast Your Eyes: Mixture-of-Resolution Adaptation for Multimodal Large Language Models](https://arxiv.org/pdf/2403.03003) | Article | arXiv | [Code](https://github.com/luogen1996/LLaVA-HR) |
| 64 | [SPHINX: The Joint Mixing of Weights, Tasks, and Visual Embeddings for Multi-modal Large Language Models](https://arxiv.org/pdf/2311.07575) | Article | arXiv | [Code](https://github.com/Alpha-VLLM/LLaMA2-Accessory) |
| 65 | [MoAI: Mixture of All Intelligence for Large Language and Vision Models](https://arxiv.org/pdf/2403.07508) | Article | arXiv | [Code](https://github.com/ByungKwanLee/MoAI) |

## Multimodal Alignment Learning

???????????????????????????????????????????????????????????????????????????????????????????

### Multimodal RLHF

????????????????????????????????????????????????????????????? LLaVA-RLHF?RLHF-V ??? VisualPRM?MM-RLHF ???????????????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [ALIGNING LARGE MULTIMODAL MODELS WITH FACTUALLY AUGMENTED RLHF](https://arxiv.org/pdf/2309.14525) | Article | arXiv | [Code](https://github.com/llava-rlhf/LLaVA-RLHF) / [Project](https://llava-rlhf.github.io/) |
| 2 | [RLHF-V: Towards Trustworthy MLLMs via Behavior Alignment from Fine-grained Correctional Human Feedback](https://arxiv.org/pdf/2312.00849) | Article | arXiv | [Code](https://github.com/RLHF-V/RLHF-V) / [Project](https://rlhf-v.github.io/) |
| 3 | [VisualPRM: An Effective Process Reward Model for Multimodal Reasoning](https://arxiv.org/pdf/2503.10291) | Article | arXiv | [Project](https://internvl.github.io/blog/2025-03-13-VisualPRM/) |
| 4 | [Gemini: A Family of Highly Capable Multimodal Models](https://arxiv.org/pdf/2312.11805) | Article | arXiv | [Project](https://deepmind.google/technologies/gemini/) |
| 5 | [MM-RLHF: The Next Step Forward in Multimodal LLM Alignment](https://arxiv.org/pdf/2502.10391) | Article | arXiv | [Code](https://github.com/Kwai-YuanQi/MM-RLHF) / [Project](https://mm-rlhf.github.io/) |
| 6 | [Seed1.5-VL Technical Report](https://arxiv.org/pdf/2505.07062) | Article | arXiv | [Code](https://github.com/ByteDance-Seed/Seed1.5-VL) / [Project](https://seed.bytedance.com/en/tech/seed1_5_vl) |
| 7 | [MiMo-VL Technical Report](https://arxiv.org/pdf/2506.03569) | Article | arXiv | [Code](https://github.com/XiaomiMiMo/MiMo-VL) |

### Multimodal RLAIF

????? AI Feedback ????????????????????????????????????????????????????????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Tuning Large Multimodal Models for Videos using Reinforcement Learning from AI Feedback](https://arxiv.org/pdf/2402.03746) | Article | arXiv | [Code](https://github.com/yonseivnl/vlm-rlaif) / [Project](https://dcahn12.github.io/projects/vlm-rlaif/) |
| 2 | [RLAIF-V: Open-Source AI Feedback Leads to Super GPT-4V Trustworthiness](https://arxiv.org/pdf/2405.17220) | Article | arXiv | [Code](https://github.com/RLHF-V/RLAIF-V) |
| 3 | [SILKIE: Preference Distillation for Large Visual Language Models](https://arxiv.org/pdf/2312.10665) | Article | arXiv | [Code](https://github.com/vlf-silkie/VLFeedback) / [Project](https://vlf-silkie.github.io/) |

### Multimodal Direct Preference Optimization

????????????????????????????????????????????????????????? on-policy ????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [Direct Preference Optimization of Video Large Multimodal Models from Language Model Reward](https://arxiv.org/pdf/2404.01258) | Article | arXiv | [Code](https://github.com/RifleZhang/LLaVA-Hound-DPO) |
| 2 | [ISR-DPO: Aligning Large Multimodal Models for Videos by Iterative Self-Retrospective DPO](https://arxiv.org/pdf/2406.11280) | Article | arXiv | [Code](https://github.com/snumprlab/isr-dpo) / [Project](https://dcahn12.github.io/projects/isr-dpo/) |
| 3 | [Beyond Hallucinations: Enhancing LVLMs through Hallucination-Aware Direct Preference Optimization](https://arxiv.org/pdf/2311.16839) | Article | arXiv | [Code](https://github.com/opendatalab/HA-DPO) / [Project](https://opendatalab.github.io/HA-DPO/) |
| 4 | [Mitigating Hallucination in Multimodal Large Language Model via Hallucination-targeted Direct Preference Optimization](https://arxiv.org/pdf/2411.10436) | Article | arXiv | - |
| 5 | [V-DPO: Mitigating Hallucination in Large Vision Language Models via Vision-Guided Direct Preference Optimization](https://arxiv.org/pdf/2411.02712) | Article | arXiv | [Code](https://github.com/YuxiXie/V-DPO) |
| 6 | [CLIP-DPO: Vision-Language Models as a Source of Preference for Fixing Hallucinations in LVLMs](https://arxiv.org/pdf/2408.10433) | Article | arXiv | - |
| 7 | [Mitigating Hallucinations in Multimodal LLMs via Object-aware Preference Optimization](https://arxiv.org/pdf/2508.20181) | Article | arXiv | [Code](https://github.com/aimagelab/CHAIR-DPO) |
| 8 | [MDPO: Conditional Preference Optimization for Multimodal Large Language Models](https://arxiv.org/pdf/2406.11839) | Article | arXiv | [Code](https://github.com/luka-group/mDPO) / [Project](https://feiwang96.github.io/mDPO/) |
| 9 | PEA-DPO: Perception-Enhanced Alignment Direct Preference Optimization for MLLMs Alignment | Model | - | [Project](https://openreview.net/forum?id=uZ5AmOJKqV) |
| 10 | [MoD-DPO: Towards Mitigating Cross-modal Hallucinations in Omni LLMs using Modality Decoupled Preference Optimization](https://arxiv.org/pdf/2603.03192) | Article | arXiv | [Project](https://mod-dpo.github.io/) |
| 11 | [OMNI DPO: A Preference Optimization Framework to Address Omni-Modal Hallucination](https://arxiv.org/pdf/2509.00723) | Article | arXiv | - |
| 12 | [DA-DPO: Cost-efficient Difficulty-aware Preference Optimization for Reducing MLLM Hallucinations](https://arxiv.org/pdf/2601.00623) | Article | arXiv | [Code](https://github.com/Artanic30/DA-DPO) / [Project](https://artanic30.github.io/project_pages/DA-DPO/) |
| 13 | [Uncertainty-Aware Exploratory Direct Preference Optimization for Multimodal Large Language Models](https://arxiv.org/pdf/2605.04874) | Article | arXiv | - |
| 14 | [Mitigating Hallucinations in Large Vision-Language Models via DPO: On-Policy Data Hold the Key](https://arxiv.org/pdf/2501.09695) | Article | arXiv | [Code](https://github.com/zhyang2226/OPA-DPO) / [Project](https://opa-dpo.github.io/) |
| 15 | [LPOI: Listwise Preference Optimization for Vision Language Models](https://arxiv.org/pdf/2505.21061) | Article | arXiv | [Code](https://github.com/fatemehpesaran310/lpoi) |

## Multimodal Reasoning Enhancement

?????????????????????????????????????????????????????????????????? R1-style ??????????????????? on-policy distillation ????

### R1-based Multimodal Reasoning

????? R1-style ??????????????GRPO?????????????????????????????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [VLM-R1: A Stable and Generalizable R1-style Large Vision-Language Model](https://arxiv.org/abs/2504.07615) | Article | arXiv | [Code](https://github.com/om-ai-lab/VLM-R1) |
| 2 | [Visual-RFT: Visual Reinforcement Fine-Tuning](https://arxiv.org/abs/2503.01785) | Article | arXiv | [Code](https://github.com/Liuziyu77/Visual-RFT) |
| 3 | [Vision-R1: Incentivizing Reasoning Capability in Multimodal Large Language Models](https://arxiv.org/abs/2503.06749) | Article | arXiv | [Code](https://github.com/Osilly/Vision-R1) |
| 4 | [VideoChat-R1: Enhancing Spatio-Temporal Perception via Reinforcement Fine-Tuning](https://arxiv.org/abs/2504.06958) | Article | arXiv | [Code](https://github.com/OpenGVLab/VideoChat-R1) |
| 5 | [Video-R1: Reinforcing Video Reasoning in MLLMs](https://arxiv.org/abs/2503.21776) | Article | arXiv | [Code](https://github.com/tulerfeng/Video-R1) |
| 6 | [VisualPRM: An Effective Process Reward Model for Multimodal Reasoning](https://arxiv.org/abs/2503.10291) | Article | arXiv | [Code](https://github.com/OpenGVLab/InternVL) / [Project](https://internvl.github.io/blog/2025-03-13-VisualPRM/) / [HF](https://huggingface.co/OpenGVLab/VisualPRM-8B) |
| 7 | [R1-VL: Learning to Reason with Multimodal Large Language Models via Step-wise Group Relative Policy Optimization](https://arxiv.org/abs/2503.12937) | Article | arXiv | - |
| 8 | [R1-Zero's "Aha Moment" in Visual Reasoning on a 2B Non-SFT Model](https://arxiv.org/abs/2503.05132) | Article | arXiv | [Code](https://github.com/turningpoint-ai/VisualThinker-R1-Zero) |
| 9 | [MM-Eureka: Exploring the Frontiers of Multimodal Reasoning with Rule-based Reinforcement Learning](https://arxiv.org/abs/2503.07365) | Article | arXiv | [Code](https://github.com/ModalMinds/MM-EUREKA) / [HF](https://huggingface.co/FanqingM/MM-Eureka-8B) |
| 10 | [R1-Onevision: Advancing Generalized Multimodal Reasoning through Cross-Modal Formalization](https://arxiv.org/abs/2503.10615) | Article | arXiv | [Code](https://github.com/Fancy-MLLM/R1-onevision) |
| 11 | [R1-Omni: Explainable Omni-Multimodal Emotion Recognition with Reinforcement Learning](https://arxiv.org/abs/2503.05379) | Article | arXiv | [Code](https://github.com/HumanMLLM/R1-Omni) |
| 12 | [Retrv-R1: A Reasoning-Driven MLLM Framework for Universal and Efficient Multimodal Retrieval](https://arxiv.org/abs/2510.02745) | Article | arXiv | [Code](https://lanyunzhu.site/RetrvR1/) / [Project](https://lanyunzhu.site/RetrvR1/) |

### Thinking with Images

??????????????????????????????? grounded intermediate representation?????????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [GRIT: Teaching MLLMs to Think with Images](https://arxiv.org/abs/2505.15879) | Article | arXiv | [Code](https://github.com/eric-ai-lab/GRIT) / [Project](https://grounded-reasoning.github.io/) |
| 2 | [Point-RFT: Improving Multimodal Reasoning with Visually Grounded Reinforcement Finetuning](https://arxiv.org/abs/2505.19702) | Article | arXiv | - |
| 3 | [OpenThinkIMG: Learning to Think with Images via Visual Tool Reinforcement Learning](https://arxiv.org/abs/2505.08617) | Article | arXiv | [Code](https://github.com/OpenThinkIMG/OpenThinkIMG) / [HF](https://huggingface.co/collections/Warrieryes/openthinkimg) |
| 4 | [VisionReasoner: Unified Reasoning-Integrated Visual Perception via Reinforcement Learning](https://arxiv.org/abs/2505.12081) | Article | arXiv | [Code](https://github.com/dvlab-research/VisionReasoner) |
| 5 | [DeepEyes: Incentivizing "Thinking with Images" via Reinforcement Learning](https://arxiv.org/abs/2505.14362) | Article | arXiv | [Code](https://github.com/Visual-Agent/DeepEyes) / [HF](https://huggingface.co/ChenShawn/DeepEyes-7B) |
| 6 | [VTool-R1: VLMs Learn to Think with Images via Reinforcement Learning on Multimodal Tool Use](https://arxiv.org/abs/2505.19255) | Article | arXiv | [Code](https://github.com/VTOOL-R1/vtool-r1) / [Project](https://vtool-r1.github.io/) |
| 7 | [Visual Planning: Let's Think Only with Images](https://arxiv.org/abs/2505.11409) | Article | arXiv | [Code](https://github.com/yix8/VisualPlanning) |
| 8 | [LanteRn: Latent Visual Structured Reasoning](https://arxiv.org/abs/2603.25629) | Article | arXiv | [Code](https://github.com/GuilhermeViveiros/LantErn) / [HF](https://huggingface.co/AGViveiros/LanteRn-3B-RL) |

### Multimodal Self-Evolving

?????????????????????????????????????????????????????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [VIGC: Visual Instruction Generation and Correction](https://arxiv.org/abs/2308.12714) | Article | arXiv | [Code](https://github.com/opendatalab/VIGC) / [Project](https://opendatalab.github.io/VIGC) |
| 2 | [MindGYM: Enhancing Vision-Language Models via Synthetic Self-Challenging Questions](https://arxiv.org/abs/2503.09499) | Article | arXiv | [Code](https://github.com/modelscope/data-juicer/tree/MindGYM) |
| 3 | [SRPO: Enhancing Multimodal LLM Reasoning via Reflection-Aware Reinforcement Learning](https://arxiv.org/abs/2506.01713) | Article | arXiv | [Code](https://github.com/SUSTechBruce/SRPO_MLLMs) / [Project](https://srpo.pages.dev/) |
| 4 | [LLaVA-Critic: Learning to Evaluate Multimodal Models](https://arxiv.org/pdf/2410.02712) | Article | arXiv | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) / [Project](https://llava-vl.github.io/blog/2024-10-03-llava-critic/) |
| 5 | [MM-UPT: Unsupervised Post-Training for Multi-Modal LLM Reasoning via GRPO](https://arxiv.org/abs/2505.22453) | Article | arXiv | [Code](https://github.com/waltonfuture/MM-UPT) / [HF](https://huggingface.co/WaltonFuture/Qwen2.5-VL-7B-MM-UPT-MMR1) |
| 6 | [LLaVA-Critic-R1: Your Critic Model is Secretly a Strong Policy Model](https://arxiv.org/abs/2509.00676) | Article | arXiv | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) |

### Multimodal Distillation

???????????????MoE ??? on-policy distillation ????????????????????????????????????????

| # | Paper | Type | Venue | Resources |
|---:|---|---|---|---|
| 1 | [LLaVA-KD: A Framework of Distilling Multimodal Large Language Models](https://arxiv.org/abs/2410.16236) | Article | arXiv | [Code](https://github.com/Fantasyele/LLaVA-KD) |
| 2 | [LLAVADI: What Matters For Multimodal Large Language Models Distillation](https://arxiv.org/abs/2407.19409) | Article | arXiv | - |
| 3 | [Silkie: Preference Distillation for Large Visual Language Models](https://arxiv.org/abs/2312.10665) | Article | arXiv | [Code](https://github.com/vlf-silkie/VLFeedback) / [Project](https://vlf-silkie.github.io/) / [HF](https://huggingface.co/MMInstruction/Silkie) |
| 4 | [LLaVA-MoD: Making LLaVA Tiny via MoE Knowledge Distillation](https://arxiv.org/abs/2408.15881) | Article | arXiv | [Code](https://github.com/shufangxun/LLaVA-MoD) |
| 5 | [Video-OPD: Efficient Post-Training of Multimodal Large Language Models for Temporal Video Grounding via On-Policy Distillation](https://arxiv.org/abs/2602.02994) | Article | arXiv | - |
| 6 | [X-OPD: Cross-Modal On-Policy Distillation for Capability Alignment in Speech LLMs](https://arxiv.org/abs/2603.24596) | Article | arXiv | - |
| 7 | [Uni-OPD: Unifying On-Policy Distillation with a Dual-Perspective Recipe](https://arxiv.org/abs/2605.03677) | Article | arXiv | [Code](https://github.com/WenjinHou/Uni-OPD) |
| 8 | [Vision-OPD: Learning to See Fine Details for Multimodal LLMs via On-Policy Self-Distillation](https://arxiv.org/abs/2605.18740) | Article | arXiv | [Code](https://github.com/VisionOPD/Vision-OPD) |
| 9 | [VA-OPD: Visual-Advantage On-Policy Distillation for Vision-Language Models](https://arxiv.org/abs/2605.21924) | Article | arXiv | - |

## Multimodal Domain Adaptation

> ????????????? Table 4 ???????????????

## Multimodal scalable training

> ????????????? Table 5?Table 6?Table 7 ????????????

### LoRA-based methods

> ????

### MoE-based methods

> ????

### compute-efficient methods

> ????

## Multimodal Benchmarks

> ????????????? Table 8?Table 9 ??????????

## Citation

????????????????? Star?Fork ??? Pull Request ?????????????????? BibTeX ???

## Contributing

?????????????????????????????? PR ??????????????????/??????????????

## License

???????????????????????????????????????????????????
