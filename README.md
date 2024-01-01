# DiscordMusicDownloaderBot

## Overview
DiscordMusicDownloaderBot is a very simple Discord bot that allows users to easily download and tag music directly to a shared location. It utilizes the discord.py library for interacting with the Discord API, as well as other libraries such as youtube_search, pytube, and pydub for handling YouTube searches and audio processing. Additionally, the bot leverages MusicBrainz Picard to enhance the downloaded audio files by automatically clustering and tagging them with accurate metadata.

<div style="text-align: center;">
  <div style="display: inline-block; margin-right: 20px;">
    <p>Using !search to download and tag .mp3 files:</p>
      <img src="https://github.com/JakeTurner616/DiscordMusicDownloader/blob/0de4b8953c76e2e0d03093a4b071cba5b76e79ff/docs/demo0.gif" alt="/search demo">


  </div>

## Binary Downloader
[musicbrainz-binary-downloader.py](https://github.com/JakeTurner616/DiscordMusicBot/blob/main/musicbrainz-binary-downloader.py) can be optionally used to automate the process of downloading the latest MusicBrainz Picard binary from the official download page and verifies its integrity using an MD5 hash.

## Features
1. **YouTube Search:** Users can search for YouTube videos using the `!search` command. The bot will display the top 5 search results, and users can select a video by reacting to the message with a corresponding number emoji.

2. **Audio Conversion:** After selecting a video, the bot downloads the audio using pytube, converts it to MP3 format using pydub, and utilizes MusicBrainz Picard to cluster related files and add audio file metadata.

## Setup Musicbrainz-Picard for Automatic file managment

To setup automatic file managment in Picard, begin by launching the MusicBrainz application binary. Upon the initial launch, a `Config.ini` file is generated in the `/Musicbrainz-Picard` directory within the working prohject directory. To customize file movement preferences, navigate to the MusicBrainz `Config.ini` and modify the following values according to your preferences to allow for a destination folder to be set to a network share, or music library folder:

./MusicBrainz-Picard/Config.ini:
```Config.ini
move_files=true
move_files_to=C:\\Users\\jaked\\Music
move_additional_files=true
move_additional_files_pattern=*.jpg *.png
```


## TOS and legality Disclaimer
DiscordMusicDownloaderBot is distributed on an "as-is" basis, and the user assumes full responsibility for its usage. While the bot facilitates the download and tagging of audio content from YouTube videos, users are unequivocally advised to adhere to all relevant legal regulations pertaining to content acquisition and distribution of non-copyleft media. Users are strongly encouraged to thoroughly review and comply with the terms and conditions of all required libraries, ensuring that their usage aligns with legal and subjective moral standards. DiscordMusicDownloaderBot is strictly intended for personal non-commercial use, and users are explicitly prohibited from engaging in any activities that involve the commercial exploitation or monetization of any of the bot's functionalities, particularly concerning the re-distribution of copyrighted, or proprietary music.

## License
This bot is distributed under the [GNU General Public License v3.0](https://github.com/JakeTurner616/DiscordMusicBot/blob/main/LICENSE).
