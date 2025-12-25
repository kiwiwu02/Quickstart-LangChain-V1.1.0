# LangChain Essentials（Python）学习笔记

此代码仓库收录了我根据 LangChain Academy《LangChain Essentials》课程整理的练习与笔记。每个 Notebook 都围绕构建 LangChain LLM 应用的关键主题展开，从基础 Agent 配置、工具调用到中间件与人类介入流程。
![alt text](./assets/image.png)
## 文件概览

- `01.Fast_Agent.ipynb` – 从零搭建 SQL Agent：创建数据库上下文、定义工具并观察 ReAct 流程。
- `02.Messages.ipynb` – 演示 BaseMessage 类型与多轮提示设计，覆盖 system、human、ai 消息。
- `03.Streaming.ipynb` – 展示模型流式输出、增量 UI 更新与对 token 流的处理方式。
- `04.tools.ipynb` – 编写并注册工具，演练 LangChain 工具调用链条与错误处理。
- `05.tools_with_mcp.ipynb` – 将 MCP 服务器纳入工具体系，体验跨进程调用。
- `06.memory.ipynb` – 讲解会话记忆的配置、清理与状态序列化。
- `07.StructuredOutput.ipynb` – 使用 Pydantic 构建结构化响应与类型校验。
- `08.middleware.ipynb` – 在链路中插入中间件以实现日志、监控与防护逻辑。
- `09.humanInTheLoop.ipynb` – 演示 HITL：中断、人工审批与反馈回写。
- `LangChain V1 Essentials-Python.pdf` – 官方课件原件，供对照课程内容与幻灯片。
- `env_utils.py` – 环境与依赖检查脚本。
- `requirements.txt` 与 `pyproject.toml` – Notebook 共享依赖清单。

## 快速上手

1. **创建 Python 环境**
   ```bash
   cd code
   python3 -m venv .venv
   source .venv/bin/activate
   pip install -r requirements.txt
   ```
   如果希望以可编辑模式安装，也可以结合 `pyproject.toml` 运行 `pip install -e .`。

2. **配置环境变量**
   - 复制 `.env` 或自行创建，并填写 `DASHSCOPE_API_KEY` 等必要密钥。
   - 运行 `env_utils.doublecheck_env(".env")` 可在执行 Notebook 前快速检查缺失项。

3. **运行 Notebook**
   - 启动 Jupyter 或 VS Code，打开任一 Notebook。
   - 先执行每个 Notebook 顶部的设置单元，再继续后续示例。

## 提示

- 示例默认通过 DashScope API 访问 Qwen 模型，如需替换，请调整模型配置。
- 若示例涉及 SQLite 示例库 Chinook（[Chinook.db](./Chinook.db)），请确认文件位于当前工作目录。
- Notebook 结构与课程同步，但内容与注释反映了我的理解与实验记录。

## 参考链接

- 原始课程资料：[LangChain Academy – LangChain Essentials (Python)](https://academy.langchain.com/courses/take/langchain-essentials-python)
- 学习笔记参考：[LangChain 官方教程总结（博客）](https://zxj-2023.github.io/2025/12/02/%E5%AD%A6%E4%B9%A0/ai%E6%A1%86%E6%9E%B6/langchain%E5%AE%98%E6%96%B9%E6%95%99%E7%A8%8B/)
- 官方课件：`LangChain V1 Essentials-Python.pdf`（随仓库提供）
