# Setup passwordless SSH on Linux

1. Create Authentication Keys on Computer 1 : `ssh-keygen`
2. Create SSH Directory on Computer 2 : `ssh user@computer2 'mkdir -p .ssh'`
3. Copy public keys Computer 1 to Computer 2 : `cat .ssh/id_rsa.pub | ssh user@computer2 'cat >> .ssh/authorirez_keys'`
4. Set permission on Computer 2 : `ssh user@computer2 'chmod 700 .ssh && chmod 640 .ssh/authorized_keys'`

## Error and Resolution

1. Agent admitted failure to sign using the key.
Just run `ssh-add` on Computer 1.
2. Could not open a connection to your authentication agent.
Just run `eval $(ssh-agent)` then `ssh-add` on Computer 1.
