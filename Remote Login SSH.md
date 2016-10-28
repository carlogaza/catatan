# Remote Login SSH with Reverse SSH

`ssh -f -N -R 4444:localhost:22 root@carlogaza.com`

so you can remote from server carlogaza.com with this command :

`ssh -p 4444 -t device_user@localhost`
