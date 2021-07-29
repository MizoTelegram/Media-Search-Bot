# Media-Search-Bot [Modified](https://github.com/Mahesh0253/Media-Search-bot)

## Features
<details>
  <summary><b>Show Features</b></summary>
<br/>

* Imdb posters for autofilter.
* Custom captions for your files.
* Index command to index all the files in a given channel (No USER_SESSION Required).
* Ability to Index Public Channels without being admin.
* Support Auto-Filter (Both in PM and in Groups)
* Once files saved in Database , exists until you manually deletes. (No Worry if post gets deleted from source channel.)
* Added Force subscribe (Only channel subscribes can use the bot)
* Ability to restrict groups(AUTH_GROUPS)

</details>

---

## Variables
<details>
  <summary><b>See Required Variables</b></summary>
<br/>

* `BOT_TOKEN`: Create a bot using [@BotFather](https://telegram.dog/BotFather), and get the Telegram API Token.
* `API_ID`: Get this value from [telegram.org](https://my.telegram.org/apps)
* `API_HASH`: Get this value from [telegram.org](https://my.telegram.org/apps)
* `CHANNELS`: Username or ID of channel or group. Separate multiple IDs by space
* `ADMINS`: Username or ID of Admin. Separate multiple Admins by space
* `DATABASE_URI`: [mongoDB](https://www.mongodb.com) URI. Get this value from [mongoDB](https://www.mongodb.com). For more help watch this [video](https://youtu.be/nj-lJfkgb6w)
* `DATABASE_NAME`: Name of the database in [mongoDB](https://www.mongodb.com). For more help watch this [video](https://youtu.be/nj-lJfkgb6w)

</details>

<details>
  <summary><b>See Optional Features</b></summary>
<br/>

* `OMDB_API_KEY`: OMBD_API_KEY to generate imdb poster for filter results.Get it from [omdbapi.com](http://www.omdbapi.com/apikey.aspx)
* `CUSTOM_FILE_CAPTION` : A custom caption for your files. You can format it with file_name, file_size, file_caption.(supports html formating)
Example: `<b>Join [tgbotsProject](https://t.me/tgbotsProject) for more useful bots</b>\n\n<code>{file_name}</code>\nSize{file_size}\n{file_caption}.`
* `AUTH_GROUPS` : ID of groups which bot should work as autofilter, bot can only work in thease groups. If not given , bot can be used in any group.
* `COLLECTION_NAME`: Name of the collections. Defaults to Telegram_files. If you going to use same database, then use different collection name for each bot
* `CACHE_TIME`: The maximum amount of time in seconds that the result of the inline query may be cached on the server
* `USE_CAPTION_FILTER`: Whether bot should use captions to improve search results. (True/False)
* `AUTH_USERS`: Username or ID of users to give access of inline search. Separate multiple users by space. Leave it empty if you don't want to restrict bot usage.
* `AUTH_CHANNEL`: ID of channel. Without subscribing this channel users cannot use bot.
* `START_MSG`: Welcome message for start command.

</details>

---

## Installation

<details><summary><b>Deploy to Heroku</b></summary>
<p>
<br>
<a href="https://heroku.com/deploy?template=https://github.com/ZauteKm/Media-Search-Bot">
  <img src="https://www.herokucdn.com/deploy/button.svg" alt="Deploy">
</a>
</p>
</details>

<details>
  <summary><b>Deploy in your VPS</b></summary>
<br/>

```bash
# Create virtual environment
python3 -m venv env

# Activate virtual environment
env\Scripts\activate.bat # For Windows
source env/bin/activate # For Linux or MacOS

# Install Packages
pip3 install -r requirements.txt

# Edit info.py with variables as given below then run bot
python3 bot.py
```
Check [`sample_info.py`](sample_info.py) before editing [`info.py`](info.py) file

</details>

---

## Admin Commands
<details>
  <summary><b>See Commands</b></summary>
<br/>

```
channel - Get basic infomation about channels
total - Show total of saved files
delete - Delete file from database
index - Index all files from channel.
logger - Get log file
```

</details>

---

## Tips
- You can use `|` to separate query and file type while searching for specific type of file. For example: `Avengers | video`
- If you don't want to create a channel or group, use your chat ID / username as the channel ID. When you send a file to a bot, it will be saved in the database.

---

## Thanks to 
• [Pyrogram](https://github.com/pyrogram/pyrogram)
• Original [Repo](https://github.com/Mahesh0253/Media-Search-bot)

---

## License
Code released under [The GNU General Public License](LICENSE).
