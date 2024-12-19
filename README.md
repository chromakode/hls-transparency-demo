# An attempt at HLS with transparent background

Unfortunately, the resulting video doesn't appear to have alpha. My best guess is this is a limitation of the mp4 container.

```
ffmpeg -c:v libvpx -i ./soccer1.webm -t 3 -c:v libvpx-vp9 -vf "format=yuva420p" -f hls -hls_segment_type fmp4 tpv.m3u8
```
