## Running a PHP server using DockerFile on a AWS EC2 Instance & Automating it with GitHub Actions

xflow@wajahat:Downloads$ ssh -i ubuntu-server-1.pem ubuntu@44.202.92.141
Welcome to Ubuntu 24.04 LTS (GNU/Linux 6.8.0-1009-aws x86_64)

 * Documentation:  https://help.ubuntu.com
 * Management:     https://landscape.canonical.com
 * Support:        https://ubuntu.com/pro

 System information as of Fri Aug  2 07:43:37 UTC 2024

  System load:  0.0               Processes:             113
  Usage of /:   42.0% of 6.71GB   Users logged in:       1
  Memory usage: 38%               IPv4 address for enX0: 172.31.89.167
  Swap usage:   0%


Expanded Security Maintenance for Applications is not enabled.

0 updates can be applied immediately.

Enable ESM Apps to receive additional future security updates.
See https://ubuntu.com/esm or run: sudo pro status


*** System restart required ***
Pending kernel upgrade!
Running kernel version:
  6.8.0-1009-aws
Diagnostics:
  The currently running kernel version is not the expected kernel version 6.8.0-1012-aws.
Last login: Fri Aug  2 07:42:00 2024 from 115.186.134.230
ubuntu@ip-172-31-89-167:~$ ls
Dicecamp-12
ubuntu@ip-172-31-89-167:~$ cd .ssh/
ubuntu@ip-172-31-89-167:~/.ssh$ ls
authorized_keys  id_rsa  id_rsa.pub
ubuntu@ip-172-31-89-167:~/.ssh$ cat id_rsa.pub 
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAACAQCqi1j+nNG2517RGqO4qSHkS3Gllo+oKyiMfZoTBXro2FR+tivpI8ZLiI2VzMdy1Hfm1FKE7qsqvymiA6jzg3bOL5mIQdkwM2qio8iSnHQzJqMe/lQcTCg4qdhSMVvgcGaIa8sekluO2oN+9+Ga8Xkom8GWSwJ77M+yxUX46zdN5Bj2vWlFdyxawIjIPq5b9j+1CpG8GMZSP/aXTDZPGvhyVunH5oAIHDK/oCDjVbakmd6RwqzNoTx7bhfR+HuojQJxsKw1dqfPWrNX2pIYrcJea+FGjSISYDjwx8YCN1FVPJIaH0Rtzm+H5b9RAv2HI5Ze3nFxYVatz49ZWHsxg+gC6w2Xw6lV9hHzC5FYs2vcyLnjWG3YUyi85H828hGVAs+yi1xGhVJkgBT8L4+lFVDB/E8TVjgUAjDGEFEtmFpCRiYw6H3LICZNwwgQZWGLuJBbdJXkOHl9tX5l6DQl/MjkDDmSJpXpSJNDzIhCR9CXKQBORd/gxFbxVmK7jX55Mwr0lX3w61ORY3Ywck/VYfRNyBWGR0rwWQhDx6dNJUruIlIPAv1x+UIomBCmQpX8nU1rla9tc8NlucneNbQRr2Nd4eCyEFhZgAKgYy55uKBBuHn0OI7UGBPNv4yYYLKP9T/6wCL1NC4cIxNXBNKRh/uhJ0oZNGzf463RICGFYC7GDQ== wajahat37@gmail.com
ubuntu@ip-172-31-89-167:~/.ssh$ cd
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ ls
Dicecamp-12
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ ssh -T git@github.com
The authenticity of host 'github.com (140.82.114.3)' can't be established.
ED25519 key fingerprint is SHA256:+DiY3wvvV6TuJJhbpZisF/zLDA0zPMSvHdkr4UvCOqU.
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Hi wajahatrazi! You've successfully authenticated, but GitHub does not provide shell access.
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ ls
Dicecamp-12
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ 
ubuntu@ip-172-31-89-167:~$ cd Dicecamp-12/
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ ls
Assignment_2  Assignment_3  README.md
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git add .
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git commit -m "Setting up workflows"
On branch main
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)

nothing to commit, working tree clean
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git push 
Username for 'https://github.com': ^C
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git config --global user.name "wajahatrazi"
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git config --global user.email "wajahat37@gmail.com"
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git push
Username for 'https://github.com': wajahatrazi
Password for 'https://wajahatrazi@github.com': 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git remote -v
origin	https://github.com/wajahatrazi/Dicecamp-12.git (fetch)
origin	https://github.com/wajahatrazi/Dicecamp-12.git (push)
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git remote set-url origin git@github.com:wajahatrazi/Dicecamp-12.git
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git remote -v
origin	git@github.com:wajahatrazi/Dicecamp-12.git (fetch)
origin	git@github.com:wajahatrazi/Dicecamp-12.git (push)
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ ls
Assignment_2  Assignment_3  README.md
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ ls -a
.  ..  .git  .github  Assignment_2  Assignment_3  README.md
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ git push origin main
Enumerating objects: 6, done.
Counting objects: 100% (6/6), done.
Compressing objects: 100% (2/2), done.
Writing objects: 100% (5/5), 359 bytes | 359.00 KiB/s, done.
Total 5 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To github.com:wajahatrazi/Dicecamp-12.git
   c15e42d..0d3fe58  main -> main
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ eval "$(ssh-agent -s)"
Agent pid 15551
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ ssh-add ~/.ssh/id_rsa
Identity added: /home/ubuntu/.ssh/id_rsa (wajahat37@gmail.com)
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ ls
Assignment_2  Assignment_3  README.md
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
ubuntu@ip-172-31-89-167:~/Dicecamp-12$ 
