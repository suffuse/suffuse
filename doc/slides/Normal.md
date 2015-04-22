# Suffuse for Normals

--

## Images
- Open /a/pic.jpg
- It's ridiculously large, run JPEGmini
- minified image replaces the original
- initial call to open succeeds!

--

## Audio
- Attempt to open /a/song.mp3
- it doesn't "typecheck" (exist)
- suffuse searches for an "implicit conversion"
- /a/song.flac exists, config defines flac->mp3
- mp3 is generated and cached
- initial call to open succeeds!

--

### Torrents
 - Given a large index of (legal) torrent files
 - virtually giant filesystem offers every file
 - Access file, it is torrented and cached
 - initial call to open succeeds!

--

### Lyrics
 - Given a means of retrieving song lyrics such as [beets](http://beets.radbox.org/)
 - Populate the lyrics metadata when the song is played
 - Actually populate the whole album at that point
 - And album art, musicbrainz, etc.

--

## Archives
- Given the existence of /s/foo.zip
- cd to /s/foo, find the exploded contents
- change something, /s/foo.zip is updated
- /s/foo.jar is there too, as is /s/foo.tgz, etc.
