# Exploring Linux

Course Reference : [DevOps Bootcamp: Learn Linux & Become a Linux Sysadmin](https://academy.zerotomastery.io/p/devops-bootcamp)

---

### The man-page (manual)

description: `man` command in Linux is used to display the user manual of any command that we can run on the terminal

syntax: `$ man COMMAND`


Extra : [man vs help vs info](https://unix.stackexchange.com/questions/19451/difference-between-help-info-and-man-command/159817)

* Pressing `h` will show a list of `less` commands

* Anything that appears before an ellipsis (...) in the synopsis can be repeated

      synopsis:  `$ ls [OPTION]... [FILE]...`

      Here for `ls` we can provide multiple options like `$ ls -a -C` etc.

* Anything that appears inside [] is optional

      For example in the `ls` command we can ignore both arguments.

* Anything that appears in bold should be typed as it is
* Anything with _ or italics should be substituted
* Search in man-age using `/`, go to next (`n`), go to previous ('`Shift + n`)
* Search from end of man-page `?`

### TO check if a command is a shell builtin or executable.
syntax : `$ type COMMAND`

* Use `help` for shell builtin

      $ help ls -----> INVALID

However, we can use `--help` flag or option in both shell builtin or executable command

--- 

### Linux Command Structure

* We can place one or more white space between the arguments. (IT DOESN"T MATTER)
* Standard practice is to write `arguments` after the `command` name. For example: `$ ping -c 1 yahoo.com` rather than `$ ping yahoo.com -c 1`
* We can group short `arguments/options` For example : `$ ls -lh` instead of `$ ls -l -h`. 

---

### Some useful keyboard shortcuts

`CTRL + L` -> Clear screen -> Still scrollable

(CMD + K on mac) or (`clear` command)

`CTRL + D` -> Close the terminal (`exit` command)

`CTRL + A` -> To move the cursor beginning of the line

`CTRL + E` -> To move to the end of line

`CTRL + U` -> Deletes all characters before the cursor ( Cuts and adds it to the clipboard)

`CTRL + C` -> Interrupt the process running in the terminal

`Up Arrow / Down Arrow` -> To get navigate commands from history

---

### The Linux terminal history

* Everything is case sensitive in Linux

`$ cat .bash_history`

`$ echo $HISTFILESIZE` by DEFAULT 2000.

* Run `history` command to list them.
* Run `$ ![COMMAND_NO]` to run the command at `COMMAND_NO` in the history.
* Run `$ !!` -> Similar to running latest command by running doing up arrow.
* Run `$ !-[COMMAND_NO]` run from the last.
* Run the last `command` by doing `$ !command` [CAREFUL can be dangerous]
* Check before you run the command by running ` $ !command:p` to print the command without running it.
* Remove from history `$ history -d LINE_NO`
* Remove entire history `$ history -c`



