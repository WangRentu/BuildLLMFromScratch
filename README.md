# BuildLLMFromScratch

## 简介

本项目旨在通过 PyTorch 从零实现一个类似 GPT-2 的大规模语言模型框架。虽然项目名称中涉及 “GPT2” 和 “LLM”，但是项目不仅包括预训练（PreTraining）、模型参数加载、微调（FineTuning）和评估（Evaluate）的完整流程，而且还详细解释了每个环节的实现原理和代码逻辑。因为项目覆盖了从数据预处理到模型评估的全过程。

## 功能概述

整个项目从最初的数据准备开始，逐步实现注意力机制、搭建模型架构、进行预训练、构造训练循环，并最终实现微调与评估。虽然每一步都独立且复杂，但是正是因为各阶段之间紧密的联系，才使得整个框架具备了高度的连贯性和可扩展性。

## 仓库结构与模块说明

仓库中主要包含以下部分：

1. **数据准备与采样**  
   在 `Stage1.1DataPreparationSampling.ipynb` 中，首先对原始数据进行预处理与采样。因为数据是模型训练的基础，所以这一步骤十分关键，直接影响后续模型的效果。

2. **注意力机制实现**  
   通过 `Stage1.2AttentionMechanism.ipynb`，项目展示了如何构建注意力机制。这里的 “Attention” 可以拆解为 “attend”（关注）加上名词后缀 “-tion”，表示一个关注过程。因为注意力机制帮助模型捕捉输入序列中的关键部分，所以在自然语言处理任务中显得尤为重要。

3. **模型架构搭建**  
   在 `Stage1.3LLMArchitecture.ipynb` 中，搭建了类似 GPT-2 的模型架构。

4. **预训练阶段**  
   在 `Stage2.1PreTraining.ipynb` 中，使用大规模数据对模型进行预训练。预训练就是在正式任务训练前进行的基础性训练，为后续微调打下基础。

5. **训练循环**  
   接着在 `Stage2.2TrainLoop.ipynb` 中，通过详细的代码讲解了训练循环的构造。虽然训练循环是深度学习中常见的模式，但是通过逐步解析每一行代码，可以帮助读者理解模型训练的内部逻辑。

6. **与 OpenAI GPT-2 对比**  
   在 `Stage2.3OpenAIGPT2.ipynb` 中，通过对比 OpenAI 的 GPT-2 模型，验证了项目实现的有效性。因为对比可以帮助发现差异和改进方向，所以这一环节非常具有参考意义。

7. **微调与评估**  
   最后，在 `Stage3.1FinetuningForClassifier.ipynb`、`Stage3.2FinetuningForInstruction.ipynb` 与 `Stage3.3LoadandEvalLLM.ipynb` 中，分别展示了如何对模型进行微调以及如何加载和评估模型。这里 “FineTuning” 中的 “Fine” 表示精细化，“Tuning” 则代表调整，二者结合意味着对模型进行更精确的训练。

## 环境与依赖

因为项目基于 PyTorch 实现，所以需要先安装以下依赖：

```bash
pip install torch torchvision
```
## 重要参考
1. https://github.com/rasbt/LLMs-from-scratch/tree/main
2. https://www.youtube.com/watch?v=Xpr8D6LeAtw&t=17s