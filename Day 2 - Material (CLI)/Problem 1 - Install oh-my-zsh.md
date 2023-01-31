# Problem 1 - Install oh-my-zsh
##
### Mentee : Muhammad Aditya Fathur Rahman
---
#
1. Install WSL Debian
```console
> wsl --install Debian
> wsl
```
![Alt text](p1-01.png?raw=true "Install WSL Debian")
2. Install ZSH, curl, git, & iputils-ping
```shell
$ sudo apt-get update -y && sudo apt-get upgrade -y && sudo apt-get install zsh curl git -y && sudo apt-get install iputils-ping --reinstall -y && sudo sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)" && chsh -s /bin/zsh
```
![Alt text](p1-02.png?raw=true "Install ZSH")