# Discord Token Grabber

A high-performance Discord token extraction tool that retrieves authentication tokens from Discord client storage and browser local storage, then sends comprehensive user data to a configured Discord webhook endpoint.

## Features

- Extracts tokens from Discord, Discord Canary, Discord PTB, and Discord Development installations
- Cross-platform support: Windows, Linux, and macOS
- Browser token extraction (Chrome, Brave, Microsoft Edge)
- Concurrent multi-threaded token extraction for optimal performance
- Validates token authenticity using Discord API v10
- Retrieves complete user profile data including:
  - User ID, username, discriminator
  - Email and phone number (if available)
  - Nitro subscription status
  - Friends list
  - Server (guild) membership
  - Direct message channels
  - Connected external accounts (Spotify, Steam, etc.)
  - Billing information (subscription status)
- Sends detailed Discord embeds via webhook
- Exports all data to JSON file for archival purposes

## Requirements

- Python 3.8 or higher (type hints require 3.8+)
- Operating System: Windows 7+, macOS 10.12+, or any Linux distribution

## Installation

1. Clone or download this repository

2. Install required Python packages:
```bash
pip install -r requirements.txt
