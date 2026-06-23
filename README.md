# Gym-Advanced-Git-Exercise-Solutions
Hello it is  Aziel
#Challenge 1
```bash
applelab@Mac Aziel  GIT % cd git-survival
applelab@Mac git-survival % ls -a
.                                       .git
..                                      Gym-Advanced-Git-Exercise-Solutions
applelab@Mac git-survival % cd Gym-Advanced-Git-Exercise-Solutions
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git remote remove origin              
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git remote add origin https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git branch -M main
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git push -u origin main
Enumerating objects: 19, done.
Counting objects: 100% (19/19), done.
Delta compression using up to 8 threads
Compressing objects: 100% (10/10), done.
Writing objects: 100% (19/19), 4.69 KiB | 4.69 MiB/s, done.
Total 19 (delta 4), reused 19 (delta 4), pack-reused 0
remote: Resolving deltas: 100% (4/4), done.
To https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
 * [new branch]      main -> main
branch 'main' set up to track 'origin/main'.
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git remote -v
origin  https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git (fetch)
origin  https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git (push)
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git config --local user.name "Leiza"
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git config --local user.email "fatimabobegoto@gmail.com"
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git branch
* main
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git checkout -b feature/docs dev
fatal: 'dev' is not a commit and a branch 'feature/docs' cannot be created from it
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git checkout -b feature/docs    
Switched to a new branch 'feature/docs'
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git branch
* feature/docs
  main
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % touch README.md
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % nano README.md
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % nano README.md
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git add README.md
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git commit -m "first commit" 
[feature/docs ee94b1d] first commit
 1 file changed, 2 insertions(+), 1 deletion(-)
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git push -u origin feature/docs
Enumerating objects: 5, done.
Counting objects: 100% (5/5), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 326 bytes | 326.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
remote: 
remote: Create a pull request for 'feature/docs' on GitHub by visiting:
remote:      https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro/pull/new/feature/docs
remote: 
To https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
 * [new branch]      feature/docs -> feature/docs
branch 'feature/docs' set up to track 'origin/feature/docs'.
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git checkout dev
error: pathspec 'dev' did not match any file(s) known to git
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git branch
* feature/docs
  main
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git add . 
applelab@Mac Gym-Advanced-Git-Exercise-Solutions % git push
To https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
```

##Challenge 2

```bash
applelab@uok-i-mac22 Aziel  GIT % cd git-survival
applelab@uok-i-mac22 git-survival % ls 
Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 git-survival % ls -a
.                                       .git
..                                      Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html.save  team.html       text3.txt
..              config.txt      README.md       text1.txt
.git            home.html       service.html    text2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt 
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout -b feature/conflict
Switched to a new branch 'feature/conflict'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt 
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "update conflict"
[feature/conflict 765b0b8] update conflict
 1 file changed, 1 insertion(+)
 create mode 100644 config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls    
about.html      home.html.save  service.html    text1.txt       text3.txt
home.html       README.md       team.html       text2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git rm config.txt
fatal: pathspec 'config.txt' did not match any files
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout -b feature/conflict
fatal: a branch named 'feature/conflict' already exists
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout feature/conflict
Switched to branch 'feature/conflict'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls
about.html      home.html       README.md       team.html       text2.txt
config.txt      home.html.save  service.html    text1.txt       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev             
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               .git            home.html       README.md       team.html       text2.txt
..              about.html      home.html.save  service.html    text1.txt       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               .git            home.html       README.md       team.html       text2.txt
..              about.html      home.html.save  service.html    text1.txt       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout feature/docs
Switched to branch 'feature/docs'
Your branch is up to date with 'origin/feature/docs'.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               .git            home.html       README.md       team.html       text2.txt
..              about.html      home.html.save  service.html    text1.txt       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git branch
  dev
  feature/conflict
* feature/docs
  main
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % touch config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "creation of conflict"
[dev 76b1e25] creation of conflict
 1 file changed, 2 insertions(+)
 create mode 100644 config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout feature/conflict
Switched to branch 'feature/conflict'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html.save  team.html       text3.txt
..              config.txt      README.md       text1.txt
.git            home.html       service.html    text2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "conflict"
On branch feature/conflict
nothing to commit, working tree clean
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % gid add .
zsh: command not found: gid
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "conflict created"
On branch dev
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   config.txt

no changes added to commit (use "git add" and/or "git commit -a")
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .                       
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "conflict created"
[dev bd9b58a] conflict created
 1 file changed, 1 insertion(+), 1 deletion(-)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git merge feature/conflict
Auto-merging config.txt
CONFLICT (add/add): Merge conflict in config.txt
Automatic merge failed; fix conflicts and then commit the result.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano config.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "conflict resolved"
[dev 8e5b9fe] conflict resolved
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git push 
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

```

##Challenge 3

```bash
applelab@uok-i-mac22 Aziel  GIT % cd git-survival
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Exercise-Solutions
cd: no such file or directory: Gym-Advanced-Exercise-Solutions
applelab@uok-i-mac22 git-survival % ls 
Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html.save  team.html       text3.txt
..              config.txt      README.md       text1.txt
.git            home.html       service.html    text2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git mv README.md Readme.md
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html.save  team.html       text3.txt
..              config.txt      Readme.md       text1.txt
.git            home.html       service.html    text2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "typo resolved"
[dev 0c82eaa] typo resolved
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename README.md => Readme.md (100%)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git push
fatal: The current branch dev has no upstream branch.
To push the current branch and set the remote as upstream, use

    git push --set-upstream origin dev

To have this happen automatically for branches without a tracking
upstream, see 'push.autoSetupRemote' in 'git help config'.

applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git push -u origin main
To https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
 ! [rejected]        main -> main (fetch first)
error: failed to push some refs to 'https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git branch
* dev
  feature/conflict
  feature/docs
  main
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git feature/docs
git: 'feature/docs' is not a git command. See 'git --help'.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout feature/docs
Switched to branch 'feature/docs'
Your branch is up to date with 'origin/feature/docs'.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      README.md       text1.txt
..              home.html       service.html    text2.txt
.git            home.html.save  team.html       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git mv README.md Readme.md
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "typo resolved"
[feature/docs 1e14a1e] typo resolved
 1 file changed, 0 insertions(+), 0 deletions(-)
 rename README.md => Readme.md (100%)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git push
Enumerating objects: 3, done.
Counting objects: 100% (3/3), done.
Delta compression using up to 8 threads
Compressing objects: 100% (2/2), done.
Writing objects: 100% (2/2), 238 bytes | 238.00 KiB/s, done.
Total 2 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
   ee94b1d..1e14a1e  feature/docs -> feature/docs
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git mv Readme.md README.md
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      README.md       text1.txt
..              home.html       service.html    text2.txt
.git            home.html.save  team.html       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano README.md
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "typo resolved"
[feature/docs 94658b7] typo resolved
 1 file changed, 1 insertion(+), 1 deletion(-)
 rename Readme.md => README.md (66%)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git push
Enumerating objects: 4, done.
Counting objects: 100% (4/4), done.
Delta compression using up to 8 threads
Compressing objects: 100% (3/3), done.
Writing objects: 100% (3/3), 331 bytes | 331.00 KiB/s, done.
Total 3 (delta 1), reused 0 (delta 0), pack-reused 0
remote: Resolving deltas: 100% (1/1), completed with 1 local object.
To https://github.com/fatimabobegoto-collab/Git-survival-kit-Webpro.git
   1e14a1e..94658b7  feature/docs -> feature/docs

```

##Challenge 4

```bash
applelab@uok-i-mac22 Aziel  GIT % cd git-survival
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      README.md       text1.txt
..              home.html       service.html    text2.txt
.git            home.html.save  team.html       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git branch
  dev
  feature/conflict
* feature/docs
  main
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout -b feature/rebase-tes
t
Switched to a new branch 'feature/rebase-test'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % touch sample{1,2}.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html.save  sample2.txt     text1.txt
..              config.txt      Readme.md       service.html    text2.txt
.git            home.html       sample1.txt     team.html       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add sample1.txt 
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add sample2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "First commit of Challenge4"
[feature/rebase-test a4fd91e] First commit of Challenge4
 2 files changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 sample1.txt
 create mode 100644 sample2.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % touch fakeCommit.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "fake commit"
[dev 1c75ea3] fake commit
 1 file changed, 0 insertions(+), 0 deletions(-)
 create mode 100644 fakeCommit.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout feature/rebase-test
Switched to branch 'feature/rebase-test'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git rebase dev
Successfully rebased and updated refs/heads/feature/rebase-test.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git log --oneline
51f9ddf (HEAD -> feature/rebase-test) First commit of Challenge4
1c75ea3 (dev) fake commit
0c82eaa typo resolved
8e5b9fe conflict resolved
bd9b58a conflict created
76b1e25 creation of conflict
765b0b8 (feature/conflict) update conflict
ee94b1d first commit
826dcdb (origin/main, main) Merge pull request #3 from fatimabobegoto-collab/master
1242260 first commit bundle2
1982bae Merge pull request #2 from fatimabobegoto-collab/master
42b03a8 first commit
1d1874a Merge pull request #1 from fatimabobegoto-collab/master
e84e8a4 first commit
```

##Challenge 5

```bash 
applelab@uok-i-mac22 Aziel  GIT % cd git-survival
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Exercise-Solutions
cd: no such file or directory: Gym-Advanced-Exercise-Solutions
applelab@uok-i-mac22 git-survival % git branch
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git branch
  dev
  feature/conflict
  feature/docs
* feature/rebase-test
  main
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout main
Switched to branch 'main'
Your branch is up to date with 'origin/main'.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % touch app.js
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano app.js
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "creation of app.js"

[main 32fee63] creation of app.js
 1 file changed, 1 insertion(+)
 create mode 100644 app.js
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout -b hotfix/zero-fix ma
in
Switched to a new branch 'hotfix/zero-fix'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % nano app.js
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git add .
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit -m "app.js modified"
[hotfix/zero-fix d2e8699] app.js modified
 1 file changed, 1 insertion(+), 1 deletion(-)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout main
Switched to branch 'main'
Your branch is ahead of 'origin/main' by 1 commit.
  (use "git push" to publish your local commits)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git merge hotfix/zero-fix
Updating 32fee63..d2e8699
Fast-forward
 app.js | 2 +-
 1 file changed, 1 insertion(+), 1 deletion(-)
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git checkout dev
Switched to branch 'dev'
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git merge hotfix/zero-fix
hint: Waiting for your editor to close the file... error: There was a problem with the editor 'vi'.
Not committing merge; use 'git commit' to complete the merge.
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git commit
[dev df608e2] Merge branch 'hotfix/zero-fix' into dev
```


##Challenge 6
```bash
applelab@uok-i-mac22 Aziel  GIT % cd git-survival
applelab@uok-i-mac22 git-survival % cd Gym-Advanced-Git-Exercise-Solutions
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git branch
* dev
  feature/conflict
  feature/docs
  feature/rebase-test
  hotfix/zero-fix
  main
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % touch .gitignore
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html       team.html
..              app.js          home.html.save  text1.txt
.git            config.txt      Readme.md       text2.txt
.gitignore      fakeCommit.txt  service.html    text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % cd .gitignore
cd: not a directory: .gitignore
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % mkdir .gitignore
mkdir: .gitignore: File exists
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git rm .gitignore
fatal: pathspec '.gitignore' did not match any files
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html       team.html
..              app.js          home.html.save  text1.txt
.git            config.txt      Readme.md       text2.txt
.gitignore      fakeCommit.txt  service.html    text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % mkdir .Gitignore
mkdir: .Gitignore: File exists
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git rm -f .gitignore
fatal: pathspec '.gitignore' did not match any files
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % git rm -f gitignore 
fatal: pathspec 'gitignore' did not match any files
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      home.html       team.html
..              app.js          home.html.save  text1.txt
.git            config.txt      Readme.md       text2.txt
.gitignore      fakeCommit.txt  service.html    text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % ls -a
.               about.html      fakeCommit.txt  Readme.md       text1.txt
..              app.js          home.html       service.html    text2.txt
.git            config.txt      home.html.save  team.html       text3.txt
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % mkdir .gitignore
applelab@uok-i-mac22 Gym-Advanced-Git-Exercise-Solutions % cd .gitignore
applelab@uok-i-mac22 .gitignore % touch secrets.env node_modules/
touch: node_modules/: No such file or directory
applelab@uok-i-mac22 .gitignore % ls -a
.               ..              secrets.env
applelab@uok-i-mac22 .gitignore % touch node_modules/ 
touch: node_modules/: No such file or directory
applelab@uok-i-mac22 .gitignore % ls -a              
.               ..              secrets.env
applelab@uok-i-mac22 .gitignore % touch node_modules.env
applelab@uok-i-mac22 .gitignore % git checkout -b test
Switched to a new branch 'test'
applelab@uok-i-mac22 .gitignore % dd if=/dev/zero of=large.bin bs=1M count=100)
zsh: parse error near `)'
applelab@uok-i-mac22 .gitignore % dd if=/dev/zero of=large.bin bs=1M count=100 
100+0 records in
100+0 records out
104857600 bytes transferred in 0.030721 secs (3413222226 bytes/sec)
applelab@uok-i-mac22 .gitignore % git rm --cached large.bin
fatal: pathspec 'large.bin' did not match any files
applelab@uok-i-mac22 .gitignore % 
```
