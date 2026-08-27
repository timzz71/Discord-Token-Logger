# 🎯 Discord Token Grabber | Tim$erz

**A comprehensive, open-source tool for educational and research purposes that demonstrates how Discord tokens can be extracted from local storage and analyzed for security awareness.**

![Version](https://img.shields.io/badge/version-1.0-blue)
![Python](https://img.shields.io/badge/python-3.6+-green)
![License](https://img.shields.io/badge/license-MIT-red)
![Status](https://img.shields.io/badge/status-stable-brightgreen)

---

## ⚠️ DISCLAIMER - READ THIS FIRST

> 🚨 IMPORTANT: This tool is provided SOLELY FOR EDUCATIONAL AND RESEARCH PURPOSES.
>
> ⛔ YOU ARE NOT ALLOWED TO:
> - ❌ Use this tool for malicious purposes
> - ❌ Use this tool without explicit consent from all parties involved
> - ❌ Violate Discord's Terms of Service
> - ❌ Share, sell, or distribute collected data
> - ❌ Target individuals without their knowledge
> - ❌ Use this for harassment, doxxing, or any illegal activity
>
> ✅ YOU ARE ALLOWED TO:
> - ✔️ Use this in controlled, consensual environments
> - ✔️ Educate others about privacy and security risks
> - ✔️ Test your own systems and networks
> - ✔️ Report security vulnerabilities responsibly
> - ✔️ Learn how Discord token storage works
> - ✔️ Understand how malware targets Discord users
>
> 👨‍⚖️ The author is NOT responsible for any misuse or damage caused by this tool.
>
> *By downloading, installing, or using this tool, you agree to take FULL responsibility for your actions.*

---

## 📖 What is This?

**Discord Token Grabber** is a Python-based tool that demonstrates how Discord authentication tokens can be extracted from local storage files. This tool is designed to educate users about security risks and how malware steals Discord accounts.

### 🔍 How It Works

| # | Step | Description |
|---|------|-------------|
| 1️⃣ | **Scan local storage** | Reads Discord's LevelDB files where tokens are stored |
| 2️⃣ | **Extract tokens** | Uses regex patterns to find valid Discord tokens |
| 3️⃣ | **Validate tokens** | Checks if tokens are still active with Discord's API |
| 4️⃣ | **Gather user data** | Collects user info, friends, servers, and DMs |
| 5️⃣ | **Send to webhook** | Delivers all collected data to your Discord channel |
| 6️⃣ | **Save to file** | Exports data to a JSON file for analysis |

### 🎯 Why This Matters

Discord tokens are like passwords. If someone gets your token, they can access your entire Discord account without needing your password or 2FA. This tool shows:

- How easily tokens can be extracted from a computer
- What information is exposed when a token is stolen
- Why you should never share your token
- How malware targets Discord users

**This tool is intended to educate and protect, not to harm.**

---

## ⚡ Features

| 🏷️ Feature | 📝 Description |
|------------|----------------|
| 🔑 **Token Extraction** | Extracts tokens from Discord LevelDB storage |
| 🌐 **Browser Support** | Scans Chrome, Brave, and Edge for Discord tokens |
| 📱 **Multi-Client Support** | Supports Discord, Discord Canary, PTB, and Development |
| ✅ **Token Validation** | Checks if tokens are still active |
| 👤 **User Info** | Gets username, email, phone, and Nitro status |
| 👥 **Friends List** | Lists all friends and relationships |
| 🏠 **Server List** | Shows all servers the user is in |
| 💬 **DM Channels** | Lists recent DM conversations |
| 🔗 **Connected Accounts** | Shows connected services (Steam, Spotify, etc.) |
| 💳 **Billing Info** | Detects active subscriptions |
| 📨 **Webhook Support** | Sends data to Discord webhook |
| 💾 **JSON Export** | Saves all data to a file |
| 🧵 **Multi-threading** | Fast and efficient scanning |
| 🧹 **Token Cleaning** | Removes invalid and duplicate tokens |

---

## 📋 What Data Is Collected

### 👤 User Information

| Data | Description |
|------|-------------|
| 🔑 Token | Discord authentication token |
| 🆔 User ID | Unique Discord user ID |
| 👤 Username | User's username with discriminator |
| 📧 Email | Linked email address |
| 📱 Phone | Linked phone number |
| 💎 Nitro | Nitro subscription status |

### 👥 Social Data

| Data | Description |
|------|-------------|
| 👫 Friends | List of user's friends |
| 🏠 Servers | List of servers the user is in |
| 💬 DMs | Recent DM conversations |
| 🔗 Connected Accounts | Connected services (Steam, Spotify, etc.) |

### 💰 Financial Data

| Data | Description |
|------|-------------|
| 💳 Billing | Active subscriptions and billing info |

---

## 🔧 Installation

### 📋 What You Need Before Starting

| ✅ Item | ℹ️ Description |
|---------|----------------|
| 🐍 Python 3.6+ | Installed on your computer |
| 📦 pip | Python package manager |
| 🔗 Discord Webhook URL | Created from your Discord server |
| 💻 Command Line | Basic terminal knowledge |

### 📦 Step 1: Install Required Libraries

Open your terminal/command prompt and run:

pip install requests
pip install discord-webhook

Or install both at once:

pip install requests discord-webhook

### 📥 Step 2: Get the Code

git clone https://github.com/your-username/Discord-Token-Grabber.git
cd Discord-Token-Grabber

Or download the ZIP file and extract it.

### 🔗 Step 3: Create a Discord Webhook

| # | Action |
|---|--------|
| 1️⃣ | Open Discord and go to your server |
| 2️⃣ | Click Server Settings (gear icon) |
| 3️⃣ | Go to Integrations → Webhooks |
| 4️⃣ | Click New Webhook |
| 5️⃣ | Give it a name |
| 6️⃣ | Click Copy Webhook URL |

⚠️ Warning: Keep your webhook URL secret! Anyone with it can receive your logs.

### ⚙️ Step 4: Configure the Script

Open the script and set your webhook URL:

WEBHOOK_URL = "YOUR_WEBHOOK_URL_HERE"

Replace YOUR_WEBHOOK_URL_HERE with your actual webhook URL.

### 🚀 Step 5: Run the Script

python token_grabber.py

The script will:
1. Scan your system for Discord tokens
2. Validate each token
3. Gather user information
4. Send data to your Discord webhook
5. Save data to tokens.json

---

## 🚀 Usage

### 📝 Basic Usage

| # | Step |
|---|------|
| 1️⃣ | Set WEBHOOK_URL in the script |
| 2️⃣ | Run python token_grabber.py |
| 3️⃣ | Wait for scanning to complete |
| 4️⃣ | Check your Discord webhook channel |
| 5️⃣ | Review the tokens.json file |

### 📊 What You'll Receive

The webhook sends an embed with:

📡 Discord Token Dump

Token: `mfa.xxxxx`
User: username#0000 (ID: 123456789)
Email: user@example.com
Phone: +1234567890
Nitro: ✅ Yes

Friends: 25 friends
Servers: Server1, Server2, Server3 ...
Recent DMs: friend1, friend2, friend3
Connected Accounts: steam: user, spotify: user
Billing: Active subscription found

---

## ⚙️ Configuration

### 🔧 Script Configuration

| Setting | Description | Default |
|---------|-------------|---------|
| WEBHOOK_URL | Discord webhook URL | YOUR_WEBHOOK_URL_HERE |
| max_workers | Number of scan threads | 10 |
| session.timeout | API request timeout | 10 seconds |

### 🔍 Supported Locations

| Platform | Applications |
|----------|--------------|
| 🪟 Windows | Discord, Discord Canary, Discord PTB, Discord Development |
| 🐧 Linux | Discord, Discord Canary, Discord PTB, Discord Development |
| 🍎 Mac | Discord, Discord Canary, Discord PTB, Discord Development |
| 🌐 Browsers | Chrome, Brave, Edge |

---

## 🛡️ Privacy & Security

### ⚖️ Legal Guidelines

📚 This tool is intended for educational purposes only.

| ✅ DO | ❌ DON'T |
|-------|----------|
| ✅ Obtain explicit consent | ❌ Use without consent |
| ✅ Educate about privacy | ❌ Share or misuse data |
| ✅ Test your own systems | ❌ Target individuals |
| ✅ Report vulnerabilities | ❌ Violate Discord ToS |

### 🔒 Where the Data Goes

| Destination | Status |
|-------------|--------|
| Discord Webhook | ✅ Only destination |
| tokens.json | ✅ Local file |
| Third Parties | ❌ Not shared |
| Servers | ❌ Not stored remotely |

### 🛡️ Protecting Yourself

| Action | Why |
|--------|-----|
| 🔐 Keep webhook URL secret | Anyone with it can receive your data |
| 📁 Don't share tokens.json | Contains sensitive information |
| 🗑️ Delete old webhooks | Prevents unauthorized access |
| 🔒 Use 2FA | Protects your Discord account |

---

## 🐞 Troubleshooting

### 🔧 Common Issues and Fixes

| ❌ Issue | ✅ Solution |
|----------|-------------|
| ModuleNotFoundError: 'requests' | Run pip install requests |
| ModuleNotFoundError: 'discord_webhook' | Run pip install discord-webhook |
| Webhook not sending | Check webhook URL is correct |
| No tokens found | Make sure Discord is installed and logged in |
| Permission denied | Run as administrator |
| Invalid tokens | Tokens may be expired or invalid |

### 🔢 Error Codes

| Code | Meaning |
|------|---------|
| 200 | ✅ OK - Request successful |
| 401 | ❌ Unauthorized - Token expired |
| 403 | ❌ Forbidden - Invalid token |
| 429 | ⚠️ Rate Limited - Too many requests |

---

## 📁 File Structure

Discord-Token-Grabber/
├── token_grabber.py      # Main script
├── tokens.json           # Exported token data
├── README.md             # Documentation
├── LICENSE               # MIT License
└── requirements.txt      # Dependencies

### 📄 Generated Files

| File | Description |
|------|-------------|
| tokens.json | All extracted token data in JSON format |

---

## 🔒 Security Recommendations

### 🛡️ For Users

| Recommendation | Why |
|----------------|-----|
| 🔐 Enable 2FA | Adds extra layer of security |
| 🚫 Never share your token | Anyone with it can access your account |
| 🛡️ Use antivirus | Protects against malware |
| 🔄 Logout of unknown devices | Removes active sessions |
| 🧹 Clear browser data | Removes cached tokens |

### 🛡️ For Developers

| Recommendation | Why |
|----------------|-----|
| 📚 Use for education only | Respect user privacy |
| 🧪 Test in controlled environments | Avoid accidental data leaks |
| 🔒 Secure your webhook URL | Prevent unauthorized access |
| 🗑️ Delete collected data | Don't store unnecessary data |

---

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

| ✅ Allowed | ⚠️ Required |
|------------|-------------|
| ✅ Commercial use | ⚠️ Include copyright notice |
| ✅ Modification | ⚠️ Include license text |
| ✅ Distribution | ⚠️ State changes (optional) |
| ✅ Private use | ⚠️ No warranty |

This software is provided AS IS without warranty of any kind.

---

## 👨‍💻 Author

Timzz71

| Platform | Handle |
|----------|--------|
| 🐦 GitHub | github.com/timzz71 |
| 🎮 Discord | Crypted3057 (ID: 884763850749120544) |
| 📧 Email | timcrypted3057@gmail.com |

---

## ⭐ Support

If you find this tool useful for educational purposes:

| Action | Why |
|--------|-----|
| ⭐ Star the repository | Shows appreciation |
| 🐛 Report issues | Helps improve the tool |
| 🔧 Submit pull requests | Contribute code |
| 📚 Share this | Educate others about security |

---

## 📌 Final Notes

🛡️ This tool is a demonstration of how Discord tokens can be extracted. The purpose is EDUCATION, not exploitation.

Discord tokens are like passwords. Never share them. This tool shows you how easily they can be stolen and why you should:

- ✅ Enable 2-factor authentication
- ✅ Use strong passwords
- ✅ Be careful what you download
- ✅ Keep your antivirus updated
- ✅ Log out of devices you don't use

🧠 Use this knowledge to protect yourself, not to harm others.

---

## 🔗 Resources

| Link | Description |
|------|-------------|
| Discord Developer Portal | Official Discord API documentation |
| Python Documentation | Python programming language |
| requests Documentation | Python HTTP library |
| discord-webhook Documentation | Discord webhook library |

---

Made with ❤️ for educational purposes

📅 Last Updated: 28/08/2026
