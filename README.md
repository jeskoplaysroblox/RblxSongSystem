## 🎶 LyricBot – Commands & Usage

LyricBot is designed to print out song lyrics directly into Minecraft chat.  
It also supports utility commands such as echoing text and stopping playback.  
All commands are prefixed with an exclamation mark (`!`).

---

### 📖 General Usage
- Prefix every command with `!` (example: `!song "Tokyo" GPL6`)
- Some commands require the **SECRET_KEY** (default: `GPL6`) for validation
- Arguments are case-insensitive unless otherwise noted

---

### 📝 Commands

#### `!song "SONGNAME" SECRET_KEY`
- **Purpose:** Starts playing a song
- **Arguments:**
  - `SONGNAME` → Either:
    - A title that matches a song in the bot’s database, or
    - A full GitHub raw usercontent link containing lyrics
  - `SECRET_KEY` → Required authorization key
- **Behavior:**  
  - Finds the requested song and prints lyrics line by line into chat  
  - If a song is already playing, the bot will refuse until stopped  

---

#### `!echo "TEXT" SECRET_KEY`
- **Purpose:** Echoes text through the bot
- **Arguments:**
  - `TEXT` → The message you want the bot to say
  - `SECRET_KEY` → Required authorization key
- **Behavior:**  
  - Bot sends the specified text into chat as if it were speaking  

---

#### `!stop SECRET_KEY`
- **Purpose:** Stops the currently playing song
- **Arguments:**
  - `SECRET_KEY` → Required authorization key
- **Behavior:**  
  - Immediately halts lyric playback  
  - If no song is playing, the bot will notify you  

---

#### `!help`
- **Purpose:** Displays help information
- **Arguments:** None
- **Behavior:**  
  - Sends a private message (`/msg`) to the requesting player  
  - Lists all available commands and their usage  

---

### 🔒 Security Notes
- Commands requiring `SECRET_KEY` ensure only authorized users can control the bot
- The key can be rotated via console commands for added security
- Unauthorized attempts are logged and ignored

---

### ⚙️ Example Commands
```text
!song "Tokyo" GPL6
!echo "Hello world!" GPL6
!stop GPL6
!help
