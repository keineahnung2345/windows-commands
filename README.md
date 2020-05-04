# windows-commands
Some useful windows commands

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

## cd to UNC path
[Browse an UNC path using Windows CMD without mapping it to a network drive](https://superuser.com/questions/282963/browse-an-unc-path-using-windows-cmd-without-mapping-it-to-a-network-drive)
```bat
pushd "\\network_host\a\network\path"
:: go back
popd
```
