# NFT Discord Bot
This is a discord bot for ERC721 NFT collections, all the token metadata is being retrieved from opensea at the moment, instead of directly from the tokenURI in the smart contract. The bot will track nft related transactions of specified accounts

## Automatic Posts
### **Events**
The bot will track nft related transactions of specified accounts. The bot will look up events on OpenSea every 15 seconds, and all events will be posted to the configured Discord channel.

![Sales bot example](https://i.imgur.com/jUHRJWi.png)

# Configuration

| Var      | Description | Location |
| ----------- | ----------- | ----------- |
| accounts      | List of accounts to track       | You can find and modify in it [/cronjobs/sales.js](https://github.com/clovisjohn/nft-wallet-tracker/blob/9d4dfd5096947257d1abe3ded82d0af031033db6/cronjobs/sales.js#L5) |

| Env Var      | Description |
| ----------- | ----------- |
| DISCORD_BOT_TOKEN   | Pretty self explanatory        |
| DISCORD_SALES_CHANNEL_ID   | The discord channel id where sales events should be posted to, should look like a long number       |
| DISCORD_TOKEN_COMMAND | The command word you'd like the bot to respond to for posting token information, pick a simple word that represents the collection, see example above |
| OPEN_SEA_API_KEY | Contact OpenSea to request an API key at https://docs.opensea.io/reference#request-an-api-key.  The bot will work without it, but heavy use may result in being blocked. |

# Deployment
If running locally, just checkout the repository and run
  
`npm install`

followed by

`npm start`

You can also deploy directly to Heroku in just a few minutes.

[![Deploy](https://www.herokucdn.com/deploy/button.svg)](https://heroku.com/deploy)
