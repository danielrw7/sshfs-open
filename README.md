# sshfs-open

A simple script to mount and un-mount remote directories

### Setup:
1. Install [sshfs](https://github.com/libfuse/sshfs).
2. Run `git clone https://github.com/danielrw7/sshfs-open.git`
3. If you want to add `sshfs-open` to your PATH, add this to your bashrc:
```
export PATH=$PATH:/path/to/sshfs-open
```

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
