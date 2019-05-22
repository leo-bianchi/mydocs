## Some instructions when managing repositories

Let's suppose you are starting a new project on your machine, and you will want to use git as your VCS.

Follow these instructions to create a Github repository without the need to use a Web Browser

*   First of all, install git package.
```bash
$ sudo apt install git -y
```

*   Now, go to your project main directory and start git VCS:
```bash
$ git init
```
This will add a .git file into your project directory.

*   Create the remote git repository
```bash
$ curl -u 'username' https://api.github.com/user/repos -d '{"name":"repo_name"}'
```
*   Add remotes into the repo
```bash
$ git remote add origin git@github.com:username/reponame
```

*   Add your files locally
```bash
$ git add .
```

*   Commit locally
```
$ git commmit -m "My Commit Commentary"
```

*   Push into master
```bash
$ git push origin master
```

In case of 'permission denied when you try to push, follow these steps:

*   Install ssh package
```bash
$ sudo apt install ssh -y
```

*   Config a pub key
```bash
$ cd ~/.ssh
$ ssh-keygen
```
*   Copy the key to Github
```bash
$ cat ~/.ssh/id_rsa.pub
```

Paste the key on 'Key' field and give a name for the key.
```
Github Settings-> SSH and GPG keys-> New SSH key
```

```bash
$ ssh -T git@github.com
```
Now you are able to push your project!

*   On project directory type:
```bash
$ git push origin master
```
*   Git status:
```bash
$ git status
Output: Your branch is up-to-date with 'origin/master'.
```
