Commands for YT-DLP
Notes and Commands for CMD application YT-DLP

###To download a high-quality MP3 with the artist and cover art embedded using yt-dlp

  Command for a playlist:
  (To download an entire playlist, use this command, replacing [PLAYLIST_URL] with the playlist link.)
  
  ```yt-dlp -x --audio-format mp3 --audio-quality 0 --embed-thumbnail --add-metadata --yes-playlist --parse-metadata "%(artist)s" -o "%(playlist_index)s - %(artist)s - %(title)s.%(ext)s" "[PLAYLIST_URL]"```
  
  Command breakdown:  
      -x: Tells yt-dlp to extract only the audio from the video.
      --audio-format mp3: Converts the extracted audio to an MP3 file.
      --audio-quality 0: Fetches the highest possible MP3 quality (VBR).
      --embed-thumbnail: Embeds the video's thumbnail as the album art in the MP3 file.
      --add-metadata: Writes metadata like title and album information to the MP3 file.
      --parse-metadata "%(artist)s": Instructs yt-dlp to parse the video's creator or channel name and set it as the "artist" metadata.
      -o "%(artist)s - %(title)s.%(ext)s": Sets the output filename format. This command saves the file as "Artist - Title.mp3". For playlists, it adds %(playlist_index)s to number the tracks.
      --yes-playlist: Explicitly confirms you want to download an entire playlist. 
