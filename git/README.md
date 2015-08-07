# GIT tips

---------------------------------
1. Rollback to a specific commit:
---------------------------------
git reset --hard <commit-id>

<...change/commit if need...>

git push <reponame> -f

-------------------------------------------------------------------------
2. Rollback to a specific commit, also with add commit for understanding:
-------------------------------------------------------------------------
git reset <commit-id>

# Move the branch pointer back to the previous HEAD
git reset --soft HEAD@{1}

git commit -m "Revert to ..."

# Update working copy to reflect the new commit
git reset --hard

git push <reponame> -f


--------------------------------------------------------
3. Show diff for staged file (added, not yet committed):
--------------------------------------------------------
git diff --staged <file-path>
or
git diff --cached <file-path>


------------------------------------------------------
4. Checkout and create branch auto named as on server:
------------------------------------------------------
git fetch

...<will see the branch-name on server>...

git checkout <branch-name>


------------------------------
5. Upload an project to github
------------------------------
* Quick setup git repository on github: create on website and get link as
https://github.com/dunght163/test.git
or
git@github.com:dunght163/test.git
(We recommend every repository include a README, LICENSE, and .gitignore.)

or

* Create a new repository on the command line
echo "# test" >> README.md
git init
git add README.md
git commit -m "first commit"
git remote add origin https://github.com/dunght163/test.git
git push -u origin master

or 

* Push an existing repository from the command line

git remote add origin https://github.com/dunght163/test.git
git push -u origin master


----------------------------
6. Merge without auto commit
----------------------------
git merge <branch> --no-commit --no-ff
