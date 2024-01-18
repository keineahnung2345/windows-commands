# Hyper-V

## Copy file from host to VM
```sh
Copy-VMFile "vmname" -SourcePath "vm_file_path" -DestinationPath "host_destination_path" -CreateFullPath -FileSource Host
```

## Make VM full screen

[How to adjust virtual machine display resolution to adapt to full screen](https://learn.microsoft.com/en-us/answers/questions/341631/how-to-adjust-virtual-machine-display-resolution-t)

```sh
Set-VMVideo -VMName "vmname" -HorizontalResolution 1920 -VerticalResolution 1080 -ResolutionType Single
```

