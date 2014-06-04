gitTutorial
===========

Simple tutorial for using git for UAARG projects.

We use git for:
- Keeping track of changes to all of our software
- Writing software collaboratively, with lots of people on a team

Both of these are pretty important when writing software. You don't want to make a major change that breaks everything and have no way to go back to a working version. You also don't want to email around individual changes to your code and then end up with a mess of different versions.

git is a tool that lets you avoid that. More specifically, it's a *software version control tool*.

How do I get started?
---------------------

### Getting a local repository ###
Clone the repository. Type this in at your command line:
`git clone https://github.com/uaarg/gitTutorial.git`

This makes a version of the repository on your computer in a new folder called gitTutorial. You can see that all of the files in the gitTutorial Github repository have been downloaded to your computer.

A **repository** is different from just a folder with a bunch of code in it because it has the full history of the project as well. Use a `git log` to see the project history.

### Making and logging changes ###
git will know about any changes you make to files inside the repo. Type `git status` to see the status of any changes you have. To actually log these changes, you need to **commit** them.

There's a file called `names.txt` in this repo. Edit this in your favourite text editor (you can use `gedit` on Ubuntu) and add your name to the file. (or a nice/terrible message if you like)

Type a `git status` again, and you should see some changes show up like this:

```
# On branch master
#
# Changes not staged for commit:
#   (use "git add <file>..." to update what will be committed)
#   (use "git checkout -- <file>..." to discard changes in working directory)
#
#	modified:   names.txt
#
```

These changes won't automatically be committed. As far as git is concerned, changes you make in a repo fall under 3 categories:

1. Changes in your working directory. This is like items that you've got in a warehouse that you want to ship eventually.
2. Changes in your staging area. This is like items that you've put on the loading dock of a warehouse.
3. Changes that have been committed. This is like items that you actually load from the dock onto a truck to be shipped off.

To get your changes from the working directory to the staging area, use `git add [file_name]`. In this case it'll be `git add names.txt`.

```
# On branch master
#
# Changes to be committed:
#   (use "git reset HEAD <file>..." to unstage)
#
#	modified:   names.txt
#
```

To commit this change, use `git commit -m "[commit message]"`, eg. `git commit -m "I added my name for the file. Am I a git master now???"`.

```
[master 184919b] I added my name for the file. Am I a git master now???
 1 file changed, 1 insertion(+)
```

### Putting changes on Github ###

If you've set everything up properly, `git push` will do this.
