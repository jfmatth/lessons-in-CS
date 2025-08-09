# Windows

- Use windows Terminal for all access to command-line stuff
- Powershell should be the default

## Install latest powershell and UV

UV is the preferred method to use Python

```
winget install microsoft.powershell
winget install astral.uv
```

## Make a folder on your system to keep all your projects
```
mkdir projects
cd projects
```



# Linux on Windows

## WSL (Windows Subsystem for Linux)
https://learn.microsoft.com/en-us/windows/wsl/install

## Installation
- This is already installed and tested.
- WSL 2 is running

## Launching and Using

From Terminal, choose WSL distribution "Ubunut 24.04 LTS"

From here, it's just linux, with a few special exceptions for Windows users:
- The windows filesystem is mounted at ```/mnt/c/``` is your C: from Windows
- The WSL filesystem is in Windows Explorer as a mounted system called Linux
- ```localhost``` on Windows maps to the WSL localhost (if WSL is running)
    - This makes most localhost / 127.0.0.1 / 0.0.0.0 applications work from a Windows browser
- VSCode can be launched from any folder by ```code```.
    - Sometimes there is a mismatch of WSL version and Windows version during upgrades to VSCode, if that happens, close down WSL and try again.

## C programs on WSL
Since WSL is a true version of Linux, installing it with ```apt`` should be standard

### Install GCC
```
sudo apt install gcc -y
```

### Hello World
- Create a file in VSCode
    ```
    code main.c
    ```

- Add the following program and Save it (Ctrl-W + Y)
    ```
    #include <stdio.h>

    int main() {
    printf("Hello, World!");
    return 0;
    }
    ```

- Compile it
    ```
    gcc main.c -o hello
    ```

- Run it
    ```
    ./hello
    ```
    (unlike Windows, in Linux, applications in the folder you're in need to have the ```./``` prepended)


### Cool links
- https://howik.com/how-to-run-c-on-wsl-a-complete-guide