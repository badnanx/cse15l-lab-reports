# Lab report 3

* [index](https://badnanx.github.io/cse15l-lab-reports/index.html)



## Streamlining ssh
---
* Here I made a .ssh/config file to simplify logging in to the remote machine

![image](lab3-p1-config.png)

* now I can just use `ssh ieng6` to login

![image](lab3-p1-ssh-login.png)

* I can also use `scp` with this method

![image](lab3-p1-scp.png)

## Setup github access from ieng6
---
* Here I made a private/public ssh key pair with ieng6 and github so I can access github from the remote machine

* Public key location on github:
![image](lab3-p2-pubkey-github.png)

* Public and private key location on ieng6:
![image](lab3-p2-pubkey-privkey-ieng6.png)

* We can now commit and push to github from ieng6!:
![image](lab3-p2-git-commit.png)
![image](lab3-p2-git-push.png)

* here is a link to that commit:
[HelloSaturn.txt-commit](https://github.com/badnanx/dir1-repo/blob/c27c406f676e4f96c4b1bd7431872dae97a10407/HelloSaturn.txt)

## Copy whole directories with `scp -r`
---
* We can copy entire directories with `scp -r` as shown:
![image](lab3-p3-scp-r.png)

* this is most faster than copying files one at a time!

* logging in to ieng and running tests:
![image](lab3-p3-tests.png)

* combining actions into one line:
![image](lab3-p3-one-liner.png)



