Convert to webm
```
ffmpeg -i test.mp4 -c:v libvpx -crf 15 -b:v 1M -c:a libvorbis test.webm
```
Convert to ogv
```
ffmpeg -i test.mp4 -codec:v libtheora -qscale:v 6 -codec:a libvorbis -qscale:a 6 test.ogv
```