# How to mount Windows Sharing Folder on Linux Terminal

```bash
mkdir ~/Windows-Share
sudo mount.cifs //192.168.1.100/Public/data /home/carlogaza/Windows-Share -o uid=1001,gid=1001
```

That command wil mount folder `data` on Windows (192.168.1.100) to directory `/home/carlogaza/Windows-Share` and give permission to userid 1001 and groupid 1001. To check userid and groupid, you can use command `id <username>`.
