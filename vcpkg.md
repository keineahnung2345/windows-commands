# vcpkg

## install from source
```sh
mkdir C:/src
cd C:/src
git clone https://github.com/microsoft/vcpkg
cd vcpkg
bootstrap-vcpkg.bat
```

## update
```sh
cd C:/src/vcpkg
git pull
bootstrap-vcpkg.bat
```

## upgrade installed packages

```sh
vcpkg upgrade --no-dry-run
```
