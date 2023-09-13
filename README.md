## build container:

 ```bash
podman build -f Dockerfile-rocky9-systemd -t rockylinux-systemd-desktop:9 .
 ```

## run container:
  ```bash
podman run -itd -p 3333:3389 --name  rockylinux9-s-d rockylinux-systemd-desktop:9
 ```

## get into the container environment
```bash
podman exec -it rockylinux9-s-d bash
 ```
### create user and start xrdp
```bash
adduser NAME
passwd NAME

systemctl start xrdp
```

Now the remote desktop is available on port 3333.
