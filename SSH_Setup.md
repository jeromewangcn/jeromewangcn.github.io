# Interate WSL with Github
First, try to generate ssh key in wsl
```
ssh-keygen -t ed25519 -C "jeromewangcn@outlook.com"
```
you will get
```
Generating public/private ed25519 key pair.
Enter file in which to save the key (/home/jerome/.ssh/id_ed25519): 
```
press enter to continue
```
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
```
Enter the passphrase
```
Your identification has been saved in /home/jerome/.ssh/id_ed25519
Your public key has been saved in /home/jerome/.ssh/id_ed25519.pub
The key fingerprint is:
SHA256: jeromewangcn@outlook.com
The key's randomart image is:
+--[ED25519 256]--+
|  . B*@.         |
|   =oB+O         |
|   o=.+oo        |
|   oo..Bo.       |
|     o=.S..      |
|    .  + ..      |
|   . .  .. . .   |
|    . .o+ o.E    |
|     .++o=....   |
+----[SHA256]-----+
```
Then add ssh key
```
ssh-agent bash
ssh-add ~/.ssh/id_ed25519
```
Finally test the connectivity
```
ssh -T git@github.com
The authenticity of host 'github.com (20.205.243.166)' can't be established.
ED25519 key fingerprint is 
This key is not known by any other names.
Are you sure you want to continue connecting (yes/no/[fingerprint])? yes
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
Hi jeromewangcn! You've successfully authenticated, but GitHub does not provide shell access.
```
