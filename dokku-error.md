# DOKKU ERROR NOTES
___

## Dokku Push Error
This error occurs when I try to deploy new application on dokku.
```
$ git push dokku master

fatal: 'app-name' does not appear to be a git repository
fatal: Could not read from remote repository.

Please make sure you have the correct access rights
and the repository exists.
```
This error because dokku cannot validate the computer public key, or dokku has duplicate public key on dokku authorized_keys. You are prohibited to add ssh keys manually on dokku. You must use command `dokku ssh-keys:add key_name /path/to/keys.pub`. To resolve this error, you must delete the authorized_keys on dokku user and add new key using dokku command.
```
$ sudo rm -rf /home/dokku/.ssh/authorized_keys
$ dokku ssh-keys:add carlogaza /home/carlogaza/.ssh/id_rsa.pub
```
Change `carlogaza` with anything and change the `/home/carlogaza/.ssh/id_rsa.pub` with the path of your public key.
And this will solve your problem. :)
