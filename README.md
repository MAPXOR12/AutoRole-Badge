# Discord AutoRole Badges

[![downloadsBadge](https://img.shields.io/npm/dt/discord-autorole-badges?style=for-the-badge)](https://npmjs.com/discord-autorole-badges)
[![versionBadge](https://img.shields.io/npm/v/discord-autorole-badges?style=for-the-badge)](https://npmjs.com/discord-autorole-badges)

Discord AutoRole Badges New is a powerful [Node.js](https://nodejs.org) module that allows you to easily give badges roles when new member join a server

If you don't understand something in this page, you are experiencing problems, or you just need a gentle
nudge in the right direction, please don't hesitate to join our official [Support Server](https://discord.gg/QAcAksjZmC)

## Note 
Pls Star This Project ⭐️
## Installation

```
npm i discord-autorole-badges-new
```

## Example
```js
const {Manager} = require('discord-autorole-badges');
const {Client} = require('discord.js');
const client = new Client({ intents: 32767})


let manager = new Manager(client, {
    STAFF: "role_id",
    PARTNER: "role_id",
    HYPESQUAD: "role_id",
    BUG_HUNTER_LEVEL_1: "role_id",
    HYPESQUAD_ONLINE_HOUSE_1: "role_id",
    HYPESQUAD_ONLINE_HOUSE_2: "role_id",
    HYPESQUAD_ONLINE_HOUSE_3: "role_id",
    PREMIUM_EARLY_SUPPORTER: "role_id",
    TEAM_USER: "role_id",
    BUG_HUNTER_LEVEL_2: "role_id",
    VERIFIED_BOT: "role_id",
    ACTIVE_DEVELOPER: "role_id",
    VERIFIED_DEVELOPER: "role_id",
    CERTIFIED_MODERATOR: "role_id",
    

})
client.on("guildMemberAdd", async (member) => {
    await manager.setRole(member);
})

client.on("ready", () => {
    console.log("ready")
})

client.login("SUPER_SECRET_TOKEN")
```

List of supported badges by the package: 
Links: 
* [Discord.js Documentation](https://discord.js.org/#/docs/main/stable/class/UserFlags?scrollTo=s-FLAGS)
* [Discord.dev](https://discord.com/developers/docs/resources/user#user-object-user-flags)
```js
    STAFF
    PARTNER
    HYPESQUAD
    BUG_HUNTER_LEVEL_1
    HYPESQUAD_ONLINE_HOUSE_1
    HYPESQUAD_ONLINE_HOUSE_2
    HYPESQUAD_ONLINE_HOUSE_3
    PREMIUM_EARLY_SUPPORTER
    TEAM_USER
    BUG_HUNTER_LEVEL_2
    VERIFIED_BOT
    ACTIVE_DEVELOPER
    VERIFIED_DEVELOPER
    CERTIFIED_MODERATOR
```
