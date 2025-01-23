# **Git Commands Cheat Sheet**

## Fisrt-Time Git Setup
You can use `git config --list --show-origin` to list all your settings and where they arte comming from.

You can set your identity with the following commands:

1. `git config --global user.name "John Doe"`
2. `git config --global user.email "johndoe@example.com"`
<hr>

You can set a **default text editor** with the follwing command:
<br>
 `git config --global core.editor emacs`
 <br>
 _In this case, **Emacs** is configured as text editor._
<hr>

Another way is to provide the path of the text editor:
<br>
`git config --global core.editor "'C:/Program Files/Notepadt++/notepad++.exe' -multiInst" -notabbar -nosession -noPlugin`
<hr>

Set a different **default branch name**:
<br>
`git config --global init.defaultBranch main`
<hr>

List all git settings: `git config --list`

Query Git the origin for a value for the configuration variable
`git config --show-origin rere.autoUpdate file:/home/johndoe/.gitconfig false`
<hr>

Get help with a command.
<br>
These three commands are equivalent:
`git help <verb>`
`git <verb> --help`
`man git-<verb>`

## Git Basics

Initialize a repository in an existing directory:
<br>
 `git init`
<hr>

Clone a git repository:
<br>
`git clone https://github.com/libgit2/libgit2`

###  Checking the Status of Your Files
Determine which files are in which state:
<br>
`git status`

**Result:**
On branch master
Your branch is up-to-date with 'origin/master'.
nothing to commit, working tree clean

### Tracking New Files
In order to begin tracking a new file, you use the command git add.
<br>
Adds an untracked file to git repository:
<br>
`git add <filename>`

Example:
`git add README.md`

### Staging Modified Files
Adds a file to the staging area.<br>
To stage a modified file, you run the `git add` command. `git add` is a **multipurpose command** — you use it to begin
tracking new files, to stage files, and to do other things like marking merge-conflicted files as
resolved.
`git add <filename>`

Example:
`git add README.md`

We can also add all the files at once:<br>
`git add`

### Short Status
if you run `git status -s` or `git
status --short` you get a far more simplified output from the command:
<br>
`git status -s`

### Ignoring Files
You can create a file named `.gitignore` that contains a list of patterns to ignore specific files from the repository.<br>

### Viewing Your Staged and Unstaged Changes
To see what you’ve changed but not yet staged, type `git diff` with no other arguments:
<br>
`git diff`

It compares what it is in the working directory with what it is in the staging area.

If you want to see what you’ve staged that will go into your next commit, you can use `git diff
--staged`. This command compares your staged changes to your last commit:
<br>
`git diff --staged`

It compares staged changes with the last commit.

You can also use `git diff --cached` to see what you’ve staged so far (`--staged` and `--cached` are synonyms).

### Committing Your Changes
To commit your changes, type `git commit`.
<br>
Doing so launches your editor of choice.

For an even more explicit reminder of what you’ve modified, you can pass the `-v`
option to `git commit`. Doing so also puts the `diff` of your change in the editor so you
can see exactly what changes you’re committing.

Alternatively, you can type your commit message inline with the `commit` command by specifying it
after a `-m` flag, like this:
<br>
Example:
`git commit -m "Added README.md"`
<hr>

### Skipping the Staging Area
To skip the staging area and commit directly to the repository, use the `-a` option to `git commit`:
<br>
Example:
`git commit -a -m "Added README.md"`

### Removing Files
To remove files from the staging area and the working directory, use the `git rm` command:
<br>
Example:
`git rm README.md`

Note: If you modified the file or
had already added it to the staging area, you must force the removal with the `-f` option

Another useful thing you may want to do is to keep the file in your working tree but remove it from
your staging area, use the `--cached` option to `git rm`:

### Moving Files
If you want to rename a file, use the `git mv` command:
<br>
Example:
`git mv README.md README.md.new`

### Viewing the Commit History

