# DjsV13-Handler
An easy Djs V13 Handler for your bot!

[![Remix on Glitch](https://cdn.glitch.com/2703baf2-b643-4da7-ab91-7ee2a2d00b5b%2Fremix-button.svg)](https://glitch.com/edit/#!/import/github/FikryGanzz/DjsV13-Handler)<br>
[![Run on Repl.it](https://repl.it/badge/github/vcodes-xyz/bot-list)](https://repl.it/github/FikryGanzz/DjsV13-Handler)<br>
[![ISSUES](https://img.shields.io/github/issues-raw/FikryGanzz/DjsV13-Handler?color=blue&logo=github&style=for-the-badge)](https://github.com/FikryGanzz/DjsV13-Handler/issues)

## Requirements
1. Discord bot token **[GUIDE](https://discordjs.guide/preparations/setting-up-a-bot-application.html#creating-your-bot)**
2. MongoDB URI **[LINK](https://mongodb.com/)**
3. Node.js v16.6.0 or newer
4. Brain(ofc)

## Configuration 
**⚠️Don't let others see your Discord Bot Token or MongoDB Uri⚠️**

Fill out the values on the `config.json`!
```json
{
        "prefix": ":",
        "ownerID": [""],
        "token": "",
        "mongoUri": "",
}
```
## For Replit User, Run:
```shell
npm i --save-dev node@latest && npm config set prefix=$(pwd)/node_modules/node && export PATH=$(pwd)/node_modules/node/bin:$PATH
```

## Setup
1. Run `npm install` to install all the required package
2. Run `node index.js` to starting the bot

## How to make Command or Slash Command?
1. Command
```js
const { Client, Message, MessageEmbed } = require("discord.js");
module.exports = {
        name: "",
        description: "",
        aliases: [""],
        ownerOnly: false,
        userPermissions: [""],
        botPermissions: [""],
        usage: [""],
        args: /*boolean (true or false)*/,
        /**
         * @param {Client} client
         * @param {Message} message
         * @param {String()} args
         */
        run: async(client, message, args) => {}
}
```
2. Slash Command
```js
const { Client, CommandInteraction, MessageEmbed } = require("discord.js");
module.exports = {
        name: "",
        description: "",
        userPermissions: [""],
        botPermissions: [""],
        ownerOnly: false,
        options: [
                {
                name: "",
                description: "",
                type: "STRING",
                required: false
        }
                 ],
        type: "CHAT_INPUT",
        /**
         * @param {Client} client
         * @param {CommandInteraction} interaction
         */
        run: async({ client, interaction }) => {}
}
```