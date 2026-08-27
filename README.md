# 🛡️ TOKEN GRABBER | Tim$erz

**A powerful, open-source tool for educational and security research purposes that demonstrates how Discord tokens are stored locally and how they can be extracted for security awareness.**

![Version](https://img.shields.io/badge/version-2.1.0-blue)
![Python](https://img.shields.io/badge/python-3.8+-green)
![License](https://img.shields.io/badge/license-MIT-red)
![Status](https://img.shields.io/badge/status-stable-brightgreen)
![Platform](https://img.shields.io/badge/platform-Windows%20%7C%20Linux%20%7C%20macOS-lightgrey)

---

## ⚠️ DISCLAIMER - READ THIS FIRST

> **🚨 IMPORTANT: This tool is provided SOLELY FOR EDUCATIONAL AND RESEARCH PURPOSES.**
> **IT EXTRACTS DISCORD TOKENS AND RETRIEVES USER DATA VIA DISCORD API.**

> **⛔ YOU ARE NOT ALLOWED TO:**
> - ❌ Use this tool for malicious purposes
> - ❌ Use this tool without explicit consent from all parties involved
> - ❌ Violate Discord's Terms of Service
> - ❌ Share, sell, or distribute collected data
> - ❌ Target individuals without their knowledge
> - ❌ Use this for harassment, doxxing, or illegal activity
> - ❌ Deploy on systems you do not own or lack authorization to test

> **✅ YOU ARE ALLOWED TO:**
> - ✔️ Use this in controlled, consensual security testing environments
> - ✔️ Educate others about token security and privacy risks
> - ✔️ Test your own systems and networks
> - ✔️ Report security vulnerabilities responsibly
> - ✔️ Learn how Discord stores authentication tokens
> - ✔️ Understand how token-based authentication works
> - ✔️ Conduct authorized penetration testing with written consent

> **👨‍⚖️ The author is NOT responsible for any misuse or damage caused by this tool.**
>
> *By downloading, installing, or using this tool, you agree to take FULL responsibility for your actions.*

---

## 📖 What is This?

**Token Grabber** is a Python-based utility that extracts Discord tokens from local storage databases and retrieves associated user information via the Discord API.

### 🔍 How It Works

| # | Step | Description |
|---|------|-------------|
| 1️⃣ | **Scan for tokens** | Scans Local Storage and LevelDB files on the target system |
| 2️⃣ | **Extract tokens** | Uses regex patterns to find JWT-format tokens |
| 3️⃣ | **Validate tokens** | Validates token structure and decodes base64 tokens |
| 4️⃣ | **Query Discord API** | Queries Discord API for user information using each token |
| 5️⃣ | **Collect data** | User info, friends, guilds, DMs, billing, connections |
| 6️⃣ | **Send webhook** | Sends all data to Discord via webhook |
| 7️⃣ | **Save to file** | Saves data to tokens.json file |

### 🎯 What Data Is Collected

| Category | Data |
|----------|------|
| 👤 **User Info** | ID, Username, Discriminator, Email, Phone, Nitro Status |
| 👥 **Friends** | All friends with usernames and IDs |
| 🏠 **Servers** | Server names, IDs, member counts, permissions |
| 💬 **DMs** | Recent direct message channels |
| 💳 **Billing** | Subscription information (Nitro, etc.) |
| 🔗 **Connected Accounts** | Linked accounts (Twitch, YouTube, Spotify, etc.) |

### 🎯 Why This Matters

Discord uses tokens as authentication credentials. These tokens are stored locally on the user's machine. Understanding how they are stored and what information they can access is important for:
- 🔒 Security awareness and education
- 🛡️ Protecting against credential theft
- 🧠 Understanding authentication mechanisms
- 🔐 Improving personal security practices

---

## ⚡ Features

| 🏷️ Feature | 📝 Description |
|------------|----------------|
| 🔍 **Token Extraction** | Scans LevelDB for Discord tokens |
| 🌐 **Multi-Platform** | Supports Windows, Linux, and MacOS |
| 🔑 **Multi-Client** | Discord, Canary, PTB, Development |
| 🌐 **Browser Support** | Chrome, Brave, Edge (LevelDB scan) |
| 🔐 **Token Validation** | Validates JWT structure and decodes base64 |
| 📊 **Discord API Client** | Retrieves user data via Discord API |
| 👥 **Friends List** | Extracts all friends from account |
| 🏠 **Guilds/Servers** | Lists all servers the user is in |
| 💬 **Direct Messages** | Gets recent DM channels |
| 💳 **Billing Info** | Checks for Nitro subscriptions |
| 🔗 **Connected Accounts** | Linked third-party accounts |
| ⚡ **Multi-Threading** | Fast concurrent token processing |
| 📨 **Webhook Support** | Discord webhook integration |
| 💾 **JSON Output** | Saves data to tokens.json |
| 🛡️ **Error Handling** | Graceful failure handling |

---

## 🔧 Installation

### 📋 What You Need Before Starting

| ✅ Item | ℹ️ Description |
|---------|----------------|
| 🐍 Python 3.8+ | Installed on your computer |
| 🎮 Discord Account | A server/channel you control |
| 🔗 Discord Webhook URL | Created from your Discord server settings |
| 🖥️ Command Line | Basic knowledge of terminal/command prompt |
| 📦 pip | Python package manager |

### 📥 Step 1: Get the Code

Open your terminal/command prompt and run:

```bash
git clone https://github.com/your-repo/token-grabber.git
cd token-grabber
