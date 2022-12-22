# Vinted Alerting Bot

I decided to open-source by Vinted alerting bot. This bot will inform you via Discord message when new articles that correspond to your criteria are posted on Vinted.

## How it works?

Once installed, your Discord server will have 3 new commands registered:

```sh
/subscriptions # Display the list of your subscribed searches with ID
/subscribe [channel] [url] # Subscribe to a new search and receive alerts in a channel
/unsubscribe [id] # Unsubscribe of an alert with its ID
```

Once you saved a subscription, the bot will fetch new articles every 30 seconds and alert you in case of new findings!

### Creating bot on Discord Developer

1. Create an application on [Discord Developer](https://discord.com/developers/applications)
2. Create a bot in your application
3. Copy the `.env.example` file to `.env` and copy/paste the token
4. Invite your bot by generating an URL (OAuth2 -> URl Generator)

**Important:** Set the following scopes:

- `bot`
- `applications.commands`

And also set the following bot permission:

- Send Messages
- Embed Links
- Read Messages/View Channels
- Use Slash Commands

### Installation

Python >3.8 is recommended.

1. Install dependencies: `pip install -r requirements.txt`
2. Start the bot: `python main.py`

If you want to stop the bot, you can just press **CTRL+C** once. Don't spam **CTRL+C**, it may take a few seconds before it completely stop because of the background thread used to sync items.

### Keeping the bot up all the time

