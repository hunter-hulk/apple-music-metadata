<h1 align="center">apple-music-metadata</h1>

## A simple typscipt package for scraping metadata for apple music playlists and songs

# Installation

```
npm install apple-music-metadata
```

#  Usage

## Song data
```ts
import getSong from "apple-music-metadata";
const songLink = "https://music.apple.com/us/album/example/1541902791?i=1541903021";
const song = await getSong(songLink); 
returns Promise{RawAppleSong {
    type: 'song'
    artist: string, 
    title: string
};}
```
## Playlist data 
```ts
import getSong from "apple-music-metadata";
const playlistLink = "https://music.apple.com/us/playlist/example/06496496e1292466839207";
const playlist = await getPlaylist(playlistLink); 
returns Promise{RawApplePlaylist{
    name: string
    type: 'playlist'|'album'
    author: string
    tracks: { artist: string, title: string }[]
}}
```

## Auto 
```ts
import autoGetApple from "apple-music-metadata";
const link = "exapmle" // song ablum or playlist link
returns RawAppleSong|RawApplePlaylist
```

use the type key to sort return