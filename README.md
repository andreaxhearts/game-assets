### Extract Frames
You can extract frames from an animated webp file with this command:
```
magick input.webp -coalesce -define webp:lossless=true frame-%03d.webp
```
