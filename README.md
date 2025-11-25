# YouTube Video Recommender Chatbot

A **Dialogflow-based chatbot** that recommends YouTube videos based on user preferences such as category, duration, and style. This project uses **Dialogflow ES** for natural language understanding and a **Python Flask webhook** to fetch video results from the YouTube Data API v3.

---

## Features

- Conversational interface where users specify the type of video they want to watch.
- Asks follow-up questions for more specific recommendations.
- Fetches video results from YouTube using the YouTube Data API.
- Returns video title and link to the user in chat.
- Easily extensible to include more parameters (e.g., language, popularity).

---

## Technologies Used

- **Dialogflow ES** – For intent recognition and conversation handling.
- **Python 3 & Flask** – Webhook server to process requests and fetch videos.
- **YouTube Data API v3** – To search and retrieve video data.
- **Ngrok** – For local webhook testing (optional).

---

## Getting Started

### Prerequisites

- Python 3.10+
- `pip` package manager
- YouTube Data API key (enable API v3 in [Google Cloud Console](https://console.cloud.google.com/))

---

### Installation

1. Clone the repository:

```bash
git clone https://github.com/yourusername/youtube-chatbot.git
cd youtube-chatbot
