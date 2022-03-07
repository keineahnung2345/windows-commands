# Powershell

## Copy recursively

[Copy items from Source to Destination if they don't already exist](https://stackoverflow.com/questions/25916197/copy-items-from-source-to-destination-if-they-dont-already-exist)

[How to robocopy subfolders with content](https://stackoverflow.com/questions/24385239/how-to-robocopy-subfolders-with-content)

```bash
robocopy /xc /xn /xo <src_dir> <dst_dir> /E
```

`/xc`: exclude changed, `/xn`: exclude newer, `/xo`: exclude older, `/E`: copy subdirectories, including empty ones

## Timer
[How do I measure execution time of a command on the Windows command line?](https://stackoverflow.com/questions/673523/how-do-i-measure-execution-time-of-a-command-on-the-windows-command-line)
```bat
Measure-Command {your-command}
```

## Ssh server

[SSH Server on Windows 10](https://virtualizationreview.com/articles/2020/05/21/ssh-server-on-windows-10.aspx)

To install ssh server, go to Settings > Apps > Optional features > Add a feature > OpenSSH Server > Install.

To start ssh server:
```bat
Start-Service sshd
Get-Service sshd
```

To send/receive file:
```bat
scp <user_name>@<ip_address>:<file_path_relative_to_user_home_dir> .
```

Note: this can be used in Windows-to-Windows file transfer.

Ex:

```bat
scp *.mp4 user@192.168.1.1:C:\Users\user\Downloads
```

## Error response from daemon: open \\.\pipe\docker_engine_linux: The system cannot find the file specified.

[Error response from daemon: open \\.\pipe\docker_engine_linux: The system cannot find the file specified.](https://github.com/docker/for-win/issues/4495)

If using:
```bat
docker ps
```

generates the following error:
```
Error response from daemon: open \\.\pipe\docker_engine_linux: The system cannot find the file specified.
```

It can be solved by:
```bat
Net stop com.docker.service
Net start com.docker.service
```
