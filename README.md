YouTube Video Recommender Chatbot

A Dialogflow-based chatbot that recommends YouTube videos based on user preferences such as category, duration, and style. This project uses Dialogflow ES for natural language understanding and a Python Flask webhook to fetch video results from the YouTube Data API v3.

Features

Conversational interface where users specify the type of video they want to watch.

Asks follow-up questions for more specific recommendations.

Fetches video results from YouTube using the YouTube Data API.

Returns video title and link to the user in chat.

Easily extensible to include more parameters (e.g., language, popularity).

Technologies Used

Dialogflow ES – For intent recognition and conversation handling.

Python 3 & Flask – Webhook server to process requests and fetch videos.

YouTube Data API v3 – To search and retrieve video data.

Ngrok – For local webhook testing (optional).

Getting Started
Prerequisites

Python 3.10+

pip package manager

YouTube Data API key (enable API v3 in Google Cloud Console
)

Installation

Clone the repository:

git clone https://github.com/yourusername/youtube-chatbot.git
cd youtube-chatbot


Install dependencies:

pip install -r requirements.txt


Set your YouTube API key in app.py:

YOUTUBE_API_KEY = "YOUR_API_KEY_HERE"

Running the Webhook Locally

Start the Flask server:

python app.py


(Optional) Expose your local server to the internet using ngrok:

ngrok http 5000


Copy the ngrok URL and set it as your Webhook URL in Dialogflow:

https://<your-ngrok-id>.ngrok-free.dev/webhook

Testing

Open the Dialogflow console → Try sending messages like:

I want to watch a cardio video


The bot will ask follow-up questions (duration, style) and then return a YouTube video link.

For debugging, check the Flask console to see API requests and responses.

Folder Structure
youtube-chatbot/
│
├─ app.py             # Flask webhook server
├─ requirements.txt   # Python dependencies
├─ README.md
└─ dialogflow_agent/  # Exported Dialogflow agent ZIP

Contributing

Fork the repository

Create a new branch: git checkout -b feature-name

Commit changes: git commit -m "Add new feature"

Push to branch: git push origin feature-name

Create a pull request

License

This project is licensed under the MIT License – see the LICENSE
 file for details.
