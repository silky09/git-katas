# git-katas

## Branches:

Branch is a name given to the commit. Internally, it is pointer to the commit object.
By default, this name/pointer is master.
Every time you make a new commit, this pointer moves forward.

## What is remote ?

In Git terminology, each machine or location is called a remote, and each one may have one or more branches. Most often, you'll just have one, named origin. To list all the remotes, run

$ git remote
To see which locations these remote names are shortcuts for, run

$ git remote -v
origin git@github.com:foocoding/Git.git (fetch)
origin git@github.com:foocoding/Git.git (push)

Each remote has a directory under git/refs/remotes/:

$ ls -F .git/refs/remotes/

## Cheat sheet

1. To delete a local branch, whether tracking or non-tracking, safely: git branch -d <brachname>

2. To delete a local branch, whether tracking or non-tracking, forcefully: git branch -D <branchname>

3. To delete a remote-tracking branch: git branch -rd <remote>/<branchname>

4. To create a new local non-tracking branch: git branch <branchname> [<start-point>]

5. To create a new local tracking branch: (Note that if <start-point> is specified and is a remote-tracking branch like origin/foobar, then the --track flag is automatically included) git branch --track <branchname> [<start-point] Example: `git branch --track hello-kitty origin/hello-kitty

6. To delete a branch on a remote machine: git push --delete <remote> <branchname>

7. To delete all remote-tracking branches that are stale, that is, where the corresponding branches on the remote machine no longer exist: git remote prune <remote>

8. To check the status of the git repository. (which files are staged, added to the commit, etc.) git status

9. To see the log of previous 'n' commits, git log -n

10. To restore the file <filename> to the version of latest commit git checkout -- <filename>

11. To see the difference between the local repository and the latest commit (HEAD) git diff [filename]

12. THIS IS DANGEROUS!!: To remove the file from both working directory and git git rm

13. To remove the file from git tracking, but still keep it in the working directory: git rm --cached
