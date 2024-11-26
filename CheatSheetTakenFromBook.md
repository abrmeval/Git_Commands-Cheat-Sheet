# **Git Commands CheatSheet**

## Fisrt time Git Setup
You can use `git config --list --show-origin` to list all your settings and where they arte comming from.

You can set your identity with the following commands:

1. `git config --global user.name="John Doe"`
2. `git config --global user.email="johndoe@example.com"`
<hr>

You can set a **default text editor** with the follwing command:
<br>
In this case is configuring **Emacs** as text editor. `git config --global core.editor emacs`
<hr>

Another way is to provide the path of the text editor:
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