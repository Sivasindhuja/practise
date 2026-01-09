to initialise a new local git repo  (git init)

to check any changes between the local and remote repo (git status)

to commit from local to remote first move the files to staging area(git add filenames or . to add all the files)

to actually commit(git commit -m "commit message")

to add a remote repository to a new local(git remote add origin "link to remote repo"

to check the remote repo linked to this local(git remote -v)

to add a branch for the remote (git branch -M main or master)

to push git push -u origin main(for the first time) from the next times just write git push-->-u means upstream

to remove all the git history and replace with the current version,go to the folder and force push(git push --force origin main)

concept:
never initialise a local git repo in a folder in home.if you dont initialise a local repo in any subfolder but try to use git it will track all the system data.
git looks upward for the nearest .git folder and treats it as the root repo.if that .git is in home,code breaks

concept:
dont have nested git repos
for example you have client and server folders in a root folder and the server folder has a seperate .git file then to remove follow these steps
1.git rm --cached server
rm -rf .git/modules/server
rm -rf server/.git
git add server
git commit -m "Fix backend submodule"


