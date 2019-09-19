### Create Remote Git Repo

```
$ mkdir reponame
$ cd reponame
$ git init
$ git add .
$ git commit -m "init reponame"
$ curl -u 'username' https://api.github.com/user/repos -d '{"username":"reponame"}'
// 'username' should be replaced with your account name on github
// 'reponame' should be replaced with your reponame
$ git remote add origin https://github.com/username/reponame.git
//this step could also be completed wtih ssh:
//    git remote add origin git@github.com:username/reponame.git
$ git push origin master
```

### Add Files
```
$ git add file1 file2 ...
$ git status
```
- *TIPS*&emsp;Don't edit the file with notepad("记事本"),or a "0xefbbbf" will be added at file head."git status" is used to see the status of added files. Only the modifications of text files could be displayed.  <br/> 

### Delete files
```
$ git pull origin master
$ git rm --cached filename
// replace the filename with the file to be deleted.
$ git rm -r --cached foldername
// replace the foldername with the folder to be deleted.
$ git commit -m "your comments"
$ git push origin master
// "git push" also works.
```

### Configure Global Settings
```
$ git config --global --list
$ git config --global --edit
$ git config --global user.name yourname
$ git config --global user.email username@email.com
```

### Configure SSH Login
```
$ git config remote.origin.url git@github.com:yourname/reponame
```
