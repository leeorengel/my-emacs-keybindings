# My Emacs keybindings

Essential keybindings to help users learning emacs coming from intelliJ IDEA or the Jetbrains family of IDE's.

This page assumes you are using my emacs config at http://github.com/leeorengel/.emacs.d

This page has been organized roughly in order of importance in terms of the minimum keybindings you need to know to get going in emacs. Subsequent sections include more advanced groupings of keybindings.

In terms of analogs to IntelliJ, this assumes you are on a Mac and using OS X 10.5+ Keymaps in IntelliJ.

**Table of Contents**

+ [Navigation](#navigation)
  - [Within buffer](#within-buffer)
    - [Basic Motion](#basic-motion)
    - [Jumping Around](#jumping-around)
    - [Jumping Around (Key Chords with Avy)](#jumping-around-key-chords-with-avy)
  - [Across buffers](#across-buffers)
+ [Selection/Copy/Paste](#selectioncopypaste)
  - [Advanced](#selection-advanced)
+ [Editing](#editing)
+ [Searching/Replacing](#searchingreplacing)
+ [File Management](#file-management)
+ [Directory Management](#directory-management)
+ [Window Management](#window-management)
  - [Windmove](#windmove)
+ [Frame Management](#frame-management)
+ [Projectile](#projectile)
+ [File Navigation (NeoTree)](#file-navigation-neotree)
+ [Multiple Cursors](#multiple-cursors)
+ [Coding](#coding)
+ [Jump to Definition (Dumb jump)](#jump-to-definition-dumb-jump)
+ [Smartparens](#smartparens)
+ [Clojure/CIDER](#clojurecider)
+ [Version Control (Magit)](#version-control-magit)
+ [Org Mode](#org-mode)
  - [TODO Lists](#todo-lists)
  - [Table Editing](#table-editing)
+ [Eshell](#eshell)
+ [Minibuffer](#minibuffer)
+ [Markdown](#markdown)
+ [Workgroups](#workgroups)
+ [Help](#help)
+ [Miscellaneous](#miscellaneous)
+ [Credits](#credits)

## Navigation

### Within a buffer

#### Basic Motion

Keybindings for very basic cursor movement.

| Keybinding       | Description                      |
|------------------|----------------------------------|
| <kbd>C-p</kbd>   | move cursor to previous line     |
| <kbd>C-n</kbd>   | move cursor to next line         |
| <kbd>M-b</kbd>   | move cursor to previous word     |
| <kbd>M-f</kbd>   | move cursor to next word         |
| <kbd>C-M-b</kbd> | move cursor to next s-expression |
| <kbd>C-M-f</kbd> | move cursor to next s-expression |
| <kbd>C-a</kbd>   | Go to beginning of line          |
| <kbd>C-e</kbd>   | Go to end of line                |

#### Jumping Around

Keybindings for jumping around inside a single buffer.

| Keybinding     | Description                            | Notes             |
|----------------|----------------------------------------|-------------------|
| <kbd>C-[</kbd> | Previous cursor position within buffer | Custom keybinding |
| <kbd>C-]</kbd> | Next cursor position within buffer     | Custom keybinding |
| <kbd>M-<</kbd> | Go to beginning of buffer              |                   |
| <kbd>M-></kbd> | Go to end of buffer                    |                   |
| <kbd>M-l</kbd> | Go to line number                      | Custom keybinding |
| <kbd>C-l</kbd> | Center screen at cursor/point          |                   |
| <kbd>M-v</kbd> | Scroll to previous screen              |                   |
| <kbd>C-v</kbd> | Scroll to next screen                  |                   |

#### Jumping Around (Key chords with Avy)

| Keybinding    | Description                                                       | Notes |
|---------------|-------------------------------------------------------------------|-------|
| <kbd>jj</kbd> | Jump to the beginning of a word (`avy-goto-char`)                 |       |
| <kbd>jk</kbd> | Jump to character (`avy-goto-char-2`)                             |       |
| <kbd>jl</kbd> | Jump to the beginning of a line (`avy-goto-word-1`)               |       |
| <kbd>xx</kbd> | Executed extended command(`execute-extended-command`)             |       |

### Across buffers

Keybindings for moving in between open buffers.

| Keybinding             | Description          |
|------------------------|----------------------|
| <kbd>C-x <left></kbd>  | Previous buffer/file |
| <kbd>C-x <right></kbd> | Next buffer/file     |

## Selection/Copy/Paste

Commands for selecting, cutting, copying and pasting regions of text.

| Keybinding         | Description                                      |
|--------------------+--------------------------------------------------|
| <kbd>C-SPACE</kbd> | Mark the beginning of a selection                |
| <kbd>C-x C-x</kbd> | Toggle between beginning and ending of selection |
| <kbd>M-w</kbd>     | Copy selection                                   |
| <kbd>C-w</kbd>     | Cut and copy selection                           |
| <kbd>C-y</kbd>     | Paste (yank from kill ring)                      |
| <kbd>C-=</kbd>     | Increase region selection (via `expand-region`)  |
| <kbd>C-x h</kbd>   | Select entire buffer region                      |

### Selection advanced

| Keybinding       | Description         | Notes |
|------------------|---------------------|-------|
| <kbd>C-M-@</kbd> | Select s-expression |       |
| <kbd>C-M-h</kbd> | Select function     |       |

## Editing

Keybindings for making changes within a buffer.

| Keybinding             | Description                                              | Notes                                                                 |
|------------------------|----------------------------------------------------------|-----------------------------------------------------------------------|
| <kbd>C-/</kbd>         | Undo                                                     |                                                                       |
| <kbd>C-S-/</kbd>       | Redo                                                     |                                                                       |
| <kbd>C-x u</kbd>       | Undo tree visualize                                      |                                                                       |
| <kbd>C-Shift-Del</kbd> | Delete current line                                      |                                                                       |
| <kbd>C-k</kbd>         | Delete rest of line from cursor                          |                                                                       |
| <kbd>M-0 C-k</kbd>     | Delete from cursor to beginning of line                  |                                                                       |
| <kbd>M-Del</kbd>       | Delete previous word                                     |                                                                       |
| <kbd>M-d</kbd>         | Delete next word                                         |                                                                       |
| <kbd>C-c d</kbd>       | Duplicate current line                                   |                                                                       |
| <kbd>C-x C-t</kbd>     | Swap line with line above                                |                                                                       |
| <kbd>M-z</kbd>         | delete up to char                                        | Keep hitting char to go to next occurrence. <kbd>C-K</kbd> to delete. |
| <kbd>M-\\</kbd>        | delete all surrounding whitespace and tabs around cursor |                                                                       |

### Transposing

| Keybinding       | Description             |
|------------------|-------------------------|
| <kbd>M-t l</kbd> | Transpose lines         |
| <kbd>M-t w</kbd> | Transpose words         |
| <kbd>M-t s</kbd> | Transpose s-expressions |
| <kbd>M-t p</kbd> | Transpose params        |


## Searching/Replacing

| Keybinding       | Description                                |
|------------------|--------------------------------------------|
| <kbd>C-s</kbd>   | Find next occurrence in buffer             |
| <kbd>C-r</kbd>   | Find previous occurrence in buffer         |
| <kbd>C-M-s</kbd> | Find next occurrence using regex in buffer |
| <kbd>C-M-r</kbd> | Find previous occurrence in buffer         |


## File Management

| Keybinding                    | Description                       | Notes             |
|-------------------------------|-----------------------------------|-------------------|
| <kbd>C-x b <name> RET</kbd>   | Create a new/open recent buffer   |                   |
| <kbd>C-x 4 b <name> RET</kbd> | Create a new buffer in new window |                   |
| <kbd>C-x C-f</kbd>            | Open a file                       |                   |
| <kbd>C-x f</kbd>              | Open recent file                  |                   |
| <kbd>C-x k RET</kbd>          | Close buffer                      |                   |
| <kbd>C-x C-s</kbd>            | Save buffer                       |                   |
| <kbd>C-x C-w <name> RET</kbd> | Save buffer to file               |                   |
| <kbd>C-c D</kbd>              | Delete current buffer & file      | custom keybinding |
| <kbd>M-x <mode-name></kbd>    | Enable mode in file               |                   |

## Directory Management

| Keybinding                            | Description                                       | Notes |
|---------------------------------------|---------------------------------------------------|-------|
| <kbd>C-x d</kbd>                      | Open Dired                                        |       |
| <kbd><</kbd>                          | Previous directory in listing (skips files)       |       |
| <kbd>></kbd>                          | Next directory in listing (skips files)           |       |
| <kbd>f</kbd>                          | Open file                                         |       |
| <kbd>v</kbd>                          | View file                                         |       |
| <kbd>^</kbd>                          | Go up to parent directory                         |       |
| <kbd>d</kbd>                          | Mark file for deletion                            |       |
| <kbd>x</kbd>                          | Delete files marked for deletion                  |       |
| <kbd>q</kbd>                          | Quit                                              |       |
| <kbd>+</kbd>                          | Create directory                                  |       |
| <kbd>=</kbd>                          | Compare file at point with previously marked file |       |
| <kbd>m</kbd>                          | Mark a file for action                            |       |
| <kbd>u</kbd>                          | Unmark a file for action                          |       |
| <kbd>t</kbd>                          | Toggle marking                                    |       |
| <kbd>! \<shell command string\></kbd> | Run shell command on file at cursor               |       |

## Window Management

| Keybinding                  | Description                                   | Notes               |
|-----------------------------|-----------------------------------------------|---------------------|
| <kbd>C-x 1</kbd>            | Close all other windows except current window |                     |
| <kbd>C-x 2</kbd>            | Split current window horizontally             |                     |
| <kbd>C-x 3</kbd>            | Split current window vertically               |                     |
| <kbd>C-x 0</kbd>            | Close current window                          |                     |
| <kbd>C-x o</kbd>            | Switch to next window                         |                     |
| <kbd>M-- C-x o</kbd>        | Switch to previous window                     |                     |
| <kbd>M-<number> C-x o</kbd> | Jump ahead # of windows                       |                     |
| <kbd>C-M-Shift-v</kbd>      | Scroll backward other window                  |                     |
| <kbd>C-M-v</kbd>            | Scroll forward other window                   |                     |
| <kbd>C-x {</kbd>            | Shrink window narrower                        |                     |
| <kbd>C-x }</kbd>            | Grow window wider                             |                     |
| <kbd>C-TAB</kbd>            | Number windows and jump by number             | via `switch window` |

### Windmove

| Keybinding             | Description                                   |
|------------------------|-----------------------------------------------|
| <kbd>S-\<left\></kbd>  | Move to window to the left of current window  |
| <kbd>S-\<right\></kbd> | Move to window to the right of current window |
| <kbd>S-\<up\></kbd>    | Move to window above current window           |
| <kbd>S-\<down\></kbd>  | Move to window below current window           |

## Frame Management

| Keybinding         | Description                                 | Notes |
|--------------------|---------------------------------------------|-------|
| <kbd>C-x 5 1</kbd> | Close all other frames except current frame |       |
| <kbd>C-x 5 2</kbd> | Split current frame horizontally            |       |
| <kbd>C-x 5 0</kbd> | Close current frame                         |       |
| <kbd>C-x 5 o</kbd> | Switch to next frame                        |       |
| <kbd>C-x C-n</kbd> | Create new frame                            |       |

## Projectile

Project navigation. An alternate prefix is Command-P.

| Keybinding                                         | Description                                 | Notes             |
|----------------------------------------------------|---------------------------------------------|-------------------|
| <kbd>M-S-o</kbd> (default is <kbd>C-c p f</kbd>)   | Open file in project with completion        | Custom keybinding |
| <kbd>M-S-f</kbd> (default is <kbd>C-c p s s</kbd>) | Search all files in project using regex     | Custom keybinding |
| <kbd>M-e</kbd> (defualt is <kbd>C-c p e</kbd>)     | Show all recent opened files in project     | Custom keybinding |
| <kbd>C-c p F</kbd>                                 | Open file in ANY project with completion    |                   |
| <kbd>C-c p r</kbd>                                 | Find/replace all files in project           |                   |
| <kbd>C-c p b</kbd>                                 | Show all open project buffers               |                   |
| <kbd>C-c p p</kbd>                                 | Switch between known projects               |                   |
| <kbd>C-c p D</kbd>                                 | Open root project in dired                  |                   |
| <kbd>C-c p k</kbd>                                 | Kill all buffers in project                 |                   |
| <kbd>C-c p !</kbd>                                 | Run shell on root of project as current dir |                   |
| <kbd>C-c p p</kbd>                                 | Show all known projects                     |                   |

## File Navigation (NeoTree)

| Keybinding         | Description                                        | Notes                    |
|--------------------|----------------------------------------------------|--------------------------|
| <kbd>\<f8\></kbd>  | Toggle project explorer                            |                          |
| <kbd>C-c C-n</kbd> | Create a new file or dir if filename ends with '/' | (when in neotree buffer) |
| <kbd>C-c C-d</kbd> | Delete a file or a directory                       | (when in neotree buffer) |
| <kbd>C-c C-r</kbd> | Rename a file or a directory                       | (when in neotree buffer) |
| <kbd>g</kbd>       | Refresh project explorer                           | (when in neotree buffer) |
| <kbd>H</kbd>       | Toggle showing hidden files                        | (when in neotree buffer) |

## Multiple Cursors

See [https://github.com/magnars/multiple-cursors.el](https://github.com/magnars/multiple-cursors.el)

| Keybindings            | Description                                  | Notes              |
|------------------------|----------------------------------------------|--------------------|
| <kbd>C-S-c C-S-c</kbd> | Mark consecutive lines with multiple cursors | First select lines |
| <kbd>C-<</kbd>         | Mark previous occurrence of word             | First select word  |
| <kbd>C-></kbd>         | Mark next occurrence of word                 | First select word  |
| <kbd>C-c C-<</kbd>     | Mark all occurrences like selection          |                    |

## Coding

| Keybinding         | Description                                 | IntelliJ IDEA    |
|--------------------|---------------------------------------------|------------------|
| <kbd>C-,</kbd>     | Auto-complete at point                      | <kbd>M-SPC</kbd> |
| <kbd>C-x C-i</kbd> | List definitions in file and jump           | <kbd>M-F12</kbd> |
| <kbd>C-c p c</kbd> | Run compile on project                      |                  |
| <kbd>C-c p P</kbd> | Run tests on project                        |                  |
| <kbd>C-c p t</kbd> | Toggle between implementation and test file |                  |

## Smartparens

| Keybinding                    | Description                                                                     | Notes                                                                                                  |
|-------------------------------|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <kbd>C-M-b</kbd>              | Move backward one s-expression                                                  | Must be on a paren, otherwise behaves like backward word                                               |
| <kbd>C-M-f</kbd>              | Move forward one s-expression                                                   | Must be on a paren, otherwise behaves like forward word                                                |
| <kbd>C-M-d</kbd>              | Move down to next nested s-expression                                           |                                                                                                        |
| <kbd>C-M-n</kbd>              | Move up s-expression                                                            |                                                                                                        |
| <kbd>C-M-u</kbd>              | Move up one level in nested s-expression                                        | Requires fix for OSX interception of the keybinding (see http://emacs.stackexchange.com/a/20544/11397) |
| <kbd>C-(</kbd>,<kbd>C-{</kbd> | Pull in or out previous word/s-expression into current s-expression             |                                                                                                        |
| <kbd>C-)</kbd>,<kbd>C-}</kbd> | Pull in or out next word/s-expression into current s-expression                 |                                                                                                        |
| <kbd>M-S</kbd>                | Split current s-expression into two separate ones with cursor as split point    |                                                                                                        |
| <kbd>M-s</kbd>                | Remove parens immediately surrounding cursor point                              |                                                                                                        |
| <kbd>M-[up arrow]</kbd>       | Remove all chars before cursor point inside s-expression and surrounding parens |                                                                                                        |
| <kbd>M-[down arrow]</kbd>     | Remove all chars after cursor point inside s-expression and surrounding parens  |                                                                                                        |
| <kbd>M-r</kbd>                | Remove all chars around cursor point inside s-expression and surrounding parens |                                                                                                        |


## Clojure/CIDER

| Keybinding                        | Description                                | Notes                                                                 |
|-----------------------------------|--------------------------------------------|-----------------------------------------------------------------------|
| <kbd>C-c RET</kbd>                | clj refactor prefix                        | See [commands](https://github.com/clojure-emacs/clj-refactor.el/wiki) |
| <kbd>C-c M-j</kbd>                | Open nREPL in a clojure project            |                                                                       |
| <kbd>,</kbd>                      | Once repl is open, get command keybindings |                                                                       |
| <kbd>C-c C-t n</kbd>              | Run tests in current ns                    |                                                                       |
| <kbd>C-c C-t t</kbd>              | Run a test at the cursor position          |                                                                       |
| <kbd>C-u C-M-x</kbd>              | Start debug session                        |                                                                       |
| <kbd>M-x clojure-cheatsheet</kbd> | Clojure command cheatsheet                 |                                                                       |

## Jump to Definition (Dumb jump)

| Keybinding       | Description                      | Notes |
|------------------|----------------------------------|-------|
| <kbd>C-M-g</kbd> | Jump to definition               |       |
| <kbd>C-M-q</kbd> | Jump to definition (with dialog) |       |

## Version Control (Magit)

| Keybinding                                 | Description                          |
|--------------------------------------------|--------------------------------------|
| <kbd>C-x m</kbd>                           | See current git status/changed files |
| <kbd>g</kbd>                               | Reload status buffer                 |
| <kbd>c c, \<write message\>, C-c C-c</kbd> | Commit file                          |
| <kbd>P u</kbd>                             | Push changes to remote               |
| <kbd>F u</kbd>                             | Pull latest changes                  |
| <kbd>s</kbd>                               | Stage file                           |
| <kbd>u</kbd>                               | Unstage file                         |
| <kbd>b b</kbd>                             | Switch branch                        |
| navigate to file, then <kbd>TAB</kbd>      | Version diff                         |
| <kbd>k</kbd>                               | revert changes                       |
| <kbd>l l</kbd>                             | Show log                             |
| <kbd>b</kbd>                               | Switch to branch                     |
| <kbd>B</kbd>                               | Create a new branch                  |
| <kbd>z</kbd>                               | Stash changes                        |
| <kbd>A</kbd>                               | Unstash changes                      |
| <kbd>i</kbd>                               | Ignore file(s)                       |
| <kbd>C-u i</kbd>                           | Ignore directory                     |
| <kbd>I</kbd>                               | Exclude file(s)                      |
| <kbd>M-x magit-clone</kbd>                 | Clone a repo                         |
| <kbd>q</kbd>                               | Quit                                 |

## Eshell

| Keybinding         | Description                                   |
|--------------------|-----------------------------------------------|
| <kbd>C-z</kbd>     | Open eshell                                   |
| <kbd>M-p</kbd>     | Go back in command history                    |
| <kbd>M-n</kbd>     | Go forward in command history                 |
| <kbd>C-c C-r</kbd> | Clear the shell buffer                        |
| <kbd>M-r</kbd>     | search backwars in command history with regex |
| <kbd>M-s</kbd>     | search forward in command history with regex  |
| <kbd>!!</kbd>      | Repeats the last command                      |
| <kbd>!ls</kbd>     | Repeats the last commnd starting with ls      |

## Org mode

### TODO Lists

| Keybinding                                | Description                                     |
|-------------------------------------------|-------------------------------------------------|
| <kbd>C-c C-p</kbd>                        | Move up a heading                               |
| <kbd>C-c C-n</kbd>                        | Move down a heading                             |
| <kbd>C-c C-b</kbd>                        | Move up a heading, same level                   |
| <kbd>C-c C-f</kbd>                        | Move down a heading, same level                 |
| <kbd>TAB</kbd>                            | Toggle heading open/closed states               |
| <kbd>S-TAB</kbd>                          | Toggle entire buffer heading open/closed states |
| <kbd>M-\<down\></kbd>                     | Move heading down                               |
| <kbd>M-\<up\></kbd>                       | Move heading up                                 |
| <kbd>M-\<left\></kbd>                     | Promote heading                                 |
| <kbd>M-\<right\></kbd>                    | Demote heading                                  |
| <kbd>C-RET</kbd>                          | New heading                                     |
| <kbd>M-RET</kbd>                          | New list item entry                             |
| <kbd>/</kbd>                              | Search inside org mode                          |
| <kbd>C-c -</kbd>                          | Cycle item type                                 |
| <kbd>S-<left></kbd>, <kbd>S-<right></kbd> | Cycle state of `TODO` item                      |

### Table Editing

| Keybinding               | Description                                       |
|--------------------------|---------------------------------------------------|
| <kbd>C-c &#124;</kbd>    | Convert active region into a table                |
| <kbd>C-c C-c             | Re-align table                                    |
| <kbd>TAB</kbd>           | Re-align the table and move to the next field     |
| <kbd>S-TAB</kbd>         | Re-align the table and move to the previous field |
| <kbd>&#124; RET</kbd>    | Insert new column to the right                    |
| <kbd>RET</kbd>           | Re-align the table and move to the next row       |
| <kbd>C-c SPC</kbd>       | Blank the table cell at cursor                    |
| <kbd>C-c -</kbd>         | Insert a horizontal rule on next line             |
| <kbd>M-\<left\></kbd>    | Move column at cursor to the left                 |
| <kbd>M-\<right\></kbd>   | Move column at cursor to the right                |
| <kbd>M-S-\<left\></kbd>  | kill current column                               |
| <kbd>M-S-\<right\></kbd> | Insert a new column to the left of the cursor     |
| <kbd>M-S-\<up\></kbd>    | Kill the current table row                        |
| <kbd>M-S-\<down\></kbd>  | Insert new row above current row                  |

## Help

| Keybinding                                   | Description                                                   | Notes             |
|----------------------------------------------|---------------------------------------------------------------|-------------------|
| <kbd>M-x describe-key</kbd>                  | Tell which function is bound to key combo                     |                   |
| <kbd>C-h b</kbd>                             | All active keybindings with flx-ido narrowing                 | Custom keybinding |
| <kbd>C-h a \<topics\> RET</kbd>              | Search help system for matches to <topics>                    |                   |
| <kbd>type key prefix</kbd> and wait 1 second | Get remaining completion options                              | via `which-key`   |
| <kbd>C-h m</kbd>                             | Display documentation of the current major mode               |                   |
| <kbd>C-h f</kbd>                             | Run `help-apropos`, an interactive version of apropos-command |                   |

## Workgroups

| Keybinding           | Description                          | Notes |
|----------------------|--------------------------------------|-------|
| <kbd>C-c z C-s</kbd> | Save current session for workgroup   |       |
| <kbd>C-c z C-f</kbd> | Load a session for a given workgroup |       |
| <kbd>C-c z c</kbd>   | Create a new workgroup               |       |
| <kbd>C-c z v</kbd>   | Switch to a workgroup                |       |

## Markdown

Reference: http://ddloeffler.blogspot.ca/2013/04/keybindings-for-emacs-markdown-mode.html

| Keybinding           | Description                | Notes |
|----------------------|----------------------------|-------|
| <kbd>C-c C-t h</kbd> | Create heading             |       |
| <kbd>C-c C-a l</kbd> | Create link                |       |
| <kbd>C-c C-a L</kbd> | Create anchor link         |       |
| <kbd>C-c C-s e</kbd> | Italisize selection/region |       |
| <kbd>C-c C-s s</kbd> | Bold selection/region      |       |
| <kbd>C-c -</kbd>     | Horizontal rule            |       |

## Minibuffer

Keybindings for use inside the minibuffer.

| Keybinding                               | Description                                   | Notes |
|------------------------------------------|-----------------------------------------------|-------|
| <kbd>TAB</kbd>                           | Auto-complete as much as possible             |       |
| <kbd>SPACE</kbd>                         | Complete up to one word                       |       |
| <kbd>RET</kbd>                           | Complete and execute                          |       |
| <kbd>?</kbd>                             | Show completion possibilities                 |       |
| <kbd>M-r</kbd>                           | Regex search backward through command history |       |
| <kbd>M-s</kbd>                           | Regex search forward through command history  |       |
| <kbd>C-g</kbd> or <kbd>Esc Esc Esc</kbd> | Abort current command                         |       |

## Miscellaneous

| Keybinding                                  | Description                      | Notes                                        |
|---------------------------------------------|----------------------------------|----------------------------------------------|
| <kbd>M-x ediff</kbd>                        | Diff Files                       |                                              |
| <kbd>C-x v =</kbd>                          | View diff of current file        |                                              |
| <kbd>M-x procd</kbd>                        | View processes (like top)        | OR <kbd>C-x</kbd> p (with global keybinding) |
| <kbd>C-x d</kbd>                            | File browser (dired)             |                                              |
| <kbd>C-x g</kbd>                            | Search in Web hooks              | custom binding                               |
| <kbd>C-c u</kbd>                            | View URL                         |                                              |
| <kbd>C-x C-f /remotehost:filename RET</kbd> | TRAMP remote file editing        | Open a directory to get a Dired buffer!      |
| <kbd>M-$</kbd>                              | Check and fix spelling at cursor |                                              |

## Credits

- [Magnar Sveen](https://github.com/magnars/.emacs.d)
- [Bozhidar Batsov's favourite keybindings](http://stackoverflow.com/a/3125243/3166303)
- [Awesome Emacs](https://github.com/emacs-tw/awesome-emacs)
