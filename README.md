# Golang Slack Bot with Wolfram Alpha and Wit.ai

## Overview
This project is a Slack bot built in Golang that integrates Wolfram Alpha and Wit.ai to process user queries. The bot listens for messages on Slack, extracts relevant information using Wit.ai, and fetches computational answers from Wolfram Alpha.

## Features
- Listens for messages on Slack
- Uses Wit.ai to interpret natural language queries
- Queries Wolfram Alpha for answers
- Responds with computed answers directly in Slack
- Logs command events for analytics

## Prerequisites
Before running the bot, ensure you have the following installed:
- Golang (latest stable version recommended)
- A Slack bot token and app token
- A Wit.ai API token
- A Wolfram Alpha API key

## Installation
1. Clone this repository:
   ```sh
   git clone https://github.com/yourusername/golang-slack-bot.git
   cd golang-slack-bot
   ```
2. Install dependencies:
   ```sh
   go mod tidy
   ```
3. Set up your API keys in a `.env` file:
   ```sh
   SLACK_BOT_TOKEN=your_slack_bot_token
   SLACK_APP_TOKEN=your_slack_app_token
   WIT_AI_TOKEN=your_wit_ai_token
   WOLFRAM_APP_ID=your_wolfram_app_id
   ```

## Usage
To run the bot, use:
```sh
   go run main.go
```
Once running, the bot listens for commands in Slack and processes queries through Wit.ai and Wolfram Alpha.

## Command Format
The bot listens for commands in the following format:
```
q - <message>
```
**Example:**
```
q - Who is the president of India?
```
The bot processes the message, extracts the intent using Wit.ai, queries Wolfram Alpha, and responds with the computed answer.

## Code Structure
- `main.go` - Initializes the bot and defines command handling
- Uses `slacker` for Slack bot interactions
- Uses `wit-ai/wit-go` for NLP processing
- Uses `go-wolfram` for fetching Wolfram Alpha answers

