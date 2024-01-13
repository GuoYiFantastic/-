# 基于 InternLM 和 LangChain 搭建你的知识库

# 大模型开发范式

### LLM 的局限性
- 知识时效性受限:如何让LLM能够获取最新的知识
- 专业能力有限:如何打造垂域大模型
- 定制化成本高: 如何打造个人专属的LLM应用

### 范式一：RAG
- 低成本
- 可实时更新
- 受基座模型影响大
- 单次回答知识有限

![1705148836102](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/1a9237d4-3bff-4de5-9894-1ffabc3f9724)


### 范式二：Finetune
- 可个性化微调
- 知识覆盖面厂
- 成本高昂
- 无法实时更新

# LangChain 简介
![1705149124017](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/fe375f75-57da-409b-8a33-6160687ed37c)


# 构建向量数据库
**加载源文件> 文档分块 > 文档向量化**

- 确定源文件类型，针对不同类型源文件选用不同的加载器
- - 核心在于将带格式文本转化为无格式字符串
- 由于单个文档往往超过模型上下文上限，我们需要对加载的文档进行切分
-- 一般按字符串长度进行分
-- 可以手动控制分割块的长度和重鲁区间长度
- 使用向量数据库来支持语义检索，需要将文档向量化存入向量数据库
- - 可以使用任一一种 Embedding 模型来进行向量化
- - 可以使用多种支持语义检索的向量数据库，一般使用轻量级的 Chroma

# 搭建知识库助手

### 将 InternLM 接入 LangChain
LangChain 支持自定义LLM，可以直接接入到框架中我们只需将 InternLM 部署在本地，并封装一个自定义 LLM类，调用本地 InternLM 即可

### 构建检索问答链
- LangChain 提供了检索问答链模版，可以自动实现知识检索、Prompt 嵌入、LLM问答的全部流程
- 将基于 InternLM 的自定义 LLM 和已构建的向量数据库接入到检索问答链的上游
- 调用检索问答链，即可实现知识库助手的核心功能

![1705156064354](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/1316b2df-ae92-457c-a2b3-1f8889ac0cb6)


# Web Demo 部署

# 动手实战环节
