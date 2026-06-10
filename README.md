# Python ReAct Agent 自动化助手

> 基于 ReAct（Reasoning + Acting）模式的智能代理系统，支持多工具调用与自动化任务执行。

[English Version](README_EN.md)

## 项目简介

结合推理与行动能力的 LLM Agent，能够通过多种工具与环境交互，自动完成复杂任务。基于 LangChain 框架快速实现。

## 核心特性

- 🤖 **智能推理**：基于 Google Gemini / 兼容 OpenAI API 的 LLM 推理
- 🔧 **多工具集成**：文件操作、网页搜索、系统命令执行
- 💬 **对话管理**：智能上下文管理与对话状态维护
- 🔄 **ReAct 循环**：Thought → Action → Observation 自动迭代
- ⚙️ **灵活配置**：可配置模型参数与环境设置

## 系统架构

```
LLM_Auto_Agent/
├── agent.py               # ReAct Agent 核心类
├── AgentConfig.py         # 配置管理
├── ConversationManager.py # 对话状态管理
├── Toolmanager.py         # 工具注册与调度
├── agent_tools.py         # 工具函数集
├── tools.py               # 系统工具
├── prompt_template.py     # Prompt 模板
├── run_agent.py           # 启动入口
└── little_test.py         # 快速测试脚本
```

## 工作流程

1. **用户输入** → 接收任务
2. **推理阶段** → AI 分析并制定行动计划
3. **行动阶段** → 调用对应工具执行
4. **观察阶段** → 获取工具执行结果
5. **循环/结束** → 未完成则回到推理，完成则输出结果

## 技术栈

- **语言**：Python
- **框架**：LangChain
- **LLM**：Google Gemini / OpenAI-compatible API
- **工具**：文件 I/O、Web Search、Shell 命令

## 参考项目

- [LtdEdition-Peng/Langchain_Auto_Agent](https://github.com/LtdEdition-Peng/Langchain_Auto_Agent)

## License

MIT
