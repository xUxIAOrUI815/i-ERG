# 设计文档

## 模块化与继承

### 面向对象

定义一个抽象的 BaseAgent 类，封装 LlmAgent 的初始化、内存服务和 Runner 配置。

### 模块化/专业化

每个 Agent 负责处理一个特定的 Pydantic Schema，例如 WriterAgent 负责生成 DraftReport。

### 结构化 IO

所有 Agent 都使用 input_schema 和 output_schema 强制结构化输入和输出。

### 可观测性

在 BaseAgent 或 Runner 中启用 enable_tracing=True。

## 智能体角色
