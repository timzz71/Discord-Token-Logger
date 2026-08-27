████████████████████████████████████████████████████████████████████████████████
█                                                                              █
█     🛡️ TOKEN GRABBER - PYTHON SCRIPT - COMPLETE DOCUMENTATION              █
█                                                                              █
█                           📦 VERSION 2.1.0 - 2026                           █
█                                                                              █
█              🔬 EDUCATIONAL & SECURITY RESEARCH PURPOSE ONLY                █
█                                                                              █
█              ⚡ SUPPORTS: WINDOWS | LINUX | MACOS                           █
█                                                                              █
████████████████████████████████████████████████████████████████████████████████

═══════════════════════════════════════════════════════════════════════════════════

📌 1.0 ⚠️ DISCLAIMER - READ FIRST
═══════════════════════════════════════════════════════════════════════════════════

🚨 IMPORTANT: This tool is provided SOLELY FOR EDUCATIONAL AND RESEARCH PURPOSES.
    IT EXTRACTS DISCORD TOKENS AND RETRIEVES USER DATA VIA DISCORD API.

⛔ YOU ARE NOT ALLOWED TO:
  ❌ Use this tool for malicious purposes
  ❌ Use this tool without explicit consent from all parties involved
  ❌ Violate Discord's Terms of Service
  ❌ Share, sell, or distribute collected data
  ❌ Target individuals without their knowledge
  ❌ Use this for harassment, doxxing, or illegal activity
  ❌ Deploy on systems you do not own or lack authorization to test

✅ YOU ARE ALLOWED TO:
  ✔️ Use this in controlled, consensual security testing environments
  ✔️ Educate others about token security and privacy risks
  ✔️ Test your own systems and networks
  ✔️ Report security vulnerabilities responsibly
  ✔️ Learn how Discord stores authentication tokens
  ✔️ Understand how token-based authentication works
  ✔️ Conduct authorized penetration testing with written consent

👨‍⚖️ The author is NOT responsible for any misuse or damage caused by this tool.
By using this tool, you agree to take FULL responsibility for your actions.

═══════════════════════════════════════════════════════════════════════════════════

📖 2.0 WHAT IS THIS?
═══════════════════════════════════════════════════════════════════════════════════

Token Grabber is a Python-based utility that extracts Discord tokens from local
storage databases and retrieves associated user information via the Discord API.

🔍 2.1 HOW IT WORKS
───────────────────────────────────────────────────────────────────────────────────

┌───┬──────────────────────────────────────────────────────────────────────────┐
│ # │ STEP                                                                     │
├───┼──────────────────────────────────────────────────────────────────────────┤
│ 1 │ 🔍 Scans Local Storage and LevelDB files on the target system            │
│ 2 │ 🔑 Extracts tokens using regex patterns (JWT format)                     │
│ 3 │ ✅ Validates token structure and decodes base64 tokens                   │
│ 4 │ 🌐 Queries Discord API for user information using each token             │
│ 5 │ 📊 Collects: user info, friends, guilds, DMs, billing, connections      │
│ 6 │ 📨 Sends all data to Discord via webhook                                 │
│ 7 │ 💾 Saves data to tokens.json file                                       │
└───┴──────────────────────────────────────────────────────────────────────────┘

🎯 2.2 WHAT DATA IS COLLECTED
───────────────────────────────────────────────────────────────────────────────────

  👤 User Information: ID, Username, Discriminator, Email, Phone, Nitro Status
  👥 Friends List: All friends with usernames and IDs
  🏠 Servers/Guilds: Server names, IDs, member counts, permissions
  💬 DMs: Recent direct message channels
  💳 Billing: Subscription information (Nitro, etc.)
  🔗 Connected Accounts: Linked accounts (Twitch, YouTube, Spotify, etc.)
  📊 Token Info: OAuth2 token details (scopes, expiry, etc.)

═══════════════════════════════════════════════════════════════════════════════════

⚡ 3.0 FEATURES
═══════════════════════════════════════════════════════════════════════════════════

┌────────────────────────┬───────────────────────────────────────────────────────┐
│ 🏷️ FEATURE             │ 📝 DESCRIPTION                                      │
├────────────────────────┼───────────────────────────────────────────────────────┤
│ 🔍 Token Extraction    │ Scans LevelDB for Discord tokens                     │
│ 🌐 Multi-Platform      │ Supports Windows, Linux, and MacOS                  │
│ 🔑 Multi-Client        │ Discord, Canary, PTB, Development                   │
│ 🌐 Browser Support     │ Chrome, Brave, Edge (LevelDB scan)                  │
│ 🔐 Token Validation    │ Validates JWT structure and decodes base64          │
│ 📊 Discord API Client  │ Retrieves user data via Discord API                 │
│ 👥 Friends List        │ Extracts all friends from account                   │
│ 🏠 Guilds/Servers      │ Lists all servers the user is in                    │
│ 💬 Direct Messages     │ Gets recent DM channels                             │
│ 💳 Billing Info        │ Checks for Nitro subscriptions                      │
│ 🔗 Connected Accounts  │ Linked third-party accounts                         │
│ ⚡ Multi-Threading     │ Fast concurrent token processing                    │
│ 📨 Webhook Support     │ Discord webhook integration                         │
│ 💾 JSON Output         │ Saves data to tokens.json                           │
│ 🛡️ Error Handling     │ Graceful failure handling                           │
└────────────────────────┴───────────────────────────────────────────────────────┘

═══════════════════════════════════════════════════════════════════════════════════

✅ 4.0 ALLOWED USE CASES
═══════════════════════════════════════════════════════════════════════════════════

  ✅ Authorized penetration testing with explicit written consent from the
     system owner

  ✅ Educational research in accredited cybersecurity classrooms and
     training environments

  ✅ Personal security audits performed on machines you legally own

  ✅ Bug bounty hunting activities where token exposure is explicitly
     included in the scope of testing

  ✅ Forensic analysis of compromised systems with proper authorization

  ✅ Internal security team assessments within corporate environments

  ✅ Understanding token storage mechanisms for defensive purposes

═══════════════════════════════════════════════════════════════════════════════════

❌ 5.0 DISALLOWED / ILLEGAL USE CASES
═══════════════════════════════════════════════════════════════════════════════════

  ❌ Stealing Discord accounts without explicit permission from the account
     holder

  ❌ Unauthorized access to any third-party systems, networks, or services

  ❌ Distribution, resale, or commercial exploitation of harvested tokens

  ❌ Any use that violates Discord's Terms of Service or Community Guidelines

  ❌ Use in jurisdictions where such tools are classified as illegal under
     local computer crime laws

  ❌ Using this script to harass, impersonate, or defraud any individual or
     entity

  ❌ Deployment on systems you do not own or lack written authorization to test

═══════════════════════════════════════════════════════════════════════════════════

🧰 6.0 REQUIREMENTS
═══════════════════════════════════════════════════════════════════════════════════

6.A) SYSTEM REQUIREMENTS
───────────────────────────────────────────────────────────────────────────────────

  ● 🪟 Windows 10/11 (64-bit recommended)
  ● 🐧 Linux (Ubuntu/Debian recommended)
  ● 🍎 macOS 10.15+
  ● 🐍 Python 3.8 or higher
  ● 📂 Read access to configuration directories:
    - Windows: %APPDATA% and %LOCALAPPDATA%
    - Linux: $HOME/.config/
    - Mac: $HOME/Library/Application Support/
  ● 💾 Minimum 10 MB free disk space
  ● 🌐 Internet connection for Discord API calls and webhook

6.B) PYTHON DEPENDENCIES
───────────────────────────────────────────────────────────────────────────────────

  Run the following command to install all required packages:

  📦 pip install requests discord-webhook

  Individual package versions (tested):
    ● requests          - 2.31.0+
    ● discord-webhook   - 1.3.0+

═══════════════════════════════════════════════════════════════════════════════════

🚀 7.0 INSTALLATION
═══════════════════════════════════════════════════════════════════════════════════

7.A) STEP 1: GET THE CODE
───────────────────────────────────────────────────────────────────────────────────

  Open terminal/command prompt and run:

  💻 git clone https://github.com/your-repo/token-grabber.git
  💻 cd token-grabber

  If Git is not installed, download the ZIP file from GitHub and extract it.

7.B) STEP 2: INSTALL DEPENDENCIES
───────────────────────────────────────────────────────────────────────────────────

  💻 pip install -r requirements.txt

  Or manually:
  💻 pip install requests discord-webhook

7.C) STEP 3: CONFIGURE WEBHOOK
───────────────────────────────────────────────────────────────────────────────────

  Open the script in a text editor and set:

  🔗 WEBHOOK_URL = "YOUR_WEBHOOK_URL_HERE"

  Replace with your actual Discord webhook URL.

  How to create a webhook:
    1. Open Discord and go to your server/channel
    2. Click Server Settings → Integrations → Webhooks
    3. Click "New Webhook" → Name it → Copy URL

  ⚠️ Keep your webhook URL secret! Anyone with it can receive your logs.

7.D) STEP 4: RUN THE SCRIPT
───────────────────────────────────────────────────────────────────────────────────

  💻 python token_grabber.py

  The script will:
    1. 🔍 Scan for tokens in all Discord clients and browsers
    2. 🌐 Query Discord API for user data
    3. 📨 Send data via webhook
    4. 💾 Save data to tokens.json

═══════════════════════════════════════════════════════════════════════════════════

📁 8.0 OUTPUT FORMAT
═══════════════════════════════════════════════════════════════════════════════════

8.A) CONSOLE OUTPUT
───────────────────────────────────────────────────────────────────────────────────

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

8.B) WEBHOOK OUTPUT (Discord Embed)
───────────────────────────────────────────────────────────────────────────────────

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

8.C) JSON OUTPUT (tokens.json)
───────────────────────────────────────────────────────────────────────────────────

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

═══════════════════════════════════════════════════════════════════════════════════

🧪 9.0 TESTED PLATFORMS
═══════════════════════════════════════════════════════════════════════════════════

  ┌───────────────┬──────────┬────────────────────────────────────────────────────┐
  │ 🖥️ PLATFORM   │ 📊 STATUS │ 📝 NOTES                                          │
  ├───────────────┼──────────┼────────────────────────────────────────────────────┤
  │ Windows 11    │ ✅ FULL  │ All features functional                           │
  │ Windows 10    │ ✅ FULL  │ All features functional                           │
  │ Windows 8.1   │ ⚠️ PART  │ Some paths may differ                             │
  │ Windows 7     │ ⚠️ PART  │ Limited functionality                             │
  │ Ubuntu 20.04+ │ ✅ FULL  │ All features functional                           │
  │ Fedora 35+    │ ✅ FULL  │ All features functional                           │
  │ macOS 10.15+  │ ✅ FULL  │ All features functional                           │
  └───────────────┴──────────┴────────────────────────────────────────────────────┘

═══════════════════════════════════════════════════════════════════════════════════

🛠️ 10.0 TECHNICAL DETAILS
═══════════════════════════════════════════════════════════════════════════════════

10.A) TOKEN PATTERNS
───────────────────────────────────────────────────────────────────────────────────

  The script uses the following regex patterns to detect Discord tokens:

  Pattern 1: [\w-]{24}\.[\w-]{6}\.[\w-]{27}     (Standard JWT token)
  Pattern 2: mfa\.[\w-]{84}                      (MFA token)
  Pattern 3: [\w-]{24}\.[\w-]{6}\.[\w-]{38}     (Extended JWT token)

10.B) TOKEN VALIDATION
───────────────────────────────────────────────────────────────────────────────────

  Tokens are validated by:
    1. Checking the number of parts (3 or 4)
    2. Verifying the header contains valid base64url characters
    3. Attempting base64 decode of the token

10.C) DISCORD API ENDPOINTS
───────────────────────────────────────────────────────────────────────────────────

  GET /api/v10/users/@me                    - User information
  GET /api/v10/users/@me/relationships      - Friends list
  GET /api/v10/users/@me/guilds             - Servers list
  GET /api/v10/users/@me/channels           - DM channels
  GET /api/v10/users/@me/billing/subscriptions - Billing info
  GET /api/v10/users/@me/connections        - Connected accounts
  GET /api/v10/oauth2/@me                   - Token information

10.D) STORAGE PATHS
───────────────────────────────────────────────────────────────────────────────────

  Discord Clients:
    Windows: %APPDATA%\Discord\Local Storage\leveldb
    Linux:   $HOME/.config/discord/Local Storage/leveldb
    Mac:     $HOME/Library/Application Support/discord/Local Storage/leveldb

  Browsers:
    Chrome:  %LOCALAPPDATA%\Google\Chrome\User Data\Default\Local Storage\leveldb
    Brave:   %LOCALAPPDATA%\BraveSoftware\Brave-Browser\User Data\Default\Local Storage\leveldb
    Edge:    %LOCALAPPDATA%\Microsoft\Edge\User Data\Default\Local Storage\leveldb

═══════════════════════════════════════════════════════════════════════════════════

🔒 11.0 SECURITY NOTICE
═══════════════════════════════════════════════════════════════════════════════════

  ╔══════════════════════════════════════════════════════════════════════════════╗
  ║  ⚠️  WARNING: This script accesses sensitive user data stored on disk      ║
  ║     and retrieves personal information via the Discord API.                 ║
  ║                                                                             ║
  ║     ONLY run on systems you own OR have explicit written permission to      ║
  ║     test. Unauthorized use is illegal and unethical.                        ║
  ║                                                                             ║
  ║     The author assumes NO liability for misuse of this tool.                ║
  ║     Users are solely responsible for compliance with all applicable laws.   ║
  ╚══════════════════════════════════════════════════════════════════════════════╝

11.A) DATA HANDLING
───────────────────────────────────────────────────────────────────────────────────

  ● 🔑 Tokens are temporarily stored in memory
  ● 📨 Tokens and user data are sent via HTTPS to your webhook
  ● 💾 Data is saved locally to tokens.json in plaintext
  ● 🗑️ Delete tokens.json and logs immediately after analysis
  ● 🔒 Consider encrypting the output file for sensitive environments

11.B) PRIVACY CONSIDERATIONS
───────────────────────────────────────────────────────────────────────────────────

  This script can retrieve:
    ● 📧 Email addresses
    ● 📱 Phone numbers
    ● 👥 Full friends list
    ● 🏠 Server memberships
    ● 💳 Billing information
    ● 🔗 Connected third-party accounts

  ⚠️ This information is highly sensitive. Handle with extreme care.

═══════════════════════════════════════════════════════════════════════════════════

🐞 12.0 TROUBLESHOOTING
═══════════════════════════════════════════════════════════════════════════════════

12.A) COMMON ISSUES AND FIXES
───────────────────────────────────────────────────────────────────────────────────

  ┌────────────────────────────────────────────────────────────────────────────┐
  │ ❌ ISSUE                          │ ✅ SOLUTION                            │
  ├───────────────────────────────────┼────────────────────────────────────────┤
  │ ModuleNotFoundError: 'requests'   │ 💻 pip install requests               │
  │ ModuleNotFoundError: 'discord_webhook' │ 💻 pip install discord-webhook  │
  │ "Access denied" error             │ 🔑 Run as Administrator (Windows)     │
  │                                     │    or with sudo (Linux/Mac)         │
  │ No tokens found                   │ 🔍 Ensure Discord is logged in        │
  │ Webhook not sending               │ 🔗 Check WEBHOOK_URL is correct       │
  │ Invalid token error               │ 🔑 Token may be expired/invalid       │
  │ Script crashes on start           │ 🐍 Verify Python 3.8+ and deps       │
  │ LevelDB files not found           │ 📁 Check Discord is installed        │
  └───────────────────────────────────┴────────────────────────────────────────┘

12.B) ERROR CODES
───────────────────────────────────────────────────────────────────────────────────

  200    ✅ OK - API request successful
  401    🔑 Unauthorized - Invalid/expired token
  403    🚫 Forbidden - Insufficient permissions
  404    📂 Not Found - Endpoint or resource not found
  429    ⏳ Rate Limited - Too many API requests
  500    ❌ Internal Server Error - Discord API error

═══════════════════════════════════════════════════════════════════════════════════

📜 13.0 LICENSE
═══════════════════════════════════════════════════════════════════════════════════

  MIT License

  Copyright (c) 2026 palofsc (palo)

  Permission is hereby granted, free of charge, to any person obtaining a copy
  of this software and associated documentation files (the "Software"), to deal
  in the Software without restriction, including without limitation the rights
  to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
  copies of the Software, and to permit persons to whom the Software is
  furnished to do so, subject to the following conditions:

  The above copyright notice and this permission notice shall be included in all
  copies or substantial portions of the Software.

  THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
  AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
  LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
  OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
  SOFTWARE.

  ─── COMMERCIAL USE ───
  Commercial use requires separate written authorization from the author.
  Contact: palofsc@proton.me

═══════════════════════════════════════════════════════════════════════════════════

👨‍💻 14.0 AUTHOR & CONTACT
═══════════════════════════════════════════════════════════════════════════════════

  NAME:        palofsc (palo)
  ROLE:        Security Researcher & Tool Developer
  EMAIL:       palofsc@proton.me
  GITHUB:      https://github.com/palofsc
  DISCORD:     palofsc#0001

═══════════════════════════════════════════════════════════════════════════════════

⭐ 15.0 DISCLAIMER
═══════════════════════════════════════════════════════════════════════════════════

  THIS TOOL IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
  IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
  FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT.

  IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM,
  DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR
  OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE
  USE OR OTHER DEALINGS IN THE SOFTWARE.

  The developer is not responsible for any consequences arising from:
    ● Unauthorized use of this tool
    ● Misuse by third parties
    ● Legal action resulting from illegal activities
    ● Data loss or system damage
    ● Account bans or suspensions

  By using this software, you agree that you have read, understood, and
  accepted this disclaimer.

═══════════════════════════════════════════════════════════════════════════════════

📊 16.0 VERSION HISTORY
═══════════════════════════════════════════════════════════════════════════════════

  v2.1.0 (2026-08-28)
    ● ➕ Added multi-platform support (Windows, Linux, Mac)
    ● 🌐 Added browser support (Chrome, Brave, Edge)
    ● 👥 Added friends list extraction
    ● 🔗 Added connected accounts extraction
    ● 💳 Added billing/subscription check
    ● ⚡ Improved multi-threading performance

  v2.0.0 (2026-08-15)
    ● 🔄 Complete rewrite with Discord API integration
    ● 📨 Added webhook notification with embeds
    ● 📊 Added JSON output with full user data
    ● 🔧 Improved error handling

  v1.0.0 (2026-07-01)
    ● 🎉 Initial release
    ● 🔍 Basic token extraction from Discord

═══════════════════════════════════════════════════════════════════════════════════

🔧 17.0 REFERENCES
═══════════════════════════════════════════════════════════════════════════════════

  ● 📚 Discord API Documentation: https://discord.com/developers/docs
  ● 🔐 Discord API Reference: https://discord.com/developers/docs/reference
  ● 🌐 OAuth2 Documentation: https://discord.com/developers/docs/topics/oauth2
  ● 🛡️ OWASP Testing Guide: https://owasp.org/www-project-web-security-testing-guide/
  ● 🔑 JWT Documentation: https://jwt.io/introduction
  ● 📦 discord-webhook: https://pypi.org/project/discord-webhook/
  ● 📦 requests: https://pypi.org/project/requests/

═══════════════════════════════════════════════════════════════════════════════════

                    ██████  ███████ ███████ ████████ ███████
                    ██   ██ ██      ██         ██    ██
                    ██████  █████   ███████    ██    █████
                    ██   ██ ██           ██    ██    ██
                    ██   ██ ███████ ███████    ██    ███████

                    ════════════════════════════════════════
                    🔒 USE RESPONSIBLY. CODE ETHICALLY. 🔒
                    ════════════════════════════════════════

═══════════════════════════════════════════════════════════════════════════════════

📅 FINAL NOTES
═══════════════════════════════════════════════════════════════════════════════════

This tool is a demonstration of how Discord tokens are stored and retrieved
from local systems, and what information can be accessed once a token is obtained.

Token security is critical for account protection. Understanding how tokens
work helps both security professionals and everyday users protect themselves
from credential theft.

Key takeaways:
  🔑 Never share your tokens with anyone
  🔒 Discord tokens are equivalent to passwords
  📡 Tokens can expose all account data
  🛡️ Always use 2FA to protect your account
  🧠 Use this knowledge to improve security awareness

⚠️ REMINDER: This tool is for EDUCATIONAL PURPOSES ONLY.
    Unauthorized use is illegal and strictly prohibited.

───────────────────────────────────────────────────────────────────────────────────
Made With ❤️ For Educational & Security Research Purposes
Last Updated: 28/08/2026
───────────────────────────────────────────────────────────────────────────────────

Made By Vrex489 - Survival Directive Active
