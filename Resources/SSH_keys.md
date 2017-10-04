Some help on SSH keys

[Generating SSH keys](https://help.github.com/articles/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent/)

```shell
$ ssh-keygen -t rsa -b 4096 -C "youremail"
# you will be prompted for a password - this is not your login password but a new password
# you can use for unlocking your keypair
```

Setting up ssh keys for passwordless login
==========================================
1. generate ssh key pair on your laptop
2. Copy ~/.ssh/id_rsa.pub YOURNAME@biocluster.ucr.edu
```shell
$ scp  ~/.ssh/id_rsa.pub biocluster.ucr.edu:.ssh/mylaptopkey.pub
$ ssh YOURNAME@biocluster.ucr.edu
[biocluster] $ cd .ssh
[biocluster] $ cat mylaptopkey.pub >> authorized_keys2
[biocluster] $ chmod 644 authorized_keys2
[biocluster] $ logout
$ ssh YOURNAME@biocluster.ucr.edu
```

Using Public SSH keys
====================
The public SSH keys from your laptop and one on biocluster can be
uploaded to github for easier checkin / checkout authentication via
SSH instead of HTTPS
