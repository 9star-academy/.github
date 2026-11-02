<div align="center">

<h1>9star Academy · 九星学院</h1>

<p><strong>知行合一，代码先于雄辩。</strong></p>

<p>
  以开源项目为起点，持续探索基础设施、全栈应用、AI 与系统原理。<br>
  从解决一个实际问题开始，让想法逐步落地。
</p>

<p>
  <a href="https://9staracademy.vercel.app/"><strong>访问官网 ↗</strong></a> ·
  <a href="#开源项目">开源项目</a> ·
  <a href="#一起把工具做得更好">参与贡献</a>
</p>

</div>

---

## 开源项目

目前从基础设施与运维开始，围绕 Linux 环境和日常维护构建实用工具。

| 项目 | 实现语言 | 定位与核心能力 | 文档 |
| :--- | :--- | :--- | :--- |
| [**ShellReady**](https://github.com/9star-academy/ShellReady) | Bash / Shell | **Linux 环境初始化。**<br>配置 BBR、Zsh、trzsz-go、Starship、Atuin、zoxide 等组件，提供按需安装、状态检查与卸载。 | [文档 ↗](https://github.com/9star-academy/ShellReady#readme) |
| [**secctl**](https://github.com/9star-academy/secctl) | Go | **Linux 安全管理。**<br>端口审计、SSH 加固与超时回滚、防火墙规则管理，以及 Docker IPv4 bridge 防护。 | [文档 ↗](https://github.com/9star-academy/secctl#readme) |
| [**servctl**](https://github.com/9star-academy/servctl) | Go | **systemd 服务托管。**<br>为已有程序生成服务配置，支持开机自启、异常退出自动重启、启停管理与日志查看。 | [文档 ↗](https://github.com/9star-academy/servctl#readme) |
| [**proxctl**](https://github.com/9star-academy/proxctl) | Go | **应用对外发布。**<br>反向代理、静态站点托管、自动 HTTPS、WebSocket 透传及规则热重载。 | [文档 ↗](https://github.com/9star-academy/proxctl#readme) |
| [**bakctl**](https://github.com/9star-academy/bakctl) | Go | **文件与数据库备份。**<br>支持 SQLite、PostgreSQL、本地及 S3/R2 存储、可选加密、恢复与 Linux systemd 定时任务。 | [文档 ↗](https://github.com/9star-academy/bakctl#readme) |

> 语言按工具主体实现标注；ShellReady 的 Python 代码主要用于自动化测试。支持环境、运行依赖与版本信息见各项目文档。

---

## 🚀 裸机服务器标准交付流 (Workflow)

从一台新开辟的空白 VPS 到生产可用，只需这套流水线：

```text
 ┌────────────────┐      ┌────────────────┐      ┌────────────────┐
 │ 1. ShellReady  │ ───► │   2. secctl    │ ───► │   3. servctl   │
 └────────────────┘      └────────────────┘      └────────────────┘
   终端环境一键初始化      SSH 加固与防火墙防泄露   将程序托管为 Systemd 服务
                                                         │
                                                         ▼
                         ┌────────────────┐      ┌────────────────┐
                         │   5. bakctl    │ ◄─── │   4. proxctl   │
                         └────────────────┘      └────────────────┘
                           定时加密备份至 R2/S3    反向代理与自动 HTTPS 证书
```

---

## 持续探索的方向

| 方向 | 关注领域 | 当前进展 |
| :--- | :--- | :--- |
| 基础设施与运维 | Linux · 部署 · 备份 · 安全 | 已有项目 |
| 全栈应用开发 | Web · Go · Flutter · 原生应用 | 规划中 |
| AI 与智能体 | 模型应用 · 知识检索 · MCP · Agent | 规划中 |
| 计算机基础与系统研究 | 操作系统 · 网络 · 存储 · 分布式 | 规划中 |

> 规划中的方向将在项目启动后补充代码与文档，当前进展以各仓库为准。

---

## 一起把工具做得更好

欢迎在对应项目提交 Issue，反馈问题或提出需求；也欢迎通过 Pull Request 改进代码、补充文档和分享使用经验。

---

<div align="center">

<sub>Maintained by <a href="https://github.com/reedtang666">@reedtang666</a> · <a href="https://9staracademy.vercel.app/">9star Academy</a></sub>

</div>
