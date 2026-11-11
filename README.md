# 特教课堂辅助平台

帮助教师进行学生档案管理、备课、课堂教学与记录、课后报告和教学知识浏览。

## Windows 快速启动

首次使用需要安装 Node.js 24、pnpm 10.28.2、uv 和 Docker Desktop，并启动 Docker Desktop：

1. 安装 [Node.js 24](https://nodejs.org/)、[uv](https://docs.astral.sh/uv/getting-started/installation/) 和 [Docker Desktop](https://docs.docker.com/desktop/)。
2. 在 PowerShell 执行 `npm install -g pnpm@10.28.2`，安装完成后重新打开终端。
3. 双击项目根目录的 **首次安装.cmd**。脚本安装依赖、准备本地数据库并创建演示账号。
4. 在浏览器访问 http://127.0.0.1:5173/，演示账号为 `teacher`，密码为 `classroom-demo`。

以后先启动 Docker Desktop，再双击 **启动平台.cmd**。使用时保持启动窗口打开；按 Ctrl+C 可停止平台。数据库和上传资料保存在本机，更新代码前请自行备份。

## AgentArts 配置

首次安装会根据 `.env.example` 创建本机 `.env` 并生成会话密钥。若需使用云端 Agent，请在本机 `.env` 中填写 `AGENTARTS_INVOKE_URL` 和 `AGENTARTS_API_KEY`，然后重启平台；不要将 `.env` 或密钥提交到仓库。

## 主要目录

- `frontend/`：Vue 页面、课堂交互和知识图谱。
- `backend/`：业务 API、数据库、报告与课件管理。
- `agent-service/`：智能服务适配与统计。
- `contracts/`：共享数据结构、接口定义及演示初始化所需数据。
- `infra/`、`scripts/`：数据库与启动脚本。

PPT/PPTX 静态预览需要本机安装 LibreOffice 或 Microsoft PowerPoint；也可上传 PDF。
