# 💸 Omanges Stream Tax Extensions for Streamer.bot
  
This system tracks streamer viewers’ tax payments, automatically increases redeem costs, shows leaderboards, and allows resetting tax data — all directly in your Twitch chat.

---

## 💡 Features

* 📈 Automatic percentage increase of redeem cost on each Stream Tax payment  
* 📊 Tax leaderboard showing top Stream Tax payers  
* 🧾 Individual tax paid and rank query command  
* 🔄 Reset Stream Tax data with timestamped backups  
* ⚙️ Easy configuration and setup with folder-based logging  
* ✅ Works with Streamer.bot v0.2.8+ and Twitch channel points  

---

## 🧰 Commands / Actions

| Command / Action        | Function                                   |
|------------------------|--------------------------------------------|
| Stream Tax Redeem       | Handles channel point redemptions and increases cost |
| `!taxboard` / `!taxleaderboard` | Shows the top 5 (configurable) tax payers with ranks and amounts  |
| `!taxpaid`       | Displays how much tax a user has paid and their rank |
| `!taxreset`             | Archives current data, clears log, and resets redeem cost |

---

## 🗂 Folder Structure

These extensions store logs in:
```
StreamerBot
└── Omanges Extensions
  └── Stream Tax
    ├── stream_tax.txt # Main tax log
    └── stream_tax_rst_MM-dd-yy.txt # Timestamped backups on reset
```

The scripts auto-create folders if missing.

---

Got it! Here's the updated **⚙️ Installation** section with that info integrated:

---

## ⚙️ Installation

1. **Import the Extension**

   * Download the `DynamicStreamTax.sb` file from this repository.
   * In Streamer.bot, go to the **Actions** tab.
   * Click the **Import** button and select the `DynamicStreamTax.sb` file.
   * This will automatically import all necessary actions, variables, and folders.

2. **Set Up Channel Point Reward**

   * Create or use a channel point reward for “Stream Tax” with a starting cost (default 25).
   * Make sure its name or ID matches what's expected by the imported actions (adjust if needed).

3. **Connect Triggers**

   * Add chat command triggers for:

     * `!taxboard` / `!taxleaderboard`
     * `!taxpaid`
     * `!taxreset`
   * Connect the Stream Tax redeem action to the appropriate reward redemption trigger.

4. **Folder Structure**

   * The system will automatically create and manage the `Omanges Extensions/Stream Tax/` folder structure for logs.

5. **Permissions**

   * Ensure Streamer.bot has permission to read/write files and modify channel point reward costs through your Twitch integration.

---

## 🧪 Example Output

**Stream Tax Redeem**:  
`@username has paid 25 in Stream Tax!`

**Leaderboard (`!taxboard`)**:  
`💰 Top 5 Stream Tax Payers: #1: UserA (120) | #2: UserB (95) | #3: UserC (80) | #4: UserD (60) | #5: UserE (45)`

**Tax Paid (`!taxpaid username`)**:  
`@username, you have paid 120 in Stream Tax and you're ranked #1!`

**Reset (`!taxreset`)**:  
`Stream Tax data has been reset. Previous data saved as stream_tax_rst_08-04-25.txt.`

---

## 🚧 Error Handling

The scripts handle cases where:

* Log files or folders are missing (auto-create or warn)  
* No tax data exists yet (messages to chat)  
* Invalid or unknown users request tax info  
* Duplicate backups avoided on reset

---

## ✏️ Customization Tips

* Adjust the percentage increase of redeem cost in the Redeem action’s settings.  
* Change leaderboard size or message formats in the leaderboard action.  
* Modify default cost reset value by adjusting your channel point reward manually or via Streamer.bot.  
* Use the log files to track Stream Tax history or build custom reports.

---

## 🔧 Requirements

* **Streamer.bot v0.2.8 or newer**  
* Twitch bot integration with channel point rewards enabled 

---

## 📞 Support

Join the [SIDOR Community Discord](https://discord.gg/2pcKpMrxdD) to get help, suggest features, or just hang out with other creators using this system.

---

## 💬 Feedback or Contributions

Want to suggest improvements, report bugs, or add features?

* Open a pull request  
* Create an issue on GitHub  
* Or fork the repo and customize it yourself  

Check out [GitHub Issues](https://github.com/realOmanges/DynamicStreamTax/issues) for open requests and discussions.

---

## 👤 Author

**Omanges**  
🟣 Twitch: [twitch.tv/omanges](https://twitch.tv/omanges)  
💬 Join the [SIDOR Community Discord](https://discord.gg/2pcKpMrxdD)  

---

## 📄 License

MIT License  
You’re free to use, modify, and share this—just give credit.
