# Ultimate Vim Cheat Sheet: Learn to Use Vim Like a Pro

Since the 1970s, Vi and Vim are popular amongst developers and are present on most UNIX-based servers.

These free and open source modal text editors can be a bit hard to use at first, but they are extremely powerful.

Here is our ultimate Vim Cheat Sheet, featuring over 150 commands to supercharge your coding with Vi/Vim.

**Table of Contents** [show](https://catswhocode.com/vim-cheat-sheet/#) 

## A Quick Intro to Vim

Vi is a modal text editor first released in 1976 for Unix systems. Vim, (Vi Improved) Vi’s successor, was first released in 1991. Despite its very old age, Vim is extremely popular among web developers and system administrators, as it is installed by default on all Unix-based systems (Mac OS and Linux distros).Unlike classic text editors, Vim features different modes used for different operations. Vim has a total of 12 modes, although you will mostly use the following:

- **Insert Mode:** This mode is used to insert text by typing, like you would do on any other text editor. To enter insert mode, type `i` while in command mode.
- **Command Mode:** Also named *Normal Mode*, this mode is used to type Vim commands such as those you’ll find in our Vim Cheat Sheet. To exit insert mode and enter command mode, hit the `Esc` key of your keyboard.
- **Visual Mode:** Similar to command mode, but used to highlight areas of text. Normal commands are run on the highlighted area, which, for instance, can be used to move or edit a selection. Press the `v` key to start visual mode. To exit visual mode, press the `Esc` key.

## Basics

Let’s start with basic commands that will allow you to write, save and quit files. Remember that these Vim commands need to be typed while in command or visual mode. Exit insert mode by hitting the Esc key, then type the command of your choice.

| :e filename   | Open *filename* for edition                         |
| ------------- | --------------------------------------------------- |
| :w            | Save file                                           |
| :q            | Exit Vim                                            |
| :q!           | Quit without saving current file                    |
| :x            | Write/Save file (if changes has been made) and exit |
| :sav filename | Save current file as *filename*                     |
| .             | Repeat the last change made in normal mode          |
| 5.            | Repeat 5 times the last change made in normal mode  |

## Moving In The File

Vim features powerful commands that allow you to easily move the cursor position to any desired location within the current file, making it quick and easy to insert text.

| k or Up Arrow   | move cursor up one line                                      |
| --------------- | ------------------------------------------------------------ |
| j or Down Arrow | move cursor down one line                                    |
| e               | move cursor to the end of the word                           |
| b               | move the cursor to the beginning of the word                 |
| 0               | move the cursor to the first non-blank character of the line |
| G               | move the cursor to the end of the file                       |
| gg              | move the cursor position to the beginning of the file        |
| L               | move the cursor to the bottom of the screen                  |
| :59             | move cursor to line *59*. Replace *59* by the desired line number. |
| %               | Move cursor to matching parenthesis                          |
| [[              | Jump to function start                                       |
| [{              | Jump to block start                                          |

## Cut, Copy & Paste

Vim features powerful functions to cut, copy, and paste. This section of our Vim Cheat Sheet will show you how to easily perform those operations. Please note that `y` stands for *yank* in Vim, which in other editors is usually called copy.

| y    | Yank/Copy the selected text to clipboard |
| ---- | ---------------------------------------- |
| p    | Paste clipboard contents                 |
| dd   | Cut current line                         |
| yw   | Yank/Copy word                           |
| yy   | Yank/Copy current line                   |
| y$   | Yank/Copy to end of line                 |
| D    | Cut to end of line                       |

## Search

Searching a string within a huge file or multiple files can be tricky. Thanks to Vim, using a few commands you can easily find whatever you’re looking for.

| /word                              | Search *word* from top to bottom                             |
| ---------------------------------- | ------------------------------------------------------------ |
| ?word                              | Search *word* from bottom to top                             |
| *                                  | Search the word under cursor                                 |
| /\cstring                          | Search *STRING* or *string*, case insensitive                |
| /jo[ha]n                           | Search *john* or *joan*                                      |
| /\< the                            | Search the, theatre or *then*                                |
| /the\>                             | Search *the* or *breathe*                                    |
| /\< the\>                          | Search *the*                                                 |
| /\< ¦.\>                           | Search all words consisting of 4 letters                     |
| /\/                                | Search *fred* but not *alfred* or *frederick*                |
| /fred\|joe                         | Search *fred* or *joe*                                       |
| /\<\d\d\d\d\>                      | Search exactly 4 digits                                      |
| /^\n\{3}                           | Find 3 empty lines                                           |
| :bufdo /searchstr/                 | Search in multiple files                                     |
| bufdo %s/something/somethingelse/g | Search *something* in all the open buffers and replace it with *somethingelse* |

## Replace

Similar to *Search*, Vim features powerful commands to replace any given text. This part of our cheat sheet contains Vim commands for replacing any portion of text with another.

| :%s/old/new/g         | Replace all occurences of *old* with *new* in file           |
| --------------------- | ------------------------------------------------------------ |
| :%s/onward/forward/gi | Replace onward with forward, case insensitive                |
| :%s/old/new/gc        | Replace all occurences with confirmation                     |
| :2,35s/old/new/g      | Replace all occurences between lines 2 and 35                |
| :5,$s/old/new/g       | Replace all occurences from line 5 to EOF                    |
| :%s/^/hello/g         | Replace the beginning of each line by *hello*                |
| :%s/$/Harry/g         | Replace the end of each line by *Harry*                      |
| :%s/onward/forward/gi | Replace *onward* with *forward*, case insensitive            |
| x                     | Delete character                                             |
| :%s/ *$//g            | Delete all white spaces and keep any non-blank character     |
| :g/string/d           | Delete all lines containing *string*                         |
| :v/string/d           | Delete all lines not containing *string*                     |
| :s/Bill/Steve/        | Replace the first occurrence of *Bill* with *Steve* in current line |
| :s/Bill/Steve/g       | Replace *Bill* with *Steve* in current line                  |
| :%s/Bill/Steve/g      | Replace *Bill* with *Steve* in all of the file               |
| :%s/^M//g             | Delete DOS carriage returns (^M)                             |
| :%s/\r/\r/g           | Transform DOS carriage returns in returns                    |
| :%s#<[^>]\+>##g       | Delete HTML tags but keep text                               |
| :%s/^\(.*\)\n\1$/\1/  | Delete lines that appear twice                               |
| Ctrl+a                | Increment number under the cursor                            |
| Ctrl+x                | Decrement number under cursor                                |
| ggVGg?                | Change text to Rot13                                         |

## Case

Vim provides very interesting commands to deal with case. Let’s continue to explore our Vim Cheat Sheet with super useful case-related commands.

| Vu              | Lowercase line                                               |
| --------------- | ------------------------------------------------------------ |
| VU              | Uppercase line                                               |
| g~~             | Invert case                                                  |
| vEU             | Switch word to uppercase                                     |
| vE~             | Modify word case                                             |
| ggguG           | Set all text to lowercase                                    |
| gggUG           | Set all text to uppercase                                    |
| :set ignorecase | Ignore case in searches                                      |
| :set smartcase  | Ignore case in searches except if an uppercase letter is used |
| :%s/\<./\u&/g   | Sets the first letter of each word to uppercase              |
| :%s/\<./\l&/g   | Sets the first non-blank character of each word to lowercase |
| :%s/.*/\u&      | Sets the first character of the line to uppercase            |
| :%s/.*/\l&      | Sets the first character of the line to lowercase            |

## Read and Write Files

Vim allows easy manipulation of files. Listed below are a few examples of file manipulation with Vim.

| :1,10 w outfile    | Save lines 1 to 10 in *outfile*              |
| ------------------ | -------------------------------------------- |
| :1,10 w >> outfile | Append lines 1 to 10 to *outfile*            |
| :r infile          | Insert the content of *infile*               |
| :23r infile        | Insert the content of *infile* under line 23 |

## File Explorer

Vim features a built-in file explorer that allows its users to quickly visualize and open files in the editor.

| :e .                   | Open integrated file explorer                      |
| ---------------------- | -------------------------------------------------- |
| :Sex                   | Split window and open integrated file explorer     |
| :Sex!                  | Same as *:Sex* but splits window vertically        |
| :browse e              | Graphical file explorer                            |
| :ls                    | List buffers                                       |
| :cd ..                 | Move to parent directory                           |
| :args                  | List files                                         |
| :args *.php            | Open file list                                     |
| :grep expression *.php | Return a list of .php files contening *expression* |
| gf                     | Open file name under cursor                        |

## Interacting With Unix

As Vi and Vim were initially built for Unix systems, the text editor can interact with the OS.

| :!pwd | Execute the *pwd* Unix command, then return to Vi        |
| ----- | -------------------------------------------------------- |
| !!pwd | Execute the *pwd* unix command and insert output in file |
| :sh   | Temporary return to Unix                                 |
| $exit | Return to Vi                                             |

## Alignment

Using Vim, it’s possible to automatically align lines using a few simple commands. Here are the main important ones:

| :%!fmt | Align all lines                         |
| ------ | --------------------------------------- |
| !}fmt  | Align all lines at the current position |
| 5!!fmt | Align the next 5 lines                  |

## Tabs and Windows

Vim can use various tabs and windows, which is very useful for working with many files at once.

| :tabnew             | Create/Open a new tab                           |
| ------------------- | ----------------------------------------------- |
| gt                  | Show next tab                                   |
| :tabfirst           | Show first tab                                  |
| :tablast            | Show last tab                                   |
| :tabm n(position)   | Rearrange tabs                                  |
| :tabdo %s/foo/bar/g | Execute a command in all tabs                   |
| :tab ball           | Puts all open files in tabs (Each in a new tab) |
| :new abc.txt        | Edit *abc.txt* in new window                    |

## Window Spliting

As a web developer, I always like to split my Vim editor in two parts, one for my HTML and one for my CSS stylesheet. This part of our Vim Cheat Sheet describes how to split the main editor window.

| :e filename     | Edit *filename* in current window    |
| --------------- | ------------------------------------ |
| :split filename | Split the window and open *filename* |
| ctrl-w up arrow | Put cursor in top window             |
| ctrl-w ctrl-w   | Put cursor in next window            |
| ctrl-w_         | Maximize current window vertically   |
| ctrl-w\|        | Maximize current window horizontally |
| ctrl-w=         | Gives the same size to all windows   |
| 10 ctrl-w+      | Add 10 lines to current window       |
| :vsplit file    | Split window vertically              |
| :sview file     | Same as **:split** in Read Only Mode |
| :hide           | Close current window                 |
| :­nly           | Close all windows, except current    |
| :b 2            | Open #2 in this window               |

## Auto Completion

Like much more modern editors, Vim can auto-complete your code and use dictionaries.

| Ctrl+N Ctrl+P (in insert mode) | Complete word                 |
| ------------------------------ | ----------------------------- |
| Ctrl+x Ctrl+l                  | Complete line                 |
| :set dictionary=dict           | Define *dict* as a dictionary |
| Ctrl+x Ctrl+k                  | Complete with dictionary      |

## Markers

Vim allows its users to set marks at a position of their choice, so they can easily jump back to that predefined position. A must when working with large files.

| m {a-z} | Marks current position as *{a-z}* |
| ------- | --------------------------------- |
| ‘ {a-z} | Move to position *{a-z}*          |
| ”       | Move to previous position         |

## Abbreviations

Another handy Vim function is the possibility to define abbreviations.

| :ab mail mail@provider.org | Define *mail* as abbreviation of *mail@provider.org* |
| -------------------------- | ---------------------------------------------------- |
|                            |                                                      |

## Text Indent

Indentation is the key to readable and easy-to-maintain code. Vim possesses a few commands that will come in handy for indenting any file.

| :set autoindent   | Turn on auto-indent                 |
| ----------------- | ----------------------------------- |
| :set smartindent  | Turn on intelligent auto-indent     |
| :set shiftwidth=4 | Define 4 spaces as indent size      |
| ctrl-t, ctrl-d    | Indent/un-indent in insert mode     |
| >>                | Indent                              |
| <<                | Un-indent                           |
| =%                | Indent the code between parenthesis |
| 1GVG=             | Indent the whole file               |

## Syntax Highlighting

Syntax highlighting is often very useful for preventing coding mistakes and typos. Vim can work with many different syntax highlighting modes, depending on which programming language you are coding with.

| :syntax on       | Turn on syntax highlighting  |
| ---------------- | ---------------------------- |
| :syntax off      | Turn off syntax highlighting |
| :set syntax=perl | Force syntax highlighting    |