<p align="right">
  <a href="./README.md">English</a> | <a href="./README_ko.md">한국어</a>
</p>

<div align="center">

# 🦀 ColabClaw

### Your Personal AI Automation Workspace on Google Colab

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?style=for-the-badge&logo=googlecolab&logoColor=white)](https://colab.research.google.com)
[![OpenClaw](https://img.shields.io/badge/OpenClaw-FF6B6B?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI+PHBhdGggZD0iTTEyIDJMMyAxNGgxOEwxMiAyeiIgZmlsbD0id2hpdGUiLz48L3N2Zz4=&logoColor=white)](https://github.com/openclaw/openclaw)
[![Telegram](https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white)](https://telegram.org)
[![Gmail](https://img.shields.io/badge/Gmail-D14836?style=for-the-badge&logo=gmail&logoColor=white)](https://mail.google.com)
[![GitHub](https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com)
[![Maton](https://img.shields.io/badge/Maton-6C63FF?style=for-the-badge&logoColor=white)](https://www.maton.ai)

<br/>

### *"The fastest, easiest way to learn OpenClaw — with a practical email assistant use case!"*

[🚀 Quick Start](#-quick-start) · [📋 Features](#-features) · [🔄 Workflow](#-workflow-overview) · [🛠 Setup](#-full-setup-guide) · [🇰🇷 한국어](./README_ko.md)

<br/>

[![Stars](https://img.shields.io/github/stars/tykimos/colabclaw?style=social)](https://github.com/tykimos/colabclaw/stargazers)
[![Forks](https://img.shields.io/github/forks/tykimos/colabclaw?style=social)](https://github.com/tykimos/colabclaw/network/members)
[![Watchers](https://img.shields.io/github/watchers/tykimos/colabclaw?style=social)](https://github.com/tykimos/colabclaw/watchers)
[![Last Commit](https://img.shields.io/github/last-commit/tykimos/colabclaw)](https://github.com/tykimos/colabclaw/commits/main)

</div>

---

## Why ColabClaw?

Installation issues on OpenClaw's GitHub never stop. Here are real examples:

- **All install methods fail on a clean macOS** — Node v14 PATH shadows newly installed v22, npm throws EACCES permission errors ([#21464](https://github.com/openclaw/openclaw/issues/21464))
- **npm install bricks Raspberry Pi devices** — `@discordjs/opus` lacks ARM64 prebuilds, causing native module build failure ([#23861](https://github.com/openclaw/openclaw/issues/23861))
- **sharp dependency build fails on Apple Silicon** — `node-gyp` unavailable, source build attempt errors out ([#4592](https://github.com/openclaw/openclaw/issues/4592))
- **Can't even update** — `node-llama-cpp` fails to install cmake, leaving users stuck without security patches ([#32025](https://github.com/openclaw/openclaw/issues/32025))

While teaching and learning OpenClaw, we've seen **too many people give up at the installation step**. The tool itself is great, but Node.js version conflicts, native module build failures, and OS-specific compatibility issues block people before they even start.

So we thought — **what if you could run it directly on Google Colab?**

Of course, Colab resets when the session ends, so it's not suitable for always-on production use. But for the **learning phase**, you can experience OpenClaw's core features right away without any installation hassle. No more giving up out of setup fatigue — you can even build a practical email assistant use case hands-on. That's ColabClaw.

---

## 📋 Features

| Feature | Description | Service |
|---------|-------------|---------|
| 🖥️ **Colab Terminal** | Launch a full terminal inside Google Colab | Google Colab |
| 🤖 **OpenClaw Engine** | Install and run OpenClaw as your automation core | OpenClaw |
| 💬 **Chat Interface** | Talk to OpenClaw through Telegram | Telegram |
| 📧 **Email Automation** | Read Gmail, summarize, and draft replies automatically | Gmail + Maton |
| 📁 **GitHub Workspace** | Use a repository as your structured task surface | GitHub |
| 🔄 **Scheduled Refresh** | Periodically collect and update information | Cron / OpenClaw |

---

## 🔄 Workflow Overview

```mermaid
flowchart LR
    A[Google Colab] --> B[OpenClaw]
    B --> C[Telegram]
    B --> D[Gmail via Maton]
    B --> E[GitHub Repo]

    D --> F[Read Emails]
    F --> G[Generate Draft Reply]
    G --> H{Human Approval}
    H -->|Approved| I[Send Reply]
    H -->|Edit| G

    E --> J[Track Tasks]
    E --> K[Periodic Updates]
```

---

## 🛠 Full Setup Guide

```mermaid
timeline
    title ColabClaw Setup Journey
    section Environment
        Open Colab : Start a fresh notebook
        Launch Terminal : Install colab-xterm
        Install OpenClaw : curl + onboard
    section Connections
        Telegram : Chat interface setup
        GitHub : Create workspace repo
        Maton : Connect Gmail safely
    section Automation
        Email Reading : Summarize incoming mail
        Draft Generation : Auto-create reply drafts
        Scheduled Refresh : Periodic info updates
```
---

## 🚀 Quick Start

### Step 0: Prepare Required Accounts

Set up the following services before configuring the full workflow:

```mermaid
flowchart TD
    subgraph Required["Accounts to Prepare"]
        T[Telegram<br/>Chat with OpenClaw]
        GH[GitHub<br/>Workspace & Tracking]
        GM[Gmail<br/>Email Reading & Drafts]
        M[Maton<br/>Gmail Integration]
    end

    T --> OC[OpenClaw]
    GH --> OC
    GM --> M
    M --> OC
```

| Service | Purpose | Link |
|---------|---------|------|
| **Telegram** | Communicate with OpenClaw | [telegram.org](https://telegram.org) |
| **GitHub** | Repository-based workflow & tracking | [github.com](https://github.com) |
| **Gmail** | Read emails & generate draft replies | [mail.google.com](https://mail.google.com) |
| **Maton** | Secure Gmail connection | [maton.ai](https://www.maton.ai) |

### Step 1: Open Google Colab

Start a fresh [Google Colab notebook](https://colab.research.google.com).

### Step 2: Launch Terminal

Click the terminal section at the bottom of the page.

<img width="1582" height="1036" alt="image" src="https://github.com/user-attachments/assets/a9f8fbac-0dad-44a8-8b8d-5e01e64371ad" />

### Step 3: Install OpenClaw

```bash
curl -fsSL https://openclaw.ai/install.sh | bash
```

<img width="1582" height="1036" alt="image" src="https://github.com/user-attachments/assets/55a9b3d3-e28f-4b57-b91e-371d61039aa5" />

Once installation is complete, you'll be prompted with a series of questions. Follow the example below:

◇  I understand this is personal-by-default and shared/multi-user use requires lock-down. Continue?
│  Yes
◇  Setup mode
│  QuickStart
◇  Model/auth provider
│  OpenAI
◇  OpenAI auth method
│  OpenAI Codex (ChatGPT OAuth)
◇  Paste the authorization code (or full redirect URL):
│  http://localhost:1455/auth/callback?code=oaistb_ac_1SZn995Ut-nebUP1hVMc&scope=openid+profile+email+offline_access&state=653d71043b52
◇  Default model
│  Keep current (openai-codex/gpt-5.4)
◇  Select channel (QuickStart)
│  Telegram (Bot API)
◇  How do you want to provide this Telegram bot token?
│  Enter Telegram bot token
◇  Search provider
│  DuckDuckGo Search (experimental)
◇  OpenAI auth method
│  OpenAI Codex (ChatGPT OAuth)
◇  Configure skills now? (recommended)
│  Yes
◇  Enable hooks?
│  Skip for now

Once setup is complete, run OpenClaw with:

```bash
openclaw gateway run --verbose
```
---

### Telegram Integration

Send `/start` to your bot in Telegram. You'll receive a message like:

OpenClaw: access not configured.
Your Telegram user id: 6XXX169904
Pairing code: T72W8XXX
Ask the bot owner to approve with:
openclaw pairing approve telegram T72W8XXX

Go back to the terminal, stop the running instance with Ctrl+C, then run:

```bash
openclaw pairing approve telegram T72W8XXX
```

Once pairing is confirmed, restart OpenClaw:

```bash
openclaw gateway run --verbose
```

Then say hello through Telegram — it will ask how you'd like to be called and how it should introduce itself. Answer as you prefer.

### 📁 GitHub as Your Workspace

Use a GitHub repository to store and manage:

```
📂 your-workspace-repo/
├── 📝 notes/              # Personal notes & memos
├── 📊 collected-info/     # Gathered information
├── 📋 workflows/          # Automation scripts
├── 📈 reports/            # Periodic summaries
└── 🔄 updates/            # Scheduled refresh results
```

### 📧 Email Automation Pipeline

The email workflow follows a **human-in-the-loop** design:

```mermaid
flowchart TD
    A[New Email Arrives] --> B[OpenClaw Reads Email]
    B --> C[Classify Importance]
    C -->|Important| D[Generate Summary]
    C -->|Low Priority| E[Archive]
    D --> F[Create Draft Reply]
    F --> G[Human Reviews Draft]
    G -->|Approve| H[Send]
    G -->|Edit| F
    G -->|Discard| I[Delete Draft]
```

> 💡 **Key Principle:** Draft generation is automated. Actual sending requires human approval.

To connect email via Gmail + Maton, tell OpenClaw you'd like to set up email integration, then get a Maton API Key from the Maton page and run the following in your terminal. If OpenClaw is already running, stop it first, run the command, then restart.

```bash
export MATON_API_KEY='XXXXXXX'
```

### 🔄 Periodic Refresh

Schedule recurring tasks to keep your workspace updated:

- 📊 Repository status checks
- 📋 Scheduled report summaries
- 📧 Email-related update monitoring
- 🔁 Recurring task result collection
- 📡 Lightweight monitoring outputs

---

## 🔗 Related Links

| Resource | Link |
|----------|------|
| 🤖 OpenClaw | [github.com/openclaw/openclaw](https://github.com/openclaw/openclaw) |
| 📖 OpenClaw Docs | [docs.openclaw.ai](https://docs.openclaw.ai) |
| 🔗 Maton | [maton.ai](https://www.maton.ai) |
| 💬 Telegram | [telegram.org](https://telegram.org) |
| 📁 GitHub | [github.com](https://github.com) |
| 📧 Gmail | [mail.google.com](https://mail.google.com) |

---

## ⭐ Star History

[![Star History Chart](https://api.star-history.com/svg?repos=tykimos/colabclaw&type=Date)](https://star-history.com/#tykimos/colabclaw&Date)

---

## 🤝 Contributing

Contributions are welcome! Feel free to:

- ⭐ Star this repository
- 🐛 Open an [Issue](https://github.com/tykimos/colabclaw/issues)
- 🔀 Submit a [Pull Request](https://github.com/tykimos/colabclaw/pulls)

---

## 📊 Activity

[![Last Commit](https://img.shields.io/github/last-commit/tykimos/colabclaw?label=Last%20Commit)](https://github.com/tykimos/colabclaw/commits/main)
[![Issues](https://img.shields.io/github/issues/tykimos/colabclaw)](https://github.com/tykimos/colabclaw/issues)
[![PRs](https://img.shields.io/github/issues-pr/tykimos/colabclaw)](https://github.com/tykimos/colabclaw/pulls)
[![Repo Size](https://img.shields.io/github/repo-size/tykimos/colabclaw)](https://github.com/tykimos/colabclaw)

---

## 📜 License

This project is licensed under the MIT License.

[![MIT License](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)

---

<div align="center">

**Made with ❤️ for the AI automation community**

[![Visitors](https://api.visitorbadge.io/api/visitors?path=tykimos%2Fcolabclaw&label=Visitors&countColor=%23263759)](https://visitorbadge.io/status?path=tykimos%2Fcolabclaw)

</div>
