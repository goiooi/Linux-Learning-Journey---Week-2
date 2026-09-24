# Linux-Learning-Journey---Week-2
This document summarizes what I learned during my second week of studying Linux.
In Week 2, I moved beyond the basic concepts of Linux and began learning more about open-source software, software licensing, the Linux command line, Bash, command structure, variables, the PATH variable, command history, aliases, functions, quoting, control operators, and Linux documentation tools.

This week helped me understand how the Linux command line works and how Bash allows users to interact with and control a Linux system.

---

# 1. Open Source and Closed Source Software

One of the first topics I studied this week was the difference between open-source and closed-source software.

## Closed-Source Software

Closed-source software does not generally make its source code available to users.

Users receive rights to use the software according to the terms of its license, but they normally cannot freely study, modify, or redistribute the source code.

An example is Microsoft Windows.

## Open-Source Software

Open-source software makes its source code available under the terms of an open-source license.

Depending on the license, users may have rights to study, modify, and redistribute the software.

Linux is one of the major examples of open-source software development.

I learned that open-source development encourages collaboration and allows developers to inspect, modify, and contribute to software.

---

# 2. Source Code and Binary Programs

I learned that **source code** is the human-readable form of a program.

Source code can be compiled into a binary program that the computer can execute.

Some languages are also interpreted by an interpreter rather than being compiled directly into a standalone executable in the same way.

Examples discussed in the course include:

- Perl
- Python
- Bash

This helped me understand the difference between the code written by a developer and the instructions ultimately executed by a computer.

---

# 3. Open-Source Licensing

Software licenses determine what users are legally permitted to do with software.

Different licenses provide different rights and impose different conditions.

## GNU General Public License

The **GNU General Public License (GPL)** is a copyleft free-software license.

The GPL allows users to use, study, modify, and redistribute software, subject to the conditions of the license.

An important distinction I learned is that different versions of the GPL have different terms.

The **Linux kernel is licensed under GPL version 2, with an explicit "or later" clause not applying to the kernel's license as a whole. The kernel is therefore generally described as GPL-2.0-only.**

This is an important distinction because GPLv2 and GPLv3 are separate license versions with different requirements.

## Tivoization

I also learned about **Tivoization**.

This describes situations where a device uses software under a copyleft license but employs hardware restrictions that prevent users from running modified versions of that software on the device.

Tivoization was one of the issues addressed by GPLv3.

---

# 4. Free and Open Source Software

I learned about **Free and Open Source Software (FOSS)**.

In this context, "free" refers primarily to freedom rather than price.

Free software emphasizes users' freedoms to use, study, modify, and share software.

I also learned the term **FLOSS**, which stands for:

**Free/Libre/Open Source Software**

The use of "libre" helps distinguish software freedom from software that is simply available at no cost.

---

# 5. Free Software Foundation

The **Free Software Foundation (FSF)** was founded by Richard Stallman in 1985.

The FSF promotes software freedom and supports the development and use of free software.

The four fundamental freedoms associated with free software are the freedom to:

1. Run the program for any purpose.
2. Study how the program works and modify it.
3. Redistribute copies.
4. Distribute modified versions.

The FSF also supports licenses such as the GNU General Public License.

---

# 6. Open Source Initiative

I also learned about the **Open Source Initiative (OSI)**.

The OSI promotes and protects the concept of open-source software and maintains the **Open Source Definition**.

I learned that open-source licenses can have different requirements.

One example is the **BSD family of licenses**, which are generally permissive licenses.

Permissive licenses generally allow users to use, modify, and redistribute software with relatively few conditions compared with copyleft licenses such as the GPL.

---

# 7. Creative Commons

I learned that software licenses are not generally the best licensing framework for creative works such as photographs, writing, artwork, and educational materials.

**Creative Commons (CC)** provides licenses designed for many types of creative works.

Some Creative Commons license conditions include:

- **BY - Attribution**: The creator must be credited.
- **SA - ShareAlike**: Adaptations must generally be distributed under the same or a compatible license.
- **NC - NonCommercial**: The work cannot be used for commercial purposes under that license.
- **ND - NoDerivatives**: Adapted versions cannot be distributed.

These conditions can be combined to create different Creative Commons licenses.

I also learned about **CC0**, which is designed to enable a creator to waive copyright and related rights to the extent permitted by law and dedicate the work to the public domain.

---

# 8. Open-Source Business Models

I learned that open-source software does not necessarily mean that a company cannot make money.

"Free" in the context of free software refers to freedom, not necessarily the absence of cost.

Companies can build businesses around open-source software through areas such as:

- Technical support
- Consulting
- Enterprise services
- Cloud services
- Hardware
- Additional proprietary products

Examples discussed in the course included companies such as **Canonical** and **Red Hat**.

This showed me that open-source software and commercial business models can exist together.

---

# Command Line Skills

# 9. Introduction to the Command Line

This week I began studying the Linux command line in greater detail.

The **Command Line Interface (CLI)** allows users to interact with a computer by entering text commands.

The command line can initially seem difficult because there are many commands and options to learn, but it provides a powerful and efficient way to interact with Linux.

Command-line skills can help users:

- Navigate file systems
- Perform tasks efficiently
- Automate repetitive tasks
- Write and run scripts
- Administer remote systems

---

# 10. The Shell

A **shell** is a command interpreter that provides an interface between the user and the operating system.

When a command is entered, the shell interprets it and determines how it should be executed.

## Bash

The shell I focused on during this module was **Bash**, which stands for **Bourne Again Shell**.

Bash provides features such as:

- Command history
- Command-line editing
- Variables
- Aliases
- Functions
- Command substitution
- Shell scripting
- Control operators

---

# 11. Linux Commands

A command is an instruction or executable program that performs an operation when used from the command line.

For example:

```bash
ls
```

The `ls` command lists the contents of a directory.

A common command structure is:

```bash
command [options] [arguments]
```

For example:

```bash
ls -l /etc
```

In this example:

- `ls` is the command.
- `-l` is an option.
- `/etc` is an argument.

Not every command requires options or arguments.

---

# 12. Options and Arguments

## Arguments

An argument provides additional information to a command.

For example:

```bash
ls /etc/ssh
```

Here, `/etc/ssh` is an argument that specifies the directory whose contents should be listed.

## Options

An option changes or controls how a command behaves.

For example:

```bash
ls -l
```

The `-l` option requests a long-format listing.

Options can sometimes be combined.

For example:

```bash
ls -lr
```

Here:

- `-l` requests long format.
- `-r` reverses the sorting order.

The same options can also be written separately:

```bash
ls -l -r
```

---

# 13. Human-Readable Output

I learned that the `-h` option can make certain command output easier for humans to read.

For example:

```bash
ls -lh
```

With a long listing, the `-h` option displays file sizes in units such as KB, MB, or GB where appropriate.

Many commands provide both short options and long options, although the exact options available depend on the command.

For example:

```bash
ls --human-readable
```

is supported by GNU `ls`.

---

# 14. Linux Is Case Sensitive

Linux and Bash are generally **case sensitive**.

This means that capitalization can change the meaning of a command, variable, or filename.

For example:

```bash
ls
```

is not the same command as:

```bash
LS
```

Likewise:

```bash
myfile
```

and:

```bash
MyFile
```

can refer to different filenames.

Accuracy in capitalization is therefore important when working with Linux.

---

# 15. Command History

Bash maintains a history of commands entered during the shell session.

The **Up Arrow** can be used to recall previous commands.

The **Left Arrow** and **Right Arrow** can be used to move through and edit a command.

Other useful editing keys include:

- Home
- End
- Backspace
- Delete

The `history` command displays the shell's command history.

```bash
history
```

## Re-running Previous Commands

Bash also provides history expansion.

For example:

```bash
!!
```

runs the most recent command again.

A history entry can also be referenced by its history number:

```bash
!25
```

This runs history entry number 25, assuming that entry exists.

---

# Bash Variables

# 16. Variables

A variable allows information to be stored and referenced by the shell.

Bash variables can be broadly understood as:

- Shell variables
- Environment variables

---

# 17. Shell Variables

A shell variable can be created by assigning a value:

```bash
variable1=Something
```

There must not be spaces around the `=` sign in a normal Bash assignment.

The variable's value can then be accessed using `$`:

```bash
echo $variable1
```

A shell variable exists within the shell where it was created unless it is exported to child processes.

---

# 18. The echo Command

The `echo` command displays text or the value of variables.

For example:

```bash
echo Hello
```

displays:

```text
Hello
```

A variable can also be displayed:

```bash
echo $variable1
```

The `$` tells Bash to perform variable expansion and substitute the variable's value.

---

# 19. Environment Variables

Environment variables are shell variables that are marked for export so that they are inherited by processes started by that shell.

Examples include:

- `PATH`
- `HOME`
- `HISTSIZE`

## HOME

`HOME` normally contains the path to the current user's home directory.

For example:

```bash
echo $HOME
```

## PATH

`PATH` contains a list of directories that the shell searches when looking for executable commands.

## HISTSIZE

`HISTSIZE` controls the number of commands Bash keeps in its history list in memory.

This should be distinguished from `HISTFILESIZE`, which controls the maximum number of lines stored in the history file.

---

# 20. The env Command

The `env` command can display the environment variables available to the current environment.

For example:

```bash
env
```

Because the output can be long, it can be combined with other commands using a pipe.

For example:

```bash
env | grep HOME
```

The `|` character sends the standard output of the command on its left to the standard input of the command on its right.

---

# 21. Exporting Variables

The `export` command marks a shell variable so that it is included in the environment inherited by child processes.

For example:

```bash
variable1=Something
export variable1
```

This can also be written as:

```bash
export variable1=Something
```

The `unset` command removes a variable from the current shell:

```bash
unset variable1
```

---

# PATH and Commands

# 22. The PATH Variable

The `PATH` variable contains a colon-separated list of directories.

For example:

```bash
echo $PATH
```

might produce something similar to:

```text
/usr/local/bin:/usr/bin:/bin
```

When Bash receives a command that is not a shell keyword, function, alias, or built-in command, it searches the appropriate locations, including directories in `PATH`, to find an executable.

If the command cannot be found, Bash may display:

```text
command not found
```

When modifying `PATH`, it is important not to accidentally remove the existing directories.

For example:

```bash
PATH="$HOME/bin:$PATH"
```

adds `$HOME/bin` before the existing `PATH`.

---

# 23. Paths

A path identifies the location of a file or directory in the filesystem.

For example:

```text
/home/user/Documents
```

The `/` character separates the directories in the path.

Paths can be:

- Absolute paths
- Relative paths

An absolute path starts from the root directory, while a relative path is interpreted in relation to the current working directory.

---

# Types of Commands

# 24. The type Command

The `type` command can help determine how Bash interprets a command.

For example:

```bash
type cd
```

may show that `cd` is a shell builtin.

It can also identify aliases, functions, built-ins, keywords, and executable files.

For example:

```bash
type ls
```

can show that `ls` is an executable and indicate the path Bash associates with it.

---

# 25. Shell Built-in Commands

Some commands are built into the shell itself.

For example:

```bash
cd
```

is a Bash builtin.

This makes sense because changing directories must affect the current shell process. If `cd` were only an external program, it could not change the working directory of the parent shell after it exited.

Other Bash builtins include commands such as:

```bash
echo
export
unset
```

---

# 26. External Commands

External commands are executable programs stored in the filesystem.

For example:

```bash
ls
```

is normally an external executable.

The shell can search the directories listed in `PATH` to locate external commands.

The `which` command can often be used to display the path to an executable:

```bash
which ls
```

A more shell-oriented way to determine what will be executed is:

```bash
command -v ls
```

The `type` command is also useful:

```bash
type ls
```

These tools can be especially helpful when a command name could refer to an alias, function, builtin, or executable.

---

# Aliases and Functions

# 27. Aliases

An **alias** allows a shorter name to be associated with a command.

For example:

```bash
alias ll='ls -l'
```

After creating this alias:

```bash
ll
```

can be used as a shortcut for:

```bash
ls -l
```

The `alias` command can display aliases:

```bash
alias
```

Aliases created directly in the current shell are normally temporary unless they are added to a shell startup file such as `.bashrc`.

---

# 28. Functions

Bash functions allow multiple commands to be grouped together and executed using a single function name.

For example:

```bash
myinfo() {
    echo "Current user:"
    whoami
    echo "Current directory:"
    pwd
}
```

The function can then be executed with:

```bash
myinfo
```

Functions are more flexible than simple aliases and are useful for automation and shell scripting.

---

# Quoting in Bash

# 29. Quoting

Quoting is important because Bash gives special meanings to many characters.

The main forms of quoting I learned about are:

- Double quotes `" "`
- Single quotes `' '`
- Backticks `` ` ``
- Backslash `\`

These affect how Bash interprets text, variables, wildcards, and command substitutions.

---

# 30. Double Quotes

Double quotes preserve most characters literally while still allowing variable expansion and command substitution.

For example:

```bash
name="Linux"
echo "I am learning $name"
```

produces:

```text
I am learning Linux
```

Double quotes are especially useful when working with variables containing spaces.

---

# 31. Single Quotes

Single quotes prevent Bash from performing variable expansion and command substitution inside the quoted text.

For example:

```bash
echo '$PATH'
```

prints:

```text
$PATH
```

rather than displaying the value of the `PATH` variable.

---

# 32. Backslash

The backslash can be used to prevent Bash from interpreting the next character in its special way.

For example:

```bash
echo \$HOME
```

prints:

```text
$HOME
```

instead of expanding the `HOME` variable.

The backslash can also be used to continue a command onto another line.

---

# 33. Command Substitution

Command substitution allows the output of one command to be used as part of another command.

The older syntax uses backticks:

```bash
echo `date`
```

However, the modern and preferred syntax is:

```bash
echo "$(date)"
```

The second form is generally recommended because it is easier to read and can be nested more conveniently.

---

# Control Operators

# 34. Command Sequencing

Bash provides control operators that determine how multiple commands are executed.

The operators I learned about include:

- `;`
- `&&`
- `||`

---

# 35. Semicolon

The semicolon allows commands to be executed sequentially.

For example:

```bash
echo First; echo Second
```

The second command is attempted regardless of whether the first command succeeds or fails.

---

# 36. Double Ampersand

The double ampersand:

```bash
&&
```

means that the next command should run only if the previous command succeeds.

For example:

```bash
mkdir test && cd test
```

If `mkdir test` succeeds, `cd test` is executed.

If `mkdir test` fails, the second command is not executed.

---

# 37. Double Pipe

The double pipe:

```bash
||
```

runs the second command only if the first command fails.

For example:

```bash
cd test || echo "Directory does not exist"
```

If `cd test` succeeds, the `echo` command is skipped.

If `cd test` fails, the message is displayed.

---

# Getting Help in Linux

# 38. Why Linux Documentation Matters

Linux provides thousands of commands, options, utilities, and configuration files.

It is not practical to memorize everything.

One of the most important skills I learned this week is how to find information when I do not know a command or option.

Linux provides several built-in documentation tools.

---

# 39. Man Pages

**Man pages**, short for manual pages, are one of the primary forms of Linux command documentation.

The basic syntax is:

```bash
man command
```

For example:

```bash
man ls
```

A man page normally provides information about the command, its syntax, options, and related details.

The `q` key exits the man page.

---

# 40. Sections of Man Pages

Man pages are divided into numbered sections.

Common sections include:

1. General commands
2. System calls
3. Library calls
4. Special files
5. File formats and configuration files
6. Games
7. Miscellaneous
8. System administration commands

The exact sections available can vary between systems.

A section can be specified when opening a man page.

For example:

```bash
man 5 passwd
```

opens the documentation for the `passwd` file format.

Meanwhile:

```bash
man 1 passwd
```

opens the documentation for the `passwd` command, if that section is available.

---

# 41. Searching Man Pages

The `/` key can be used to search within an open man page.

For example, after running:

```bash
man ls
```

I can press `/` and enter:

```text
sort
```

Then I can press Enter to search.

The `n` key moves to the next match.

The `N` key moves to the previous match.

---

# 42. whatis

The `whatis` command provides a short description of a command or other documented item.

For example:

```bash
whatis ls
```

This is useful when I need a quick description rather than the full manual page.

---

# 43. apropos

The `apropos` command searches manual page descriptions and names using keywords.

For example:

```bash
apropos network
```

can return commands and documentation related to networking.

This is useful when I know what I want to accomplish but do not yet know the exact command.

---

# 44. whereis

The `whereis` command searches for locations associated with a command, such as its executable, source code, and manual page.

For example:

```bash
whereis ls
```

The exact output depends on what files are installed on the system.

---

# 45. locate

The `locate` command searches a pre-built database of file paths.

For example:

```bash
locate passwd
```

can return paths containing the term `passwd`.

Because `locate` relies on a database, newly created files may not appear until the database has been updated.

On systems that provide `updatedb`, an administrator can update the database with:

```bash
sudo updatedb
```

The exact availability and configuration of `locate` and `updatedb` depends on the Linux distribution and installed packages.

---

# Info Documentation

# 46. Info Pages

I also learned about the `info` command.

Info documentation is organized into interconnected sections called **nodes**.

It can provide more structured documentation than a short command reference.

For example:

```bash
info coreutils
```

may provide documentation for the GNU Coreutils collection on systems where the relevant Info documentation is installed.

Not every command has an Info document, so `info command` is not guaranteed to exist for every command.

---

# 47. Navigating Info Documentation

The Info reader provides keyboard shortcuts for navigating between nodes.

Some useful controls include:

- Arrow keys for navigation
- `u` to move up a level
- `l` to return to the previous location
- `q` to exit
- `h` for help

The exact behavior can depend on the Info reader and documentation being viewed.

---

# Other Sources of Help

# 48. The --help Option

Many Linux commands provide basic usage information through the `--help` option.

For example:

```bash
ls --help
```

This can display the command's syntax and available options.

The exact availability and format of `--help` depends on the command.

---

# 49. README Documentation

Linux software packages may include README files and other documentation.

These files can contain information about:

- Installation
- Configuration
- Usage
- Known issues
- Additional resources

Documentation can commonly be found under:

```text
/usr/share/doc
```

The exact files and directories available depend on the software installed and the Linux distribution.

---

# Commands and Concepts I Learned

| Command / Concept | What I Learned |
|---|---|
| `ls` | Lists directory contents |
| `echo` | Displays text or expanded variable values |
| `history` | Displays Bash command history |
| `env` | Displays environment variables |
| `export` | Marks variables for inheritance by child processes |
| `unset` | Removes a shell variable |
| `type` | Shows how Bash interprets a command |
| `which` | Commonly locates an executable in `PATH` |
| `command -v` | Reports how the shell resolves a command |
| `alias` | Displays or creates command aliases |
| `man` | Opens manual pages |
| `whatis` | Provides a brief description of a command |
| `apropos` | Searches manual page descriptions and names |
| `whereis` | Locates command-related files |
| `locate` | Searches a file-location database |
| `updatedb` | Updates the database used by `locate` on systems that provide it |
| `info` | Opens GNU Info documentation where available |
| `--help` | Provides command-specific usage information when supported |
| `PATH` | Contains directories searched for executable commands |
| `HOME` | Contains the user's home directory path |
| `HISTSIZE` | Controls the number of commands kept in Bash's history list |
| `;` | Runs commands sequentially |
| `&&` | Runs the next command if the previous command succeeds |
| `||` | Runs the next command if the previous command fails |
| `|` | Pipes standard output from one command to another |

---

# Key Takeaways from Week 2

My second week of Linux learning helped me understand the command line at a much deeper level.

The most important concepts I learned were:

1. The difference between open-source and closed-source software.
2. The purpose of software licenses.
3. The role of the GPL, FSF, OSI, FOSS, and FLOSS.
4. The purpose of Creative Commons licenses.
5. How Bash works as a command interpreter.
6. The basic structure of Linux commands.
7. The difference between options and arguments.
8. The importance of Linux case sensitivity.
9. How Bash command history works.
10. The difference between shell variables and environment variables.
11. The purpose of the `echo` command.
12. The purpose of the `PATH` variable.
13. The difference between shell built-ins and external commands.
14. How aliases and functions work.
15. How quoting affects Bash commands.
16. How command substitution works.
17. How `;`, `&&`, and `||` control command execution.
18. How pipes connect the output of one command to another.
19. How to use man pages and Info documentation.
20. How to search for commands and documentation.

---

# My Progress

During Week 2, I became more comfortable with the structure of Linux commands and started understanding how Bash processes what I type into the terminal.

I learned that using the command line is not simply about memorizing commands.

It also requires understanding how commands, options, arguments, variables, paths, aliases, functions, quoting, pipes, and control operators work together.

I also learned an important Linux skill: knowing how to find help.

Instead of trying to memorize every command and option, I can use built-in documentation tools such as:

```bash
man
whatis
apropos
whereis
info
```

and command-specific help such as:

```bash
command --help
```

This makes it possible to learn independently and troubleshoot unfamiliar commands.

---

# What I Want to Practice Next

After completing Week 2, I want to continue building practical command-line skills.

My next focus areas are:

- Practicing Linux commands in the terminal
- Working with files and directories
- Using command options and arguments
- Working with Bash variables
- Practicing pipes and command combinations
- Creating and using aliases
- Writing simple Bash functions
- Using man pages effectively
- Exploring Linux documentation independently
- Building simple Bash scripts

---

# Conclusion

Week 2 helped me move from simply learning about Linux to understanding how I can interact with a Linux system through the command line.

I learned that Bash provides much more than a place to enter commands. It provides variables, command history, aliases, functions, command substitution, quoting, and control operators.

I also learned that knowing how to find help is an essential Linux skill. Rather than trying to memorize every command and option, I can use Linux's built-in documentation to understand commands and solve problems.

This week gave me a stronger foundation for the practical Linux work I will continue learning in the coming weeks.

---

## Learning in Public

This repository documents my progress as I continue learning Linux, building command-line skills, and developing a stronger foundation in system administration and technology.
