# environment
Everything needed for a smooth coding experience

## mobile-browser
Dockerfile to emulate opera-mini on the desktop

Usage:

```docker run --rm -v /tmp/.X11-unix:/tmp/.X11-unix:ro -e DISPLAY=unix$DISPLAY derfranz/opera-mini```

To include a different midlet (.jar), just mount Volume from Dockerfile to the folder with the .jar file.
