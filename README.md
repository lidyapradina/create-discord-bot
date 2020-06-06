# Create Discord Bot

[![Discord](https://discordapp.com/api/guilds/258167954913361930/embed.png)](https://discord.gg/WjEFnzC) [![Twitter Follow](https://img.shields.io/twitter/follow/peterthehan.svg?style=social)](https://twitter.com/peterthehan) [![Ko-fi](https://img.shields.io/badge/Donate-Ko--fi-F16061.svg?logo=ko-fi)](https://ko-fi.com/peterthehan) [![Patreon](https://img.shields.io/badge/Donate-Patreon-F96854.svg?logo=patreon)](https://www.patreon.com/peterthehan)

Create Discord bots using a simple widget-based framework.

## Bot Setup

### Create Bot

1. Go to Discord's [Developer Portal](https://discordapp.com/developers/applications/).
2. Create a new application.
3. Add a bot user to your app.
4. Find your bot token, you will need this in the next section.

> Keep this token and any file containing it **private**! If your token ever leaks or you suspect it may have leaked, simply `regenerate` a new token to invalidate your compromised token.

5. Invite your bot to a server using: [https://discordapp.com/oauth2/authorize?scope=bot&client_id=DISCORD_BOT_CLIENT_ID_PLACEHOLDER](https://discordapp.com/oauth2/authorize?scope=bot&client_id=DISCORD_BOT_CLIENT_ID_PLACEHOLDER)

> A Discord bot's client ID is not the same as its token!

### Get Bot

1. `npx peterthehan/create-discord-bot`
2. Follow the CLI instructions.

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/assets/master/repositories/create-discord-bot/npx-demo.gif" />
</div>

### Run Bot

1. `npm start` to start the bot.

> The bot should go from offline to online. Verify the bot is working by using the [ping](https://github.com/peterthehan/create-discord-bot/blob/master/app/src/widgets/command/commands/ping.js) command.

> The default command prefix is `.`. You can configure the [command](https://github.com/peterthehan/create-discord-bot/tree/master/app/src/widgets/command) widget's settings in [src/widgets/command/config.js](https://github.com/peterthehan/create-discord-bot/blob/master/app/src/widgets/command/config.js).

🎉 You're ready to create your own widgets! 🎉

## Widgets Setup

### Design

`create-discord-bot` comes with a [command](https://github.com/peterthehan/create-discord-bot/tree/master/app/src/widgets/command) widget. Simply follow the design of the [ping](https://github.com/peterthehan/create-discord-bot/blob/master/app/src/widgets/command/commands/ping.js) command to start building your own commands.

Each widget **must** live under the [src/widgets](https://github.com/peterthehan/create-discord-bot/tree/master/app/src/widgets) folder and **must** have a `handlers` folder containing **only** event handler files. In other words, a file tree diagram of these requirements would look like:

```
widgets
├───command
│   ├───handlers
|   |   ├───ready.js
|   |   └───message.js
├───widget1
│   ├───handlers
|   |   ├───eventHandler1.js*
|   |   ├───eventHandler2.js
|   |   └───other event handlers
├───widget2
│   ├───handlers
|   |   ├───eventHandler1.js
|   |   ├───eventHandler2.js
|   |   └───other event handlers
```

> \*: All event handler files must be named exactly the same as the emitted events found on the [Client](https://discord.js.org/#/docs/main/master/class/Client) page.

<div align="center">
  <img src="https://raw.githubusercontent.com/peterthehan/assets/master/repositories/create-discord-bot/diagram.png" />
</div>

### Widgets

The following widgets can be used by this framework by moving them into the [src/widgets](https://github.com/peterthehan/create-discord-bot/tree/master/app/src/widgets) folder:

- https://github.com/peterthehan/discord-active-role-bot
- https://github.com/peterthehan/discord-audit-log-bot
- https://github.com/peterthehan/discord-birthday-role-bot
- https://github.com/peterthehan/discord-emoji-log-bot
- https://github.com/peterthehan/discord-reaction-role-bot

## Troubleshooting

- Check if you have the latest LTS version of Node.js (v12.x.x) using `node -v`.
- If the app outputs an error for `Cannot find module <...>`, try `npm install` again.

Visit for more help or information!

<a href="https://discord.gg/WjEFnzC">
  <img src="https://discordapp.com/api/guilds/258167954913361930/embed.png?style=banner2" title="Discord Server"/>
</a>
