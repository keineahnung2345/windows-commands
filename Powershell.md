# Powershell

## Copy recursively

[Copy items from Source to Destination if they don't already exist](https://stackoverflow.com/questions/25916197/copy-items-from-source-to-destination-if-they-dont-already-exist)

[How to robocopy subfolders with content](https://stackoverflow.com/questions/24385239/how-to-robocopy-subfolders-with-content)

```bash
robocopy /xc /xn /xo <src_dir> <dst_dir> /E
```

`/xc`: exclude changed, `/xn`: exclude newer, `/xo`: exclude older, `/E`: copy subdirectories, including empty ones
