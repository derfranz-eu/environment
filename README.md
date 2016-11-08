# environment
Everything needed for a smooth coding experience

## mobile-browser
Dockerfile to emulate opera-mini on the desktop

Usage:

```docker run --rm -v /tmp/.X11-unix:/tmp/.X11-unix:ro -e DISPLAY=unix$DISPLAY derfranz/opera-mini```

To include a different midlet (.jar), just mount Volume from Dockerfile to the folder with the .jar file.

## ssdb-master-alpine
Dockerfile for a minimal [ssdb-master](http://ssdb.io/) image (current version 1.9.4).

Usage:

For test purposes you could run it without persisting the volume

```docker run --rm --name ssdb -p 8888:8888 derfranz/ssdb-master-alpine ```

To keep the data over container destructions you should mount the volume like

```docker run -d --name ssdb -p 8888:8888 -v /var/lib/ssdb:/var/lib/ssdb derfranz/ssdb-master-alpine ```

