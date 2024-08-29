---
layout: post
title:  "Command Line Basics"
---

Lesson contents:

* TOC
{:toc}

## Introduction

Command Line Interface the OS built in software used to talk to the kernel with commands. The CLI can do what the GUI and more. Each OS has different CLI and their own commands syntax.

## Lesson overview

- Describe what the CLI is.
- Open the CLI to:
    - **Navigate** dir and **print** dir content.
    - **Create** new dir and file.
    - **Rename** or **destroy** dir and file.
    - **Open** dir and file.

## Test drive your terminal

Here are ways to open terminal:

- Linux: Open the programs menu and open Terminal. Or use the shortcut `ctrl` + `alt` + `T`.
- macOS: Open Applications > Utilities and find Terminal. Or use Spotlight to open Terminal. Use `cmd` + `space` to open Spotlight and search for Terminal.

Here is the window anatomy. There will be a window, with black background and 1 line of text, what is written is based on the OS. The 1 line of text ends with `$`. Newer Macs have `%`. `$`, `%` or any other symbol there is the prompt. When you see the prompt, the terminal is waiting for you to type a command. try the `whoami` command, hit enter to send the command to the kernel.

When you go online and see this kind of snippet:

```Bash
$ whoami
```

The prompt `$` is not part of the command, they put it there to tell you that it is Bash syntax. So when you paste into terminal do not include the prompt.

## Why learn this now?

You will use CLI often. When you install softwares, or using Git, or when you use your rented server later. This is a skill all developer needs.

## Use the command line like a pro

### Copy and paste

Use the terminal shortcuts. To copy and paste, `ctrl` + `shift` + `c` or `cmd` + `c` for mac. Then use the `v` counterpart to paste.

### Tab completion

There is also tab completion, this is a feature where the terminal will type out what you want to type for you. The terminal can only type for you when there is only 1 option, example: If in the current working dir there are 2 dirs, `Documents` and `Downloads`, if you type `Do` and then press `tab`, the command line will not type the rest for you since it does not know which one to type, if you press `tab` it instead will show you the options that it is not sure which one to pick:

```Bash
$ Do
Documents/ Downloads/
```

Once you type `Doc`, then there can only be 1 outcome, then the terminal can type the rest for you.

```Bash
$ Doc
Documents
```

If say you only type `D`, then when you press `tab`, CLI will type `Do` for you. Since after that the path branches to either `Documents` or `Downloads`. There was only 1 outcome to `Do` so that is why it knows and it types it for you, it only stops when it reaches a fork in the road.

### Current work dir special dir

Here is a shortcut to opening everything in a dir. If you have a software that can open files like a notepad, you can use this to tell notepad to open all things inside a dir. `.`. Or `git add .`, or `code .`.

## Opening files in VSCode from the command line

- **Linux:**  
  Type `code` and what you type after is what you want to open in VSCode. `code my_awesome_project/`.

- **macOS:**  
  Open VSCode and open the Command Pallete with `cmd` + `shift` + `p`. Type `shell command`, pick `Shell Command: Install 'code' command in PATH`. Select and restart the terminal, then it should work.

- **WSL2:**  
  Open VSCode from CLI in WSL2, same way like in Linux. It will open VSCode in WSL2. (not windows dir, the linux dir space)

## Assignment

This assignment expects a dir called Desktop in home dir.

If using WSL2, use `wget` with the link to get the zip file in WSL2 installation.

`wget https://swcarpentry.github.io/shell-novice/data/shell-lesson-data.zip`

Then install unzip with `sudo apt install unzip`. Then use that to unzip what you just downloaded `unzip shell-lesson-data.zip`. When the course tells you to go to desktpo, you want to go to your home dir, where you downloaded the file. To quickly go back home use `cd ~` or just `cd`.

This section reference is [here](https://swcarpentry.github.io/shell-novice/), The Unix Shell course designed by the Software Carpentry Foundation.

There are many lessons on the CLI there, but here you just need to do the following:

- [Download files](https://swcarpentry.github.io/shell-novice/#download-files). Here just follow the Download files section instructions.
- [Introducing the Shell](https://swcarpentry.github.io/shell-novice/01-intro.html).
- [Navigating Files and Directories](https://swcarpentry.github.io/shell-novice/02-filedir.html).
- [Working With Files and Directories](https://swcarpentry.github.io/shell-novice/03-create.html).

## Download files

Click the link if on Linux or do the WSL2 above. Move it to desktop dir and unzip it there.

## Introduction the Shell

### Background

People made steering wheel for us to use to turn the car wheel. People also make things for people to use to interact with the computer. Most common ways to use is GUI, use mouse to click on things on screen to send commands. There is another way to send commands, using The Unix shell, that refers to the CLI and the scripting language.

### The Shell

Shell is a software for you to type commands to open softwares, create dir and more. There are many Unix shell, most popular is Bash. Bash is default on most Unix implementation, or Unix tools like Git Bash. The Git Bash syntax is similar to Bash. You can create scripts to do things, but here we just learn the commands to make file manipulation faster.

Here we show the prompt with`$`.

Here we discuss the anatomy of the CLI further. In front of the prompt is the cursor. The cursor is where the letters appear on key down. Behind the prompt there usually is your username and host name.

```Bash
nelle@localhost $
```

Does not matter how it looks, all that matters is we are using Unix shell Bash.

Try the `ls` command. It lists the current dir content.

```Bash
$ ls
computer.desktop        network.desktop    shell-lesson-data.zip  user-home.desktop
lubuntu-manual.desktop  shell-lesson-data  trash-can.desktop
```

If you type non existing command or non existing program, it prints:

```Bash
$ fdafdsafdas
fdafdsafdas: command not found
```

In the following lessons, we will learn:
- Dir / file navigation
- Dir / file creation
- Chain commands
- Get files
- The rest are covered in the reference that we will not discuss here

## Navigating Files and Directories

File system software is part of OS, it manages your files and dirs. Data in 1s and 0s are organized into files, dirs hold files or other dirs.

So far we learn how to get user username, list current dir content. Next we learn how to know where we are, the current working dir.

```Bash
$ pwd
/home/cliffordwilliam
```

**Note: Bash uses forward slashes `/`, while windows uses back slashes `\` for dirs**

The command above prints the current working dir. Just like the GUI file explorer, you can only be in 1 folder at a time, think of a folder as a room in a building. The current room that you are in is referred to as the current working dir. Running a command without extra info on where to run it will default to run it in current working dir.

Here, `/home/cliffordwilliam` is my home dir. Different OS or different OS versions will have different home dirs. At this point, return to your home dir, use the `cd` or `cd ~` to go home.

In all OS there is the most top dir, called root dir. Think of it as the top of the tree. So root dir holds all dir and files in your system. Root dir is `/`, forward slash. Usually in root there are `bin` dir that store built-in programs, `data`, `users` where user personal dirs are, `temp` for temporary files and more. So `/home/cliffordwilliam` means:

- `/` = Root dir
  - `home/` = home dir
    - `cliffordwilliam/` = current working dir

So dir are named like this `dir_name/`.

Whenever you open a terminal, it should open in home dir.

### Options

Use `ls` to see what is inside a dir. There are more options for this command. `-F` option adds type indicator to output. These options are **case sensitive**.

- Trailing `/` = directory.
- `@` = link.
- `*` = executable.
- Nothing = file

Some CLI may also use colors to indicate instead.

Options that starts with:
- `-` = is for short options.
- `--` = is for long options.

```Bash
ls -F
aseprite_files/  Documents/  index.html  Pictures/  repos/  syllabus     Templates/
Desktop/         Downloads/  Music/      Public/    snap/   syllabus.md  Videos/
```

Use `clear` to clear previous prints in terminal.

### Getting help

There is a documentation that lists down all of the commands and their options you can use in Bash.

1. `--help`: doc for 1 command.
2. `man ls`: manual for 1 command, is available in Linux and MacOS.

#### Built-in commands

Some are Bash built-in, some are separate program commands, like those that belongs to file system. **So to get Bash built-ins command help use `help cd` or other commands**.

#### The --help option

Most commands and programs that people have made for Bash (not built-ins Bash) supports `--help` option that shows info how to use that one command.

```Bash
ls --help
Usage: ls [OPTION]... [FILE]...
List information about the FILEs (the current directory by default).
Sort entries alphabetically if neither -cftuvSUX nor --sort is specified.

Mandatory arguments to long options are mandatory for short options, too.
  -a, --all                  do not ignore entries starting with .
  -A, --almost-all           do not list implied . and ..
      --author               with -l, print the author of each file
  -b, --escape               print C-style escapes for nongraphic characters
      --block-size=SIZE      scale sizes by SIZE before printing them; e.g.,
                               '--block-size=M' prints sizes in units of
                               1,048,576 bytes; see SIZE format below
  -B, --ignore-backups       do not list implied entries ending with ~
  -c                         with -lt: sort by, and show, ctime (time of last
                               modification of file status information);
                               with -l: show ctime and sort by name;
                               otherwise: sort by ctime, newest first
  -C                         list entries by columns
      --color[=WHEN]         colorize the output; WHEN can be 'always' (default
                               if omitted), 'auto', or 'never'; more info below
  -d, --directory            list directories themselves, not their contents
  -D, --dired                generate output designed for Emacs' dired mode
  -f                         do not sort, enable -aU, disable -ls --color
  -F, --classify             append indicator (one of */=>@|) to entries
...        ...        ...
```

If you see the doc for the `ls` command. There are 2 versions for the options, one is short and the other is long, both are the same thing. You want to use the short ones, long ones are used for writing scripts that we will not cover here. But is covered in the reference material.

Here is what you get when you tried to use a non existing option:

```Bash
ls -z
ls: invalid option -- 'z'
Try 'ls --help' for more information.
```

#### The man command

This opens the a command documentation.

```Bash
man ls
```

When you open this you enter a **special mode**. In this mode you need to know the manual commands:
- Up / down arrows to scroll **line-by-line**.
- `b` + `space` / `ctrl` + `space` to scroll **page-by-page**.
- `/` + word, then hit `enter` to **search**
  - `n` / `shift` + `n` to navigate search hits.
  - hit `enter` to exit search navigate mode.
- `q` to exit.

#### Help from Web

Search the Web that must include the phrase "unix man page" and followed by the command. Or you can use the GNU [manuals](https://www.gnu.org/manual/manual.html) and [core GNU utilities](https://www.gnu.org/software/coreutils/manual/coreutils.html).


### More ls options

`-l` long listing, adds extra info, file size, modified at and more.
`-h` human readable, makes number to be formatted in an easier way to read (5369 to 5.3K)

You can combine options like this

```Bash
ls -lh
total 64K
drwxrwxr-x  3 cliffordwilliam cliffordwilliam 4.0K Jul  2 18:32 aseprite_files
drwxrwxr-x  3 cliffordwilliam cliffordwilliam 4.0K Aug 27 19:16 Desktop
drwxr-xr-x  5 cliffordwilliam cliffordwilliam 4.0K Aug 24 10:31 Documents
drwxr-xr-x  3 cliffordwilliam cliffordwilliam 4.0K Aug 27 19:13 Downloads
-rw-rw-r--  1 cliffordwilliam cliffordwilliam  460 Jul 18 06:35 index.html
drwxr-xr-x  3 cliffordwilliam cliffordwilliam 4.0K Jul  2 18:40 Music
drwxr-xr-x  7 cliffordwilliam cliffordwilliam 4.0K Aug  9 18:55 Pictures
drwxr-xr-x  2 cliffordwilliam cliffordwilliam 4.0K May 27 22:25 Public
drwxrwxr-x 10 cliffordwilliam cliffordwilliam 4.0K Aug 25 19:41 repos
drwx------  4 cliffordwilliam cliffordwilliam 4.0K Jul 28 14:26 snap
-rw-rw-r--  1 cliffordwilliam cliffordwilliam 4.7K Aug 14 21:47 syllabus
-rw-rw-r--  1 cliffordwilliam cliffordwilliam 4.7K Aug 14 21:48 syllabus.md
drwxr-xr-x  2 cliffordwilliam cliffordwilliam 4.0K May 27 22:25 Templates
drwxr-xr-x  2 cliffordwilliam cliffordwilliam 4.0K May 27 22:25 Videos
```

You can use the `-t` to list by modified at ASC.

You can use the `-r` to reverse the order.

### Exploring Other Directories

#### Argument

When you use commands like `ls` it targets the current working directory. But you can also change the target by passing argument. (you pass argument, you declare parameters)

```Bash
ls -F path/to/target/dir
```

If the path does not exists it returns an error

```Bash
ls fdasfdas/
ls: cannot access 'fdasfdas/': No such file or directory
```

Note that the content of the Desktop is rendered in your computer desktop.

It is best to organize file properly and not dump everything in desktop for you to find things easily.

#### No output

Many commands do not output anything when it is successful.

### Change current working dir

You can change where you are just like how you move around in GUI file manager.

`cd` then followed with the path you want to go to.

`cd` does not print anything, but it takes path arguments.

Try to get into the `exercise-data`.

Here is using relative path if Desktop is in my current working dir. Relative path auto add where you are to what you type, meaning if you are in `/home/cliffordwilliam`, then you know there is `Desktop` dir in there, typing the relative path means you type `Desktop/` only, and that as argument will have Bash adds the missing front. So it actually evaluates to `/home/cliffordwilliam/Desktop`.

So when you are in `home/cliffordwilliam` and you know that there are `Desktop` dir in it.

This relative path argument.

```Bash
$ cd Desktop/shell-lesson-data/exercise-data/
```

Is actually evaluated to this, the absolute.

```Bash
$ cd /home/cliffordwilliam/Desktop/shell-lesson-data/
```

So writing relative is a shorthand to write absolute, as the CLI software will fill in the rest.

Now you know how to go to any dir you want in a machine.

Here is a shortcut to go up a dir, `cd ..`. This shortcut is built-ins into how the file system is organized. If you pay attention and `ls -a`, it will show files with . at the start of their names (these are hidden when you use `ls` by default, as these are config files for different softwares). And you notice that there are always 2 dir that are present no matter where you are, `.` and `..`. These are anchor point that allows `cd .` and `cd ..` to function. So when you pass `..` to the `cd` as argument, the CLI evaluates the `..` to the absolute path of the parent dir.

If you use `cd` without passing any arguments, it has default argument, the home path.

`~` = your home path. This is a shortcut in CLI. Only works if it is the first part of the path (since it includes the root path in it), so it is safe to have dir with `~` name.

But what if you have a dir with `~` name in root? You can escape this shortcut behaviour with this `cd /\~`, the `\` followed by reserved characters will be treated as normal characters. Or the easiest way is to use single or double quotes, what you put in there will be treated as path, no shortcut or anything will work in it.

You can undo, use `cd -`, this will evaluate into the prev path you passed into it. And also prints out what the prev path evaluates too.

### General Syntax of a Shell Command

Here is the syntax anatomy in Bash.

Given the following.

```Bash
$ ls -F /
```

Then (NEEDS SPACES AS DELIMITERS):
- `$`: prompt.
- `ls`: command.
- `-F`: option.
- `/`: argument.

Spaces are used as delimiter as a way to tell CLI where 1 thing begin and another ends. Otherwise how can it know when a command starts and end? The order at which you organize the parts is also fixed, the first thing after prompt is always a command in the eye of the CLI.

Options: alter command behaviour.
Arguments: the command target.

Commands are designed by someone, the way someone design it is like a machine, sometimes it has parameters, sometimes it has optional parameters, sometimes it needs multiple parameters and so on. We can consider the option as either flags, switch or parameters too. But for consistency we are referring them here as option, since they are separated in terms of syntax in comparison to the command arguments. In most programming languages there are no options, only parameters.

## Working With Files and Dirs

### Creating directories

At this point, we know how to get to any files or dirs in a machine. Now we learn how to make and move them.

Go to the `shell-lesson-data/exercise-data/writing/`.

In there create a dir called thesis.

```Bash
$ mkdir thesis
```

No output

You can use the `-R` in `ls` to list all nested sub dir,

```Bash
$ ls -FR
.:
exercise-data/  north-pacific-gyre/

./exercise-data:
alkanes/  animal-counts/  creatures/  numbers.txt  writing/

./exercise-data/alkanes:
cubane.pdb  ethane.pdb  methane.pdb  octane.pdb  pentane.pdb  propane.pdb

./exercise-data/animal-counts:
animals.csv

./exercise-data/creatures:
basilisk.dat  minotaur.dat  unicorn.dat

./exercise-data/writing:
haiku.txt  LittleWomen.txt

./north-pacific-gyre:
goodiff.sh   NENE01729A.txt  NENE01736A.txt  NENE01751B.txt  NENE01843A.txt  NENE01971Z.txt  NENE01978B.txt  NENE02040A.txt  NENE02040Z.txt  NENE02043B.txt
goostats.sh  NENE01729B.txt  NENE01751A.txt  NENE01812A.txt  NENE01843B.txt  NENE01978A.txt  NENE02018B.txt  NENE02040B.txt  NENE02043A.txt
```

### Naming files and dirs

1. **Do not use spaces:**  
  Spaces are used to separate arguments in commands, so the space character is reserved as CLI argument delimiters. You can use the '' in the path to escape the space reservation but it is better to avoid spaces. Use `-` or `_`. Take note that the `-` acts as a separator for each work so it behave just like a space, `_` is treated like another character so there is no separation between letters.

2. **Do not use `-` at start:**  
  This is because `-` is reserved for starting an option, you can escape it but better name it with something so that you can avoid using the escape.

3. **Use letters. numbers, period, dash and underscore:**  
  The reason is the other characters are reserved already.

Pay attention to the path before using it in any commands, if it has spaces or symbols, better use the quotes to escape it.

### Create a text file

Go into thesis dir and create a file:

```Bash
$ nano draft.txt
```

Nano is just like VSCode, it is a text editor, but a very light and simple one that is available in Unix like system. Like the notepad of Windows. When you use nano, it will be opened in the current working dir, that is where it looks for file and where it saves them. If you were to open Nano from GUI in start menu, it will save to either documents or desktop dirs since there are no current working dir, there should be a save as feature too.

When you open nano, there should be legendds on the nano commands at the bottom, the `^` means it is the `ctrl` key. `WriteOut` = write to disk. It will then asks what name should it be saved under, the name should be recommended as what the file name was you pass to the nano command argument. Then quit the nano. There is no output on quit but your file should be there.

Here are other ways the ctrl key may be represented as:

-Control-X
-Control+X
-Ctrl-X
-Ctrl+X
-^X
-C-x

### Creating files in a different way

TODO

## Command lists

Here are lists of commands from this lesson.

### mkdir

Make dir

No output

Argument:
- path to a non existing dir, it will make that dir exist
- add space between path to make more than 1
- make multiple dirs:

Options:
- `-p` = able to create dir with nested sub dir in it

### cd

change directory, move to absolute or relative path.

Argument:
- path. (needs the whole thing from the root)
- `.`. == current working dir path
- `..`. == parent path
- `~` == home path
- `-` == the prev path you used
- Nothing: home path default argument.

### Help flags

- `command --help`: third party help feature.
- `help command`: built-ins Bash help.
- `man command`: manual book.

### History

Use the up / down arrow to see old commands. Limit is set in CLI setting, how much it remembers.

### clear

Clear terminal.

### pwd

Prints working dir.

### ls

Listing, list current dir contents. Alphabetical name ASC default.

Options:
- `-F` = adds type indicator.
- `-l` = adds more info (size in BYTES).
- `-h` = reformat to human readable.
- `-t` = ASC modified at.
- `-r` = Flip ordering.
- `-s` = add size info in BLOCKS (diff OS diff unit).
- `-S` = ASC size.
- `-R` = list sub dirs.

### whoami

Returns username
