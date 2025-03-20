# Graudation_Essay
**My recording of Graduation Essay(Include endnote files to cite)**

## 摘要
- 阐述研究背景和目的
- 引出在研究中主要的实验过程

## 一、引言
- 1.1 研究目的
- 1.2 研究内容和创新点
- 1.3 小结

## 二、国内外研究现状
- 2.1 大模型发展经历溯源 (from bert to QWEN)
- 2.2 推理大模型发展经历溯源 (Deepseek Math，Numina Math Models，GPT O1，Kimi1.5 long context，Deepseek R1)
- 2.3 大模型微调发展
- 2.4 大模型强化学习的发展
- 2.5 推理优化的发展+量化剪枝+MoE+推理框架

## 三、相关技术研究和实验设计
- 3.1 Transformer模型架构分析
- 3.2 Qwen模型架构分析
  - 3.2.1 Qwen
  - 3.2.2 Qwen2
  - 3.2.3 Qwen2.5  
- 3.3 SFT、RFT的相关公式和原理解析~有监督微调原理
  - 3.3.1  SFT
  - 3.3.2  RFT
- 3.4 常规PPO、DPO加GPRO公式原理解析～大模型强化学习原理解析
  - 3.4.1 PPO
  - 3.4.2 DPO
  - 3.4.3 GRPO
  - 3.4.4 R1的解读
- 3.5 MoE+VLLM原理解析
  - 3.5.1 MoE机制解析
  - 3.5.2 VLLM原理解析

## 四、 数据处理和模型微调
- 研究基础设施
  - 硬件
  - [LLAMA FACTORY](https://github.com/BrenchCC/LLaMA-Factory/tree/qwen2-r1-distill-training) ～ SFT
  - [Opencompass](https://github.com/BrenchCC/opencompass_graduation) ～ Evaluation
  - [Mergekit](https://github.com/arcee-ai/mergekit) ～ MOE
  - 自行开发的R1 Trainer ———> Qwen R1 GRPO [R1-GRPO-Qwen2.5-RL](https://github.com/BrenchCC/R1-GRPO-Qwen2.5-RL)
  - [EasyR1](https://github.com/hiyouga/EasyR1) VERL ————> R1-Distlled-Qwen GRPO 再训练
  - [VLLM](https://github.com/vllm-project/vllm) 开源推理框架
- 数据格式清洗和预处理
- 评测指标介绍
- 第一阶段 以思维链数据和一些知识类数据进行SFT———>一版思维链强化型模型，一版知识强化型模型
  - [Brench/MMLU-Pro-CoT-Train-43K](https://huggingface.co/datasets/Brench/MMLU-Pro-CoT-Train-43K)
  - [AI-MO/NuminaMath-CoT](https://huggingface.co/datasets/AI-MO/NuminaMath-CoT)
  - 通过gsm8k、mmlu、humaneval进行知识、数学、代码能力的基准评测
  - 得到2-3版模型和结果对比
- 第二阶段 通过R1蒸馏高质量的思维链数据做微调以及R1-Zero线路的复刻
  - [Brench/Numina-Math-R1-COT-172K](https://huggingface.co/datasets/Brench/Numina-Math-R1-COT-172K) 详细可见[MY Huggingface Home](https://huggingface.co/Brench)
  - Qwen base model 1.5B,3B GRPO training （NuminaMath、Omni-Math、RUC-AIBOX/STILL-3-Preview-RL-Data）
  - R1-Distilled-Model 的 GRPO强化学习训练提升性能
  - 得到2-3版模型
 
## 五、实验结果分析
- 第一阶段
  - 测评结果 
- 第二阶段
  - loss+kl+completion长度变化

## 六、Dify应用模版的搭建演示
- [Dify](https://github.com/BrenchCC/dify_graduation)

## 七、总结

## 八、参考文献

## 九、致谢
