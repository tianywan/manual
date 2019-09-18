### Create Git Repo Remotely.

  mkdir reponame                # Create Repo on local server
  git init                      # Initiate Repo
  git add .                     # Add Current Repo
  git commit -m "init repo"     # Commit Repo
  curl -u 'username' https://api.github.com/user/repos -d '{"name":"reponame"}'
                                # replace "username" with your account name on github
                                # replace "reponame" with the name of your repo you will create
  git remote add origin https://github.com/username/reponame.git
  # or you can complete this step by ssh:
  git remote add origin git@github.com:username/reponame.git
  git push origin master        # push it


### File Operation

  git add file1 file2 ...       # add files to local repo, don't edit file with notepad("记事本"),
                                # or a "0xefbbbf" will be added at file head.
  git status                    # see the status of added files. Only the modifications of text files could be displayed.

### Delete some file on remote repo

  git pull origin master        # pull the project from remote project.
  git rm --cached filename      # replace the filename with the file to be deleted.
  git rm -r --cached foldername # replace the foldername with the folder to be deleted.
                                # if you removed option --cached, it will remove the file and folder at local workspace.
  git commit -m "your comments"
  git push origin master        # or just use "git push" will also work.