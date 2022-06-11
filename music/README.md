Allows you to play music through a Discord voice channel.

# How to use
1. Copy mbot.py and music_cog.py (OR mbot, music_cog2.py, & npformater.sh) to same folder
   - music_cog2.py has some custom features, WIP  
2. Copy your bot token to tok.en in same folder
3. Run mbot.py to start bot

# Dependencies for Linux users (I use a RPi):
1. the discord lib requires python 3.4 or better
2. install ffmpeg with apt: ```apt-get install ffmpeg```
3. install ffmpeg support for python with: ```pip install ffmpeg```
4. install discord for python with: ```pip install discord```
5. install voice_client support for python with: ```python -m pip install -U discord.py[voice]```

# Windows users:
I'm not sure what is different in Windows other than installing and referencing FFmpeg. I run using the powershell and could probably keep alive with taskscheduler if I didn't already have the RPi solution:
- The filepaths *must* all be changed to windows format, i.e. `C:\Users\YOUR-WINDOWS-USERNAME\Desktop\seabe\music_bot.py`
- Install Python for Windows: https://github.com/bclittleua/SEA-BE-22/tree/main/instructions
- Download and install FFmpeg here, note the install path: https://www.ffmpeg.org/download.html
- Do steps 3, 4, and 5 for linux users (above) from your Windows Command Prompt.


# Set up your bot at https://discord.com/developers/applications/  
- Make sure your bot is private, toggle Public to OFF
- No intents required, disable them in bot settings
- The only scope required for OAuth2 is 'bot'
- Give your bot admin permission to make things easy, permissions=8
- Add the bot to Discord server with https://discord.com/api/oauth2/authorize?client_id=0000000000000&permissions=8&scope=bot
  - You must replace the `0000000000000` with your own client_id!