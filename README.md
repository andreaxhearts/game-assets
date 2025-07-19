### Extract Frames
You can extract frames from an animated webp file with this command:
```
magick input.webp -coalesce -define webp:lossless=true ./frames/frame-%03d.webp
```

### Create Animation
ffmpeg can be used to create webp animations. Example:
```
ffmpeg -i frame-%03d.webp -c:v libwebp_anim -lossless 1 -framerate 29.970 anim.webp
```
`-start_number 1` can be used to change the starting frame. This option goes before the `-i`input.
