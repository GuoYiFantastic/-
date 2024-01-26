![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/b8e78179-7b05-45ab-b8ac-a54f3ce9c7da)# Finetune 简介
LLM 的下游应用中，增量预训练和指令跟随是经常会用到两种的微调模式
- 增量预训练微调
使用场景:让基座模型学习到一些新知识，如某个垂类领域的常识

训练数据:文章、书籍、代码等
- 指令跟随微调
使用场景:让模型学会对话模板，根据人类指令进行对话

训练数据:高质量的对话、问答数据
![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/22522314-70d2-4c82-9b75-9667c76a7345)
![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/ef8896ce-c7fa-48b1-9409-039f742cc62b)

### 指令跟随微调
指令跟随微调是为了得到能够实际对话的 LLM介绍指令跟随微调前，需要先了解如何使用LLM 进行对话

在实际对话时，通常会有三种角色

- System    给定一些上下文信息，比如“你是一个安全的 A1助手”
- User      实际用户，会提出一些问题，比如“世界第一高峰是?”
- Assistant 根据 User 的输入，结合 System 的上下文信息，做出回答，比如“珠穆朗玛峰”

在使用对话模型时，通常是不会感知到这三种角色的
![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/606f0071-1740-43f6-af9b-617f927cad95)

![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/d9b54c09-c396-4925-9f8c-0579604c7c44)

### 增量预训练微调
![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/fb67a310-6b77-4481-b255-db01c11ff8b1)

![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/c377b26a-c4ef-42f8-9b42-499783ea0e9b)

# XTuner 介绍

# 8GB 显卡玩转 LLM
![image](https://github.com/GuoYiFantastic/InternLM_training_camp/assets/130634988/716a94e7-d64a-4302-ab66-b4911c6bf77c)

# 动手实战环节
见作业。
