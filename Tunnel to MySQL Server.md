# Access MySQL Database via Tunnel

`ssh -f -N -L 33061:localhost:3306 root@carlogaza.com`

then, connect via mysql console :

`mysql -h 127.0.0.1 -P 33061 -u root -p`
