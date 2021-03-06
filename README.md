# *Principium* from Latin means *beginning*.
There are tips for doing many things.  
Go inside a folder and read the corresponding `README.MD` file

## Small tips that don't require separate folders:

### backup Ubuntu
[`timeshift` -- manage your backups](https://github.com/teejee2008/timeshift)  

### zsh
[Install `zsh` and `oh-my-zsh` instead of `bash`](https://www.howtoforge.com/tutorial/how-to-setup-zsh-and-oh-my-zsh-on-linux/)  
tl;dr  
`sudo apt install zsh`  
`sudo chsh -s /usr/bin/zsh root`  
`apt install wget git`  
`wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh`
`cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
source ~/.zshrc`
`zsh`
and reboot

[set `zsh` as a default shell](https://askubuntu.com/questions/131823/how-to-make-zsh-the-default-shell)  
[zsh cheatsheet](https://github.com/ohmyzsh/ohmyzsh/wiki/Cheatsheet)  

samples:  
`ga .`          - *git add*  
`gcmsg "msg"`   - *git commit -m "msg"*  
`gp`            - *git push*  

when configuring first time:  
`git config --global user.email "jakub@unold.pl"`

### Use ssh authentication to push and pull from github
[connecting-to-github-with-ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)  
[To switch from https to ssh](https://linuxize.com/post/how-to-remove-git-remotes/)
tl;dr
`ls -al ~/.ssh` - sprawdz czy masz juz *pub'a
jak nie, to `ssh-keygen -t ed25519 -C "jakub@unold.pl"`
`cat ~/.ssh/id_ed25519.pub`
skopiuj to wyjdzie i wrzuc do `add new ssh->`
w title daj `os@hardware`


### Make .iso image of your sdcard
first check out what is mounted b4 inserting sdcard
`sudo blkid`
or
`df -h`
then check again after inserting sdcard. You should receive your sd card name as  
`/dev/sdb`  
or  
`/dev/mmcblk0`  
Lastly, make a copy  
`sudo dd if=/dev/mmcblk0 of=/home/kuba/backup.iso`  

### Flash .iso to an sdcard
see deviced by typing `df -h`
if your sdcard shows up as:
```
/dev/mmcblk0p1  253M   49M  204M  20% /media/kuba/boot
/dev/mmcblk0p2   28G  4,8G   22G  19% /media/kuba/rootfs
```
then flash an iso by typing  
`sudo dd if=2021-10-30-raspios-bullseye-armhf-lite.img of=/dev/mmcblk0`

(*) :face_in_clouds: Remember to add empty ssh file in `boot` folder of the sdcard if you're flasihng raspbian 
EDIT: this does not work for me :joy:

### markdown emoji
[link to cheatsheeet](https://github.com/ikatyang/emoji-cheat-sheet)

### scan network for active devices
`nmap -sP 192.168.0.0/24` - it will scan 256 addresses such as 192.168.0.101 and etc.
`ifconfig` or `ipconfig` is deprecated  
use: `ip address show` 

### insatlling poetry

## Poetry
[How to install poetry](https://vocuzi.in/blog/python-poetry-install-ubuntu-debian/)  
[Basic usage of poetry](https://python-poetry.org/docs/basic-usage/)  

