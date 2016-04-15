# sshfs-open

A simple script to mount and un-mount remote directories

### Usage:

```
$ sshfs-open host:/some/directory/to/open [command]
```

### Example:

```
$ ./sshfs-open dev@server.com:/some/dir 
Mounted ./tmp/dev@server.com:,some,dir
Press [CTRL+C] to exit
```

To run a command on the mounted directory, pass the commands and arguments after the remote directory:

```
# Open the mounted directory with atom
$ ./sshfs-open dev@server.com:/some/dir atom 
Mounted ./tmp/dev@server.com:,some,dir
Press [CTRL+C] to exit
```

Once you press CTRL+C, the mounted directory will be unmounted, and any child processes will be killed (if you passed a command).
