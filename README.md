# LyricBot – Commands & Usage

LyricBot is a Minecraft bot that prints song lyrics directly into chat.  
It also supports utility commands such as echoing text and stopping playback.  
All commands are prefixed with an exclamation mark (`!`).

---

## General Usage
- Prefix every command with `!` (example: `!song "Tokyo" <SECRET_KEY>`).
- Some commands require an authorization key (`SECRET_KEY`) for validation.
- Arguments are case‑insensitive unless otherwise noted.

---

## Commands

### `!song "SONGNAME" SECRET_KEY`
Starts playing a song.  
- **SONGNAME**: Either a title that matches a song in the bot’s database, or a GitHub raw link containing lyrics.  
- **SECRET_KEY**: Required authorization key.  
- **Behavior**: Prints lyrics line by line into chat. If a song is already playing, the bot will refuse until stopped.

---

### `!echo "TEXT" SECRET_KEY`
Echoes text through the bot.  
- **TEXT**: The message you want the bot to say.  
- **SECRET_KEY**: Required authorization key.  
- **Behavior**: Sends the specified text into chat as if the bot were speaking.

---

### `!stop SECRET_KEY`
Stops the currently playing song.  
- **SECRET_KEY**: Required authorization key.  
- **Behavior**: Immediately halts lyric playback. If no song is playing, the bot will notify you.

---

### `!help`
Displays help information.  
- **Arguments**: None.  
- **Behavior**: Sends a private message (`/msg`) to the requesting player listing all available commands.

---

## Security Notes
- Commands requiring `SECRET_KEY` ensure only authorized users can control the bot.
- The key can be rotated via console commands for added security.
- Unauthorized attempts are logged and ignored.

---

## Example Commands
```text
!song "Tokyo" <SECRET_KEY>
!echo "Hello world!" <SECRET_KEY>
!stop <SECRET_KEY>
!help
