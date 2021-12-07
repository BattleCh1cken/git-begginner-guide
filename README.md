# git-begginner-guide



So. You want to learn how to use git.


First you need to create a local git project. This is pretty easy. Just change to the project directory, and run "git init"
If you're using an IDE with a built  in terminal, it will already be in the directory you want.

You can then use "git status" to see the status.It also shows all tracked and untracked files. You can also do "git help" to get a list of all git commands. You can also run "git help <command> to get a help page for a specific command.


Alrighty. You want to make a commit. You wanna use github. Here we go. 

First we gotta track a file. Use "git add <file/dir name>" to track a file. You only commit the files that are tracked, so if you have compiled files, or like mass code for modules, you probably shouldn't track those. You can also set up file/dirs to be ignored with a .gitignore. These are pretty flexible, you could ignore specific file types, or even exclude everything except certain files. Ignored files will not show up when you run "git status", and cannot be tracked.


Now its time to make your first commit! Run "git commit -m "yourmessagehere"". The quotation marks are important here. Usually you just put something like "Initial commit". If you're not the only person on the project, its good to be descriptive with commit messages. Otherwise they might not understand what changes you made right away. It's also useful to your future self for reference.


Now you want to send your code to github (alternativly you might want to send it to a local repo). To do this you need to add a remote origin. Run "git add remote origin <repo url>" Then, you can run "git push origin <branch>" to push it to the branch that you want (when it asks for username and password, it wants for an access token. You can make one under developer settings in github). You can also use a pull request to get the latest version of a branch from github with "git pull <branch>" Wait. What's a branch? We're getting there.


You can have multiple branches in a project. This is also really useful. Per say you wanted to test code before implementing it. You could have a testing branch for unstable code. Once its tested you can merge it into the main branch. You could also have multiple branches for different parts of a project, so that the devs don't get in each other's way.

You can make a new branch with "git checkout -b <branch name>", and switch to an exsisting branch with "git checkout" To merge, use "git merge <branch you want to merge into the current one>. You might need to clean up some merge errors, like if two devs edited the same line, but usually the merge is pretty good about being automatic.


Now you might want to know how to revert a commit, in case you messed something up. Switch to the branch you want with the checkout command, and then use "git revert <commit you want to revert to>.

You can view a list of all commits on all branches with "git log --graph --oneline --all"
