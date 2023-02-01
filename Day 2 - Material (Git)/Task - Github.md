# TASK - GITHUB
#
### Mentee : Muhammad Aditya Fathur Rahman
---
#
0. Setting koneksi ssh github
```shell
$ ssh-keygen -t ed25519 -C "madityafr3@gmail.com"
$ cat .ssh/id_ed25519.pub
```
![Alt text](gitsshkey.png?raw=true "Generate sshkey")
![Alt text](gitsshkeysubmit.png?raw=true "submit sshkey")
1. Membuat Repository di Github

Link Repo : https://github.com/mafr017/task-github

![Alt text](createrepo-0.png?raw=true "Create repository Github")
![Alt text](createrepo-1.png?raw=true "New repository Github")
```shell
$ git config --global user.name "Muhammad Aditya Fathur Rahman"
$ git config --global user.email "madityafr3@gmail.com"
$ git clone git@github.com:mafr017/task-github.git
$ echo -e "# TASK GITHUB\n##\n### Mentee : Muhammad Aditya Fathur Rahman" > README.md
$ git add .
$ git commit -m "Init Repo"
$ git push -u origin master
```

2. Implementasi branch master, dev, featureA, featureB
3. Implementasi push, pull, stash, merge
```shell
$ git checkout -b development origin/master
$ echo -e "Ini Branch Development" > file.txt
$ git add .
$ git commit -m "Add file.txt"
$ git push
$ git checkout -b featureA origin/development
$ echo -e "Ini Branch Development, Sedang membuat featureA" > file.txt
$ git add .
$ git commit -m "Edit add featureA in content file.txt"
$ git push
$ git checkout -b featureB origin/development
$ echo -e "Ini Branch Development, Sedang membuat featureB" > file.txt
$ git add .
$ git commit -m "Edit add featureB in content file.txt"
$ git push
$ git checkout development
$ git pull
$ git merge featureA
$ git push
$ echo -e "Saat Ini Branch Development, Sedang membuat featureA" > file.txt
$ git stash
```

4. Implementasi conflict di branch **dev** ketika merge dari **featureA** lalu merge dari **featureB**
```shell
$ git merge featureB
$ nano file.txt
$ git add .
$ git commit -m "Resolve conflict file.txt"
$ git push
```
![Alt text](conflict-1.png?raw=true "Resolve conflict")
![Alt text](conflict-2.png?raw=true "Resolve conflict")

5. Implementasi merge no fast forward
```shell
$ git checkout master
$ git pull
$ git merge --no-ff development
$ git push
```
![Alt text](merge-noff.png?raw=true "Merge no fast forward")

6. Screenshot hasil network di github

![Alt text](network.png?raw=true "Network")