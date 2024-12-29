# 📞Truecaller Search Bot

A Telegram bot that uses an unofficial Truecaller API to look up phone number information instantly. It's an alternative for occasional use of Truecaller than running their app in background all the time.

<br>
<div align="center"><img src=".doc/marquee.png" /><br>This bot is based on the <a href="https://github.com/sumithemmadi/truecallerjs">sumithemmadi/truecallerjs</a> library and is live at <a href="https://t.me/truecallerjs_bot">@truecallerjs_bot</a></div>

## Self-host

This is a Deno project currently deployed on Deno Deploy. It uses Deno KV which requires you to [join the waitlist](https://dash.deno.com/kv) first before you get access to it.

### Setup Telegram Bot

1. Create a new bot using [@BotFather](https://t.me/BotFather).
2. Set the bot commands:

   ```plaintext
   login - Login to Truecaller
   installation_id - Login via existing token
   logout - Logout from Truecaller
   info - Information about the bot
   ```

3. [Set the webhook URL](https://core.telegram.org/bots/api#setwebhook) after deploying the bot using the following procedure.

### Deno Deploy

1. [Fork](/../../fork) this repo on GitHub.
2. Create a [new Deno Deploy](https://dash.deno.com/new) project from the forked repo.
3. Go to the project's `Settings` tab and add the Environment Variables from [.env.example](.env.example) file. You can skip adding the optional envs as they aren't critical to the service.
4. Grab the deployment URL from the `Overview` tab and set the webhook mentioned in previous section.

## Information


ure! Here is a sample README.md file for your Deno server project that interacts with the Truecaller API and Telegram bot API.

Markdown
# TruecallerJS Telegram Bot

This project is a Deno server that integrates with the Truecaller API and Telegram bot API. The bot can handle webhook requests from Telegram, manage user login states, and perform searches on Truecaller.

## Features

- Login to Truecaller using OTP.
- Manage user states and session data.
- Search for phone numbers using the Truecaller API.
- Report errors and events to a specified Telegram channel.

## Prerequisites

- [Deno](https://deno.land/)
- [Tor](https://www.torproject.org/)
- A Telegram bot token
- Environment variables set up

## Installation

### Step 1: Install Deno

Run the following commands to install Deno:

```sh
curl -fsSL https://deno.land/x/install/install.sh | sh
Add Deno to your shell profile (e.g., ~/.bashrc or ~/.zshrc):

sh
echo 'export DENO_INSTALL="/home/$USER/.deno"' >> ~/.bashrc
echo 'export PATH="$DENO_INSTALL/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
Step 2: Set Up Environment Variables
Create a .env file in your project directory and add the necessary environment variables:

sh
TG_THIS_BOT_TOKEN=your_telegram_bot_token
TG_REPORT_CHANNEL_ID=your_report_channel_id
EVENT_PING_URL=your_event_ping_url
EVENT_PING_PROJECT_ID=your_event_ping_project_id
Step 3: Install and Start Tor
Install Tor on your machine:

sh
sudo apt-get update
sudo apt-get install tor
Start the Tor service:

sudo service tor start
Step 4: Create and Configure the Bot Code
Create a new file named bot.ts and paste the provided code into it.

Step 5: Run the Server
Execute the server with the necessary permissions:

deno run --allow-net --allow-env bot.ts
Usage
Commands
/start: Start the bot and get a welcome message.
/login: Login to Truecaller using your phone number.
/installation_id: Enter your Truecaller installation ID.
/logout: Logout from Truecaller.
/info: Get the current status and installation ID.
/search: Search for a phone number using the Truecaller API.
Example
Send /start to the bot to begin:

Code
You need to /login to Truecaller with your existing account to use the bot.
Only you will be using your own account to search the numbers.
Contributing
Feel free to open issues or submit pull requests on the GitHub repository.

License
This project is licensed under the MIT License.

Feel free to customize this `README.md` file further to suit your project's specific needs.


**Author:** [Nissan Ahmed](https://anissan.com) ([@ni554n](https://twitter.com/ni554n))

**Donate:** [PayPal](https://paypal.me/ni554n)
<img src="https://ping.anissan.com/?repo=truecallerjs_bot" width="0" height="0" align="right">
