
# BPB-Worker-Panel-Auto-update

自动同步 BPB-Worker-Panel 项目的最新稳定发行版 worker.js 文件。

## 🚀 快速开始（适合 Fork）

1. 点击右上角 Fork 本仓库到你的 GitHub 账号。
2. 打开你的仓库，进入 Actions 页面，点击 Enable workflows（启用 GitHub Actions）。
3. 无需其他配置，GitHub 默认的 GITHUB_TOKEN 权限即可推送更新。
4. 你可以手动点击 Run workflow，也可以等待每天定时自动检查。

> 注意：确保你的仓库默认分支为 main，否则推送时可能失败。

🌟 如果觉得这个项目对你有帮助，欢迎顺手点个 Star 支持一下！

---

## 功能介绍

- 每天自动检查 bia-pain-bache/BPB-Worker-Panel 仓库的最新 Release
- 自动下载最新版本的 worker.js
- 重命名为 _worker.js
- 同步更新本地 version.txt
- 自动提交并推送到本仓库

## 工作流程

GitHub Actions 会每日 00:00（UTC 时间）自动运行：

1. 获取上游仓库的最新 Release 版本号
2. 比较本地 version.txt 的记录
3. 若版本不同，则自动下载并替换 _worker.js
4. 更新 version.txt
5. 自动提交并推送到主分支（main）

> 若版本一致，则不执行任何操作。

---

## 📂 目录结构

/
├── _worker.js         
├── version.txt        
├── LICENSE            
├── .gitignore         
├── README.md          
└── .github/
    └── workflows/
        └── update_worker.yml

---

## ⚙️ 配置说明

- 无需手动设置 Token：默认使用 GitHub 提供的 GITHUB_TOKEN 进行权限认证。
- 如需修改同步源：编辑 .github/workflows/update_worker.yml，修改源仓库地址即可。

---

## 📜 开源协议

本项目使用 MIT License 开源。

您可以自由地使用、复制、修改和分发本项目，前提是附带原始许可证声明。

---

## 📢 特别说明

- 本仓库同步的内容来源于 [BPB-Worker-Panel](https://github.com/bia-pain-bache/BPB-Worker-Panel)。
- 原项目版权归原作者所有，本项目仅用于自动同步更新，不对原内容进行修改。

---
