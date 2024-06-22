Convert to webm
```
ffmpeg -i test.mp4 -c:v libvpx -crf 15 -b:v 1M -c:a libvorbis test.webm
```

Convert to ogv: generally preserve resolution
```
ffmpeg -i input.mp4 -q:v 6 -q:a 6 output.ogv
```
resize to 720p tall while keeping aspect ratio
```
ffmpeg -i input.mp4 -vf "scale=-1:720" -q:v 6 -q:a 6 output.ogv
```

https://docs.godotengine.org/en/stable/tutorials/animation/playing_videos.html#balancing-quality-and-file-size