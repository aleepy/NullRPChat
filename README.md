# NullRPChat Plugin

**NullRPChat** is a lightweight Minecraft plugin designed to enhance roleplay (RP) experiences by introducing proximity-based chat commands. It allows players to communicate in a more immersive way, with messages only being heard by nearby players. Additionally, it integrates with DiscordSRV to relay in-game chat messages to a Discord channel.

---

## Features

- **Proximity Chat**: Messages are only visible to players within a configurable radius.
- **Custom Commands**:
  - `/me` - Roleplay actions (e.g., `* John waves hello`).
  - `/do` - Describes actions or events (e.g., `* The door creaks open`).
  - `/say` - Speak in-character (e.g., `John says: Hello!`).
  - `/whisper` - Send a private message to a nearby player.
- **Discord Integration**: Relay in-game chat messages to a Discord channel using DiscordSRV.
- **Customizable Formats**: Configure message formats, colors, and radii for each command.
- **PlaceholderAPI Support**: Use placeholders to customize messages further.
- **Permission-Based Access**: Restrict commands to specific players or groups.

---

## Installation

1. **Download the Plugin**:
   - Download the latest `.jar` file from the [Releases](https://github.com/aleepy/NullRPChat/releases) page.
   - Place the `.jar` file into your server's `plugins` folder.

2. **Install Dependencies**:
   - **[PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)** (optional but recommended for advanced customization).
   - **[DiscordSRV](https://www.spigotmc.org/resources/discordsrv.18494/)** (optional for Discord integration).

3. **Restart the Server**:
   - Restart your Minecraft server to load the plugin.

4. **Configure the Plugin**:
   - After the first run, a `config.yml` file will be generated in the `plugins/NullRPChat` folder.
   - Edit the configuration file to customize chat formats, radii, and other settings.

---

## Commands

| Command       | Description                                                                 | Permission Node         |
|---------------|-----------------------------------------------------------------------------|-------------------------|
| `/me <text>`  | Perform a roleplay action (e.g., `* John waves hello`).                     | `nullrpchat.me`         |
| `/do <text>`  | Describe an action or event (e.g., `* The door creaks open`).               | `nullrpchat.do`         |
| `/say <text>` | Speak in-character (e.g., `John says: Hello!`).                             | `nullrpchat.say`        |
| `/whisper <player> <text>` | Send a private message to a nearby player.                  | `nullrpchat.whisper`    |
| `/nullrpchat reload` | Reload the plugin configuration.                                | `nullrpchat.reload`     |

---

## Configuration

The `config.yml` file allows you to customize the plugin's behavior. Below is an example configuration:

```yaml
commands:
  me:
    enabled: true
    format: "&d<%player%> %message%"
    color: "#FF00FF"
    verb: ""
    radius: 50

  do:
    enabled: true
    format: "&e<%player%> %message%"
    color: "#FFFF00"
    verb: ""
    radius: 60

  say:
    enabled: true
    format: "&7<%player%> %message%"
    color: "#AAAAAA"
    verb: "said"
    radius: 40

  whisper:
    enabled: true
    format: "&7<%player%> %message%"
    color: "#AAAAAA"
    verb: "whisper:"
    radius: 20

