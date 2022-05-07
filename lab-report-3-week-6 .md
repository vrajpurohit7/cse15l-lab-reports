# *Title*

## Streamlining ssh Configuration:
Logging into the remote server from the local machiene can be really fustrating when we need to type such long lines of code:

`$ ssh cs15lsp22amx@ieng6.ucsd.edu`

Instead, if we are able to login in with just typing `ssh ieng6` why would we trouble ourselves unnecessarily?

So, here's how we can do it:

1. In your terminal, try opening `~/.ssh/config` (on your computer, creating it if it doesn’t exist), and add the following lines of code:
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22zzz (use your username)
```
![Image](3-host.png)

2. Then try this command: `ssh ieng6`. 

If things are set up correctly, this should use the key and log you in with the username you specified using your public key.

If this doesn’t work, you can try adding a line to explicitly refer to your id_rsa file:
```
Host ieng6
    HostName ieng6.ucsd.edu
    User cs15lsp22zzz (use your username)
    IdentityFile ~/.ssh/id_rsa
 ```
Note that paths may look a little different on Windows, they may use \ instead of / for instance. 

In the end it's supposed to look like so:

![Image](3-ssh_ieng6.png)
### `scp` a file into remote server using just `ssh ieng6`:
Now when you create a file on your local computer and want to copy it to the remote one, do the following:

1. Create a `.txt` file and `scp` it to the remote server.
2. Login into the remote server using `ssh ieng6` command.
3. Type `ls` to see the contents on the server.

You should see your file there:

![Image](3-scp.png)

## Set up Github Access from ieng6:

## Copy Whole Directories with `scp -r` :