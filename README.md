spotify-controller
==================
A way of managing Spotify from the command line.

This is my Todo and feature list until it is all done, keeping it here
as a RFC.

I'm looking to use this mainly so that I can control Spotify through
[Quicksilver] the same way I could control iTunes. The client is going
to be written in [Go] using the [libspotify], so I have a project to
learn go with.

[Quicksilver]: http://qsapp.com/
[Go]: http://golang.org/
[libspotify]: https://developer.spotify.com/technologies/libspotify/

# Features

- Basic functions:
  - [ ] Play
  - [ ] Pause
  - [ ] Play previous song in playlist
  - [ ] Play next song in playlist
  - [ ] Toggle shuffle
  - [ ] Toggle repeat
- Song selection
  - [ ] Start playing a song from song id
  - [ ] Queue a song from a song id
  - [ ] Add the last song queued at the top of the current list
  - [ ] Select which playlist is the current one
- Song search
  - [ ] Search for songs and return a list of songs with Spotify ids
  - [ ] Search for songs in currently selected playlist

# CLI interface

```
spotify-client help
    play - If the current song is paused or stopped start playing
    play <song id> - Start playing <song id> now
    queue [top] <song id> [<song id>, ...]
    playlist - Name and id of currently playing playlist
    playlist search [search term] - List all playlists filtered by search term
    playlist list [playlist id] - List all songs in playlist or current pl
    playlist songs [playlist id] [search term] - Filter songs in playlist
                                                 by search term
    playlist <playlist id> - Start playing the given playlist
    pause - Pause the currently playing song
    plause - Toggle play/pause
    stop - Stop the currently playing song
    next - Play next song in playlist
    prev - Play previous song in playlist
    shuffle [on|off] - Toggle shuffle
    repeat [on|off] - Toggle repeat
```
