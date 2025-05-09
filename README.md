# YouTube Channel Analytics and Data Extraction via YouTube Data API

## 📌 Project Overview

This project is designed to **fetch, process, and analyze data** from a specified **YouTube channel** using the [YouTube Data API v3](https://developers.google.com/youtube/v3). It extracts vital video statistics such as video IDs, titles, publication dates, view counts, like counts, and comment counts. The project is developed using Python and structured to be beginner-friendly, modular, and extensible.

# 🔑 Setup and Installation

### Step 1: Clone the Repository

git clone https://github.com/yourusername/youtube-api-project.git
cd youtube-api-project
Step 2: Create Virtual Environment (Optional)
bash
Copy
Edit
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
Step 3: Install Requirements
bash
Copy
Edit
pip install -r requirements.txt
Step 4: Get Your YouTube Data API Key
Go to Google Developers Console

Create a project

Enable YouTube Data API v3

Go to Credentials → Create API Key

Copy and paste it into your script

🔧 Code Explanation
📂 Import Libraries
python
Copy
Edit
import pandas as pd
import requests
import time
🔐 Set Your API Key and Channel ID
python
Copy
Edit
API_KEY = "YOUR_API_KEY"
CHANNEL_ID = "YOUR_CHANNEL_ID"
🔁 Define a Function to Fetch Video Statistics
python
Copy
Edit
def get_video_details(video_id):
    # function implementation
    return view_count, like_count, comment_count
🔁 Define Main Function to Get Videos
python
Copy
Edit
def get_videos(df):
    # function implementation
    return df
✅ Initialize and Run
python
Copy
Edit
df = pd.DataFrame(columns=[...])
df = get_videos(df)
print(df)
🧠 How Pagination Works
The YouTube API returns a limited number of results per page. To get all results, you need to use the nextPageToken value returned in each response. You can implement this inside a while loop or recursive function.

To Do:
Implement full pagination to collect videos beyond 50 results.

This is especially useful for:

- Content creators who want analytics for their videos.
- Researchers collecting video metadata.
- Data analysts building dashboards or models based on YouTube data.
- Students learning how to work with real APIs and pandas in Python.

---

## 🚀 Features

- 🔌 Connects to YouTube Data API v3
- 📽️ Extracts all videos from a channel
- 📊 Collects metadata: title, publish date, view count, like count, and comment count
- 🧹 Saves data into a clean `pandas` DataFrame
- ⏱️ Can be extended to include pagination, scheduling, or database export

---

## 🛠️ Tech Stack

- **Python 3.x**
- **Google YouTube Data API v3**
- **pandas**
- **requests**
- (Optional) Jupyter or Google Colab for running notebooks

---

## 📁 Project Structure

```plaintext
youtube-api-project/
│
├── README.md                  # Project documentation
├── api_fetch.ipynb            # Colab notebook with all code
├── credentials.txt (ignore)   # API key (should be in .gitignore)
├── requirements.txt           # Python dependencies
└── outputs/
    └── youtube_data.csv       # Optional: output file if exported
