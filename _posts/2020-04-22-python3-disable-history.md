---
title: "How to disable history on Python 3"
categories: comp python
description: "How to disable the Python 3 interpreter logging to .python_history on Linux."
---

Since Python 2 was deprecated at the beginning of 2020, you may have noticed
that the Python 3 interpreter logs a history of all commands to
`.python_history`. This has been enabled by default since Python 3.4 and is
remarkably difficult to disable ([bug #20866](https://bugs.python.org/issue20886)),
and the official documentation is not much help.

The following method has been tested in Ubuntu and will prevent the `python3`
interpreter from creating or updating the `.python_history` file, but you should
retain the command history during a session as normal in Python 2.

## Method

### Step 1: Enable .pythonrc

Your first problem is that the Python interpreter's settings file is not enabled
by default ([bug #8919](https://bugs.python.org/issue8919)).

In your `.bashrc` or `.bash_aliases` file in your homedir, insert the following
instruction:

    export PYTHONSTARTUP=~/.pythonrc

### Step 2: Restart terminal

If you have a terminal window open at this point, you will need to restart it
for the new environment variables to take effect.

### Step 3: Edit .pythonrc

Create a file called `.pythonrc` in your homedir containing the following:

    import readline
    readline.write_history_file = lambda *args: None

Credit to this goes to [Waxrat](https://unix.stackexchange.com/a/297834)
at Unix & Linux Stack Exchange.

### Step 4: Delete .python_history

Delete the .python_history file in your homedir.

### Step 5: Check if successful

Load up `python3`, enter some commands, exit, and check if the `.python_history`
file exists. If it does not, you have been successful.
