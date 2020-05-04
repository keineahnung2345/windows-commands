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

## cd to UNC path
[Browse an UNC path using Windows CMD without mapping it to a network drive](https://superuser.com/questions/282963/browse-an-unc-path-using-windows-cmd-without-mapping-it-to-a-network-drive)
```bat
pushd \\network_host\a\network\path
:: go back
popd
```
