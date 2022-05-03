# Visual Studio

## Check compiler version
[Finding version of Microsoft C++ compiler from command-line (for makefiles)](https://stackoverflow.com/questions/1233312/finding-version-of-microsoft-c-compiler-from-command-line-for-makefiles)

```bash
cd C:\Program Files (x86)\Microsoft Visual Studio\2019\Community\VC\Tools\MSVC\14.29.30133\bin\Hostx64\x64
cl.exe
```

```
Microsoft (R) C/C++ Optimizing Compiler Version 19.29.30139 for x64
Copyright (C) Microsoft Corporation.  All rights reserved.

usage: cl [ option... ] filename... [ /link linkoption... ]
```

## Compile C++ file
[visual studio compiler how to specify the include path to build cpp](https://stackoverflow.com/questions/31395929/visual-studio-compiler-how-to-specify-the-include-path-to-build-cpp)

```bash
cl.exe /I "<include_directory_path>" <cpp_file.cpp>
```

## Check file differences
[Compare two files in Visual Studio](https://stackoverflow.com/questions/13752998/compare-two-files-in-visual-studio)

Call out command window: <kbd>Ctrl</kbd> + <kbd>Alt</kbd> + <kbd>A</kbd>

And then:

```bash
Tools.DiffFiles File1 File2
```
