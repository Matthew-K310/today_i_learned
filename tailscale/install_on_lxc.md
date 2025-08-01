To allow Tailscale to be installed and run on an unpriviledged LXC, add this
to `/etc/pve/lxc/<id>.conf`

```
"/etc/pve/lxc/112.conf"

lxc.cgroup2.devices.allow: c 10:200 rwm
lxc.mount.entry: /dev/net/tun dev/net/tun none bind,create=file
```
