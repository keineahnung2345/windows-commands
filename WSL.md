# WSL

## WSL command not recognized
[`wsl` command not recognized after enabling WSL2](https://github.com/MicrosoftDocs/WSL/issues/405)
```bat
wsl -s Ubuntu-18.04 2
```

## Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.
[Please enable the Virtual Machine Platform Windows feature and ensure virtualization is enabled in the BIOS.](https://github.com/microsoft/WSL/issues/5363#issuecomment-687663915)
```bat
bcdedit /set hypervisorlaunchtype auto
```
