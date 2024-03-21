# YouTube Video Metrics Extraction

## Overview:
This script collects video metrics (view count, like count, comment count) from the YouTube channel of Neo4j using the YouTube Data API. The extracted data is stored in a CSV file for further analysis.

## Requirements:
- Python 3.x
- pandas
- requests

## Setup Instructions:
1. Obtain a YouTube Data API key from the Google Cloud Console.
2. Replace the `API_KEY` variable with your API key.
3. Set the `CHANNEL_ID` variable to the channel ID of Neo4j.

## Usage:
1. Run the script `Neo4j_youtube_api.ipynb`.
2. The script will fetch video metrics for all videos on the Neo4j channel.
3. The extracted data will be stored in a CSV file named `youtube_vids.csv`.

## Script Explanation:
1. The `get_video_details` function retrieves view count, like count, and comment count for a given video ID.
2. The `get_videos` function fetches video details (title, upload date) for all videos on the Neo4j channel and calls `get_video_details` to get metrics.
3. The main script builds a DataFrame to store video data and calls `get_videos` to populate it.
4. Any errors encountered during the API request are handled gracefully.

## Output:
The output CSV file `youtube_vids.csv` contains the following columns:
- `video_id`: Unique ID of the video
- `video_title`: Title of the video
- `upload_date`: Date of video upload
- `view_count`: Number of views
- `like_count`: Number of likes
- `comment_count`: Number of comments

## License:
This project is licensed under the [MIT License](https://opensource.org/licenses/MIT).
