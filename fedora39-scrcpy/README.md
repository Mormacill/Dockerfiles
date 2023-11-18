## build container:

 ```bash
podman build -f Dockerfile-fedora39-scrcpy -t fedora39-scrcpy:39 .
 ```

## run container:
  ```bash
podman run -it --rm --name fedora39-scrcpy -v /tmp/.X11-unix/:/tmp/.X11-unix/ -e DISPLAY=$DISPLAY -v /dev:/dev fedora39-scrcpy:39
 ```
