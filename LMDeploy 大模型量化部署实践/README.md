# 1.大模型部署背景
通过一系列复杂算法，寻找llm在空间、时间之间的最优平衡。

# 2.LMDeploy 简介
LMDeploy 是由 [MMRazor](https://github.com/open-mmlab/mmrazor) 和 [MMDeploy](https://github.com/open-mmlab/mmdeploy) 团队开发的一个用于压缩、部署和提供大型语言模型（LLM）服务的工具包。它具有以下核心特性：

- **高效推理**：LMDeploy 通过引入持久批处理（又称连续批处理）、阻塞式 KV 缓存、动态分割与合并、张量并行性、高性能 CUDA 核心等关键特性，比 vLLM 的请求吞吐量高出多达 1.8 倍。

- **有效量化**：LMDeploy 支持仅权重和 k/v 量化，且 4 位推理性能比 FP16 高 2.4 倍。量化质量已通过 OpenCompass 评估确认。

- **轻松的分布式服务器**：利用请求分发服务，LMDeploy 便于在多台机器和多个卡上高效部署多模型服务。

- **交互式推理模式**：通过在多轮对话过程中缓存注意力的 k/v，引擎记住了对话历史，从而避免了对历史会话的重复处理。

# 3.动手实践环节
[Click Here](https://github.com/GuoYiFantastic/InternLM_training_camp/blob/main/LMDeploy%20%E5%A4%A7%E6%A8%A1%E5%9E%8B%E9%87%8F%E5%8C%96%E9%83%A8%E7%BD%B2%E5%AE%9E%E8%B7%B5/%E4%BD%9C%E4%B8%9A.md)
