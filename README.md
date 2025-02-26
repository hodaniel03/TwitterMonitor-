# Twitter Monitor with Discord Integration

This project is a Twitter Monitor that checks the latest tweets from a list of monitored Twitter users and posts any new tweets to a Discord channel using a webhook. The script uses the Tweepy v2 API to interact with Twitter and retrieve tweet data, ensuring that only new tweets (i.e., tweets posted after the script starts running) are posted to Discord.

# Features
- Monitors specified Twitter accounts for new tweets.
- Checks for new tweets every 5 minutes (configurable).
- Posts tweet URLs to a Discord channel using a Webhook when a new tweet is detected.
- Handles rate limiting by waiting when the Twitter API rate limit is exceeded (up to 15 requests per 15-minute window on the free API plan).
- Timezone-aware comparison of tweet creation times to ensure that only new tweets are posted.

# Technologies Used
Python: Main programming language for writing the script.
Tweepy: Python wrapper for interacting with the Twitter API v2.
requests: To send data to the Discord webhook.
pytz: To handle timezone-aware datetime comparisons between the tweet time and the script's current time.
dotenv: For securely loading API credentials (Bearer Token and Discord Webhook URL) from a .env file.
