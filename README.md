<img width="1254" height="1254" alt="clipfyLOGO" src="https://github.com/user-attachments/assets/3c0f6b4f-dd40-4a3d-a623-15e2b6229be2" />
# LIVE-CLIPPER
# 🌴 Clipador — Automatic Live Clipper

**Turn live streams into clips automatically.**

Clipador is a Python application that monitors live streams, identifies potentially interesting moments through audio analysis and chat activity, and automatically creates video clips.

The project includes an integrated web dashboard for managing channels, recordings, settings, users, and video libraries.

---

## ✨ Features

- 📡 **Automatic Monitoring:** Monitors channels and detects when a live stream starts.
- 🎥 **Live Recording:** Saves complete live streams locally.
- 🔊 **Highlight Detection:** Detects audio peaks and changes in chat activity.
- 💬 **Chat Analysis:** Uses Twitch chat messages to help identify interesting moments.
- ✂️ **Automatic Clipping:** Turns detected moments into individual video clips.
- 📊 **Scoring System:** Assigns scores to clips based on audio and chat indicators.
- 📱 **Vertical Video Format:** Supports video output in 1080x1920 resolution.
- 🤖 **AI Integration:** Uses the Anthropic API to generate titles based on the visual content of clips.
- 📚 **Video Library:** Organizes, plays, downloads, favorites, and deletes clips.
- 👤 **User Management:** Supports individual accounts, permissions, and daily usage limits.
- ⚙️ **Control Dashboard:** Provides a web interface to monitor and configure the application.

## 🖥️ Technologies

| Technology | Purpose |
|---|---|
| Python 3.8+ | Backend and processing |
| HTML5 | Interface structure |
| CSS3 | Styling |
| JavaScript | Frontend interactivity |
| FFmpeg | Video recording, conversion, and editing |
| Streamlink | Live stream capture |
| yt-dlp | Video downloading and processing |
| Anthropic API | AI-powered title generation |
| JSON | Data storage |

## 📋 Requirements

Before running the project, make sure you have installed:

- Python 3.8 or newer.
- FFmpeg.
- Streamlink.
- yt-dlp (for processing videos from URLs).

### Install FFmpeg

**Windows:**

```powershell
winget install ffmpeg
```

You can also download it from the official website:

https://ffmpeg.org/download.html

### Install Python dependencies

```bash
pip install streamlink yt-dlp
```

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/YOUR-USERNAME/clipador.git
```

### 2. Navigate to the project directory

```bash
cd clipador
```

### 3. Install dependencies

```bash
pip install streamlink yt-dlp
```

### 4. Run the application

```bash
python clipador.py
```

### 5. Open the dashboard

Open your browser and visit:

http://localhost:8765

On the first launch, you will be asked to create the administrator password.

**Note:** The initial administrator username is defined in the source code as `rafael_22`.

## 🎛️ How It Works

The application follows an automated workflow:

1. The user adds a channel to the monitoring list.
2. Clipador checks whether the channel is live.
3. When a stream starts, recording begins automatically.
4. The system analyzes audio and, when available, chat activity.
5. Detected moments are converted into video clips.
6. Each clip receives a score.
7. Approved clips are saved to the video library.

For YouTube videos, users can also submit a video URL and start automatic processing.

## ⚙️ Configuration

Clipador provides several options to customize the clipping process:

| Setting | Description |
|---|---|
| Pre-clip | Amount of footage captured before a detected moment |
| Post-clip | Amount of footage captured after a detected moment |
| Sensitivity | Audio detection sensitivity |
| Cooldown | Minimum interval between detections |
| Audio floor | Minimum audio intensity threshold |
| Minimum score | Minimum score required to keep a clip |
| Vertical format | Enables 9:16 video conversion |
| Keep TS | Preserves the original recording file |
| Rename mode | Defines how clips are named |
| API Key | Enables AI integration |

## 📁 File Structure

Clipador automatically organizes generated files:

```text
Clipador/
│
├── Biblioteca/
│   ├── rafael_22/
│   │   └── channel/
│   │       ├── clip.mp4
│   │       ├── clip.jpg
│   │       └── clip.json
│   │
│   └── other_users/
│
├── Lives/
│   └── user/
│
├── Videos/
│   └── user/
│
├── config.json
└── users.json
```

Each clip can have three associated files:

- `.mp4` — Video file.
- `.jpg` — Thumbnail.
- `.json` — Clip metadata and statistics.

## 🤖 Artificial Intelligence

The project supports integration with the Anthropic API to automatically generate clip titles.

The AI receives selected frames extracted from the clip, along with information about the detected moment.

Its purpose is to generate short titles in Brazilian Portuguese, making clips easier to identify and organize.

This feature requires a valid Anthropic API key and may incur API usage costs.

## 🔐 Security and User Accounts

The application includes:

- Username and password authentication.
- Password hashing using PBKDF2-HMAC-SHA256 with individual salts.
- User sessions.
- Separate user libraries.
- Administrator permissions.
- Daily clipping limits.
- Channel limits per account.

**Important:** This project was designed primarily for local use. Before exposing it publicly or over a network, additional security measures are recommended, including HTTPS, CSRF protection, and more robust session management.

## ⚠️ Limitations

- Automatic detection relies on audio and chat indicators rather than full semantic understanding.
- Real-time chat collection is currently implemented for Twitch.
- Stream availability depends on Streamlink support.
- AI title generation requires the Anthropic API.
- Processing requires CPU, memory, and storage resources.
- Behavior may vary depending on the platform and content availability.

## 🛠️ Development

Clipador was developed in Python, combining video-processing tools with an integrated web interface.

Its architecture allows the project to evolve through new features, integrations, and improvements to the highlight detection algorithm.

## 📌 Disclaimer

This project is intended for legitimate development and usage purposes.

Please respect copyright laws, platform terms of service, and content creators' permissions when recording, editing, or sharing live streams.

## 📄 License

No license has been specified yet. Please review the terms of use before redistributing or modifying this project.

---

**Clipador — Less time searching for moments. More time creating content.** 🌴
