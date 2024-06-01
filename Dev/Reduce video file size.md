```
ffmpeg -i input.mp4 -vcodec libx265 -crf 28 output.mp4
```

<10mb
```
ffmpeg -i input.mp4 -vcodec libx265 -crf 34 output.mp4
```

> a reasonable range for H.265 may be 24 to 30. Note that _lower_ CRF values correspond to _higher_ bitrates, and hence produce _higher_ quality videos.

