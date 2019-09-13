# …or create a new repository on the command line 
echo "# myRepo" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/emiliano84/myRepo.git
git push -u origin master


# …or push an existing repository from the command line
git remote add origin https://github.com/emiliano84/myRepo.git
git push -u origin master


# forcemerge
git fetch origin   # update all our origin/* remote-tracking branches

git checkout demo         # if needed -- your example assumes you're on it
git merge origin/demo     # if needed -- see below

git checkout master
git merge origin/master

git merge -X theirs demo   # but see below

git push origin master     # again, see below