# Beep Boop Discord Bot
 
## Overview

**Boop** is a multifunctional Discord bot developed using Python and the Discord API. The bot provides entertainment, automation, moderation assistance, welcome interactions, and voice channel music playback features for Discord servers.

The bot is designed to improve server engagement by responding to user interactions, welcoming new members with customized messages and images, and supporting music streaming through voice channels. 

---

## Features

### 1. Welcome System

Boop automatically welcomes new members when they join a Discord server.

#### Features:

* Randomized welcome messages
* Welcome images and GIFs 
* User avatar customization
* Rounded profile image generation using PIL

Examples:

* *"Welcome, user. We hope you brought pizza."*
* *"Challenger approaching!"*

---

### 2. Interactive Chat Features

Boop responds to text-based interactions.

#### Supported Commands

* Greeting response
* Knock-knock joke interaction
* Random conversational replies

Examples:

```text
hello boop
```

```text
knock knock
```

---

### 3. Slash Commands Support

The bot supports Discord slash commands using `discord.app_commands`.

Available commands:

| Command        | Description                       |
| -------------- | --------------------------------- |
| `/say`         | Makes the bot send a message      |
| `/join_voice`  | Connect bot to voice channel      |
| `/leave_voice` | Disconnect bot from voice channel |
| `/hop_to`      | Move bot to another voice channel |
| `/play_song`   | Play music from YouTube           |
| `/pause_song`  | Pause current song                |
| `/resume`      | Resume paused song                |
| `/stop`        | Stop playing music                |

---

### 4. Music Playback System

Boop supports music playback in Discord voice channels.

#### Features

* YouTube audio playback
* Voice channel connection
* Pause, resume, and stop support
* Audio streaming using FFmpeg
* YouTube extraction using `yt-dlp`

---

### 5. Image Processing

The bot modifies user profile pictures for welcome messages using the Python Imaging Library (PIL).

#### Capabilities

* Rounded avatar generation
* Transparent corner rendering
* Dynamic image customization

---

## Technology Stack

### Programming Language

* Python

### Libraries Used

* discord.py
* yt-dlp
* Pillow (PIL)
* python-dotenv
* asyncio
* termcolor

### APIs

* Discord API

---

## Project Structure

```text
boop-discord-bot/
│
├── bot.py
├── .env
├── guilds.txt
├── requirements.txt
├── README.md
│
├── img/
│   ├── pizza.png
│   ├── weapons.png
│   ├── banana.png
│   ├── spawn.gif
│   ├── vs.png
│   └── disappointed.png
│
└── avatar.png
```

---

## Installation Guide

### Prerequisites

Install:

* Python 3.10+
* Discord Bot Token
* FFmpeg installed

---

### Step 1: Clone Repository

```bash
git clone https://github.com/yourusername/boop-discord-bot.git
cd boop-discord-bot
```

---

### Step 2: Install Dependencies

```bash
pip install -r requirements.txt
```

---

### Step 3: Create `.env` File

Create a `.env` file in root directory:

```env
DISCORD_TOKEN=your_discord_bot_token
```

---

### Step 4: Install FFmpeg

Download and install FFmpeg.

Add FFmpeg path in code:

```python
discord.FFmpegPCMAudio(
    executable="path_to_ffmpeg",
    source=filename
)
```

---

### Step 5: Run Bot

```bash
python bot.py
```

---

## How It Works

1. Bot connects to Discord using bot token
2. Bot synchronizes slash commands
3. New users trigger welcome system
4. Commands allow voice/music interaction
5. YouTube songs stream through FFmpeg

---

## Future Improvements

* Queue system for music
* Playlist support
* Better moderation commands
* AI chatbot integration
* Custom server settings
* Admin permissions system

---

## Disclaimer

This project is intended for educational and development purposes. Ensure compliance with Discord Terms of Service and copyright regulations while streaming media.

---

## Developer Information

**Project Name:** Discord Server Bot

**Developed By:** Sashank Sahil & Himanshu Ranjan

**Language:** Python

**Type:** Discord Automation & Entertainment Bot
