# YouTube Video Recommender Chatbot

A Dialogflow-based chatbot that recommends YouTube videos based on user preferences such as category, duration, and style. This project uses Dialogflow ES for natural language understanding and a Python Flask webhook to fetch video results from the YouTube Data API v3.

## Features

- Conversational interface where users specify the type of video they want to watch.  
- Asks follow-up questions for more specific recommendations.  
- Fetches video results from YouTube using the YouTube Data API.  
- Returns video title and link to the user in chat.  
- Easily extensible to include more parameters (e.g., language, popularity).  

## Technologies Used

- **Dialogflow ES** – For intent recognition and conversation handling.  
- **Python 3 & Flask** – Webhook server to process requests and fetch videos.  
- **YouTube Data API v3** – To search and retrieve video data.  
- **Ngrok** – For local webhook testing (optional).  

## Getting Started

### Prerequisites

- Python 3.10+  
- `pip` package manager  
- YouTube Data API key (enable API v3 in Google Cloud Console)  

### Installation

Clone the repository:

```bash
git clone https://github.com/sgracevera/GRAY---a-youtube-video-recommender
cd youtube-chatbot


Install dependencies:

```bash
pip install -r requirements.txt
```

Set your YouTube API key in `app.py`:

```python
YOUTUBE_API_KEY = "YOUR_API_KEY_HERE"
```

### Running the Webhook Locally

Start the Flask server:

```bash
python app.py
```

(Optional) Expose your local server to the internet using ngrok:

```bash
ngrok http 5000
```

Copy the ngrok URL and set it as your Webhook URL in Dialogflow:

```
https://<your-ngrok-id>.ngrok-free.dev/webhook
```

### Testing

Open the Dialogflow console and try sending messages like:

```
I want to watch a cardio video
```

* The bot will ask follow-up questions (duration, style) and then return a YouTube video link.
* For debugging, check the Flask console to see API requests and responses.

## Folder Structure

```
youtube-chatbot/
│
├─ app.py             # Flask webhook server
├─ requirements.txt   # Python dependencies
├─ README.md
└─ dialogflow_agent/  # Exported Dialogflow agent ZIP
```

## Contributing

1. Fork the repository
2. Create a new branch: `git checkout -b feature-name`
3. Commit changes: `git commit -m "Add new feature"`
4. Push to branch: `git push origin feature-name`
5. Create a pull request

## License

This project is licensed under the MIT License – see the LICENSE file for details.

```

If you want, I can also make a **slightly prettier version with badges** (Python version, license, API, etc.) for GitHub that looks more professional. Do you want me to do that?
```
