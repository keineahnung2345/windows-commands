# windows-commands
Some useful windows commands

## Set environment varialbe
```bat
setx <env_var_name> <env_var_value>
```

## Comment
[批次檔中特殊符號@、::、%的用途](https://ithelp.ithome.com.tw/articles/10055209)
```bat
REM this is comment
:: this is another comment
```

## Show file structure
```bat
tree /f
```
use /f to show files

## Search for large files
[4 Ways To Find Large Files In Windows 10](https://helpdeskgeek.com/how-to/find-the-largest-files-on-your-computer/)

Find all files larger than 1GB and write their paths to the file "/path/to/largefiles.txt".

```bat
forfiles /S /M * /C “cmd /c if @fsize GEQ 1073741824 echo @path > "/path/to/largefiles.txt"
```

## Merge text files
[How to Merge Text (.Txt) Files in Command Prompt](https://www.wikihow.com/Merge-Text-(.Txt)-Files-in-Command-Prompt)
```bat
copy *.txt "merged.txt"
```

## Create a symbolic link
```bat
mklink /d <link_name> <target>
```

## cd to UNC path
[Browse an UNC path using Windows CMD without mapping it to a network drive](https://superuser.com/questions/282963/browse-an-unc-path-using-windows-cmd-without-mapping-it-to-a-network-drive)
```bat
pushd "\\network_host\a\network\path"
:: go back
popd
```

## unhide folder

[I can't unhide my folders using folder options](https://answers.microsoft.com/en-us/windows/forum/windows_7-files/i-cant-unhide-my-folders-using-folder-options/dcaffb47-4032-4d27-95b5-c1b13618bfeb)

```bat
attrib -h -s  /s /d "/path/to/folder"
```

## 7zip: exclude file lists and specific type of files
[7-zip - how to use command line to include/exclude large list of files](https://superuser.com/questions/657859/7-zip-how-to-use-command-line-to-include-exclude-large-list-of-files)

[Add to a 7-Zip archive: How to exclude certain file types/extensions?](https://superuser.com/questions/185135/add-to-a-7-zip-archive-how-to-exclude-certain-file-types-extensions)
```bat
7z.exe a Archive.7z . -r -x!*.avi -x!*.mp4 -x!*.pcd -x!*.ply  -xr@"merged.txt"
```
