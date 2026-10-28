<div align="center">

# 🌟 9star-academy

### Minimalist, Zero-Config CLI Suite for Linux Bare-Metal & Indie Developers
**专为独立开发者与全栈工程师打造的「裸机轻量运维工具集」**

<p>
  <img src="https://img.shields.io/badge/Language-Go%20%7C%20Python%20%7C%20Shell-00ADD8?style=flat-square&logo=go" alt="Language">
  <img src="https://img.shields.io/badge/Philosophy-Zero--Config%20%7C%20Single--Binary-success?style=flat-square" alt="Philosophy">
  <img src="https://img.shields.io/badge/License-MIT-blue?style=flat-square" alt="License">
</p>

<p align="center">
  拒绝重型面板（如宝塔 / 1Panel）对系统的深度侵入，把服务器的极致控制权与性能交还给开发者。<br>
  每款工具皆为<b>「单二进制 / 一行命令 / 零外部依赖」</b>，专注解决从开荒到上线的某一个核心痛点。
</p>

</div>

---

### 🚀 裸机服务器标准交付流 (Workflow)

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

### 📦 运维工具矩阵 (Toolchain)

| 工具 | 状态 / 语言 | 核心定位与解决痛点 | 快速体验 |
| :--- | :--- | :--- | :--- |
| [**ShellReady**](https://github.com/9star-academy/ShellReady) | `Python / Shell` | **一条命令配好新机器**<br>开箱集成 BBR、trzsz 拖拽传文件、Starship 极客提示符、Atuin 智能历史、zoxide | `curl -sSL ... \| bash` |
| [**secctl**](https://github.com/9star-academy/secctl) | `Go (In Progress)` | **裸机安全加固与防失联**<br>支持 GitHub 公钥防失联注入、修改端口、语义化防火墙，一键修复 Docker 绕过 UFW 端口漏洞 | `secctl audit` |
| [**servctl**](https://github.com/9star-academy/servctl) | `Go (Production)` | **免写 Unit 文件的守护神器**<br>一行命令将任意裸机可执行程序注册为标准 `systemd` 系统自启服务并接管日志 | `servctl add myapp` |
| [**proxctl**](https://github.com/9star-academy/proxctl) | `Go (In Progress)` | **极简反向代理与自动证书**<br>一行命令将本地端口映射到公网域名，内置 ACME 自动申请/续期免费 SSL 证书与静态站点托管 | `proxctl bind api.com 8080` |
| [**bakctl**](https://github.com/9star-academy/bakctl) | `Go (In Progress)` | **定时加密备份至云存储**<br>一行命令通过 Systemd Timer 将 SQLite/PG 及目录自动压缩加密同步至 R2/S3/OSS/WebDAV | `bakctl add db --to r2` |

---

### 💡 核心设计哲学 (Design Philosophy)

1. **One-liner First（极简直觉）**：任何复杂配置必须能被一条直观的人类语言命令搞定。
2. **Zero Bloatware（拒绝臃肿）**：不长期常驻无关多余内存，不篡改系统基础包管理器，全部采用单静态二进制分发。
3. **Embrace System Native（拥抱系统原生）**：绝不自己造劣质轮子，底层深度集成 Linux 内核级机制（`systemd`、`systemd-timer`、`iptables/nftables`、`ACME`）。
4. **Idiot-Proof & Safe（防呆与防失联）**：核心配置变更（如 SSH/防火墙/热备）内置自动校验和倒计时自动回滚机制，绝不锁死服务器。

---

<div align="center">

<sub>Maintained with ❤️ by <a href="https://github.com/reedtang666">@reedtang666</a> and the <b>9star-academy</b> community.</sub>

</div>
