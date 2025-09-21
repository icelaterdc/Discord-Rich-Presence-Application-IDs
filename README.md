# 🎮 Discord Rich Presence Application IDs

This repository provides a **curated list of verified Discord Rich Presence (RPC) Application IDs** for popular PC games. These IDs are essential when integrating RPC into applications, tools, or bots, enabling them to display in-game activity accurately on Discord.

The list is split into two categories:
1. **Verified IDs** → Official / confirmed Application IDs from trusted sources (Discord Developer Docs, PresenceDB, and verified RPC archives).
2. **Community IDs** → Widely used Application IDs in the community, but not officially confirmed.

---

## ✅ Verified Application IDs
Below is a collection of verified Rich Presence Application IDs for popular PC games.

| Game Title                        | Application ID        |
|-----------------------------------|-----------------------|
| PLAYERUNKNOWN’S BATTLEGROUNDS     | `356873622985506820` |
| Apex Legends                      | `542075586886107149` |
| Fortnite                          | `1402418703554842694`|
| Dota 2                            | `356875988589740042` |
| Counter-Strike: Global Offensive  | `356875057940791296` |
| Counter-Strike 2                  | `1158877933042143272`|
| VALORANT                          | `700136079562375258` |
| Overwatch 2                       | `356875221078245376` |
| Minecraft                         | `1402418491272986635`|
| League of Legends                 | `401518684763586560` |
| Rocket League                     | `356877880938070016` |
| Warframe                          | `1402418586244612216`|
| Genshin Impact                    | `762434991303950386` |
| World of Warcraft                 | `356875762940379136` |
| Call of Duty: Modern Warfare      | `631914894446297148` |
| SpeedRunners                      | `259392830932254721` |
| Forza Horizon 5                   | `905961880789590076` |
| Fall Guys                         | `742897755160313986` |
| ELDEN RING                        | `1402418436809953330`|
| Dead by Daylight                  | `357607133254254632` |
| Satisfactory                      | `1402416959819350078`|

---

## 🌍 Community-Sourced IDs
These IDs are not officially verified but are widely used by the community. They may change over time.

| Game Title               | Application ID        |
|--------------------------|-----------------------|
| Among Us                 | `1402418440685486130`|
| Rust                     | `1402418594532298837`|
| Terraria                 | `1402418344912752671`|
| Stardew Valley           | `1233785540982345870`|
| Hollow Knight            | `363431029484027904` |
| Factorio                 | `358422126602223616` |
| Don’t Starve Together    | `359508004078616586` |
| Cities: Skylines II      | `1166420945016201326`|
| Europa Universalis IV    | `687351243462541358` |
| The Elder Scrolls V: Skyrim | `359507724196773888` |
| Grand Theft Auto V (Modded) | `1402418714716143646`|

---

## 📌 Usage Example
Here’s a simple Node.js snippet using [discord-rpc](https://www.npmjs.com/package/discord-rpc):

```js
const RPC = require("discord-rpc");
const client = new RPC.Client({ transport: "ipc" });

const clientId = "356875057940791296"; // Example: CS:GO

RPC.register(clientId);

client.on("ready", () => {
  console.log("RPC connected as", client.user.username);

  client.setActivity({
    details: "Competitive Match",
    state: "Dust II",
    startTimestamp: new Date(),
    largeImageKey: "default",
    largeImageText: "Counter-Strike: Global Offensive",
    smallImageKey: "csgo",
    smallImageText: "In Game",
    instance: false,
  });
});

client.login({ clientId }).catch(console.error);
```

---

## ⚠️ Disclaimer
- Some IDs (especially community-sourced) might change or stop working if developers update their integrations.
- Always prefer **verified IDs** when possible.
- This repository is community-maintained. Feel free to contribute by opening a PR with new verified IDs.

---

## 📚 Sources
- [Discord Developer Documentation](https://discord.com/developers/docs/rich-presence/how-to)
- [PresenceDB](https://presencedb.com)
- Verified GitHub RPC archives

---

💡 *Maintained for developers, bot creators, and enthusiasts who want easy access to verified Discord Rich Presence IDs.*
