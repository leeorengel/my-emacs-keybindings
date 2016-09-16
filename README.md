# My Emacs keybindings

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
  - [Expand-region](#expand-region)
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
+ [Smartparens](#smartparens)
  - [Navigation](#smartparens-navigation)
  - [Editing](#smartparens-editing)
+ [Clojure](#clojure)
+ [CIDER](#cider)
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

| Keybinding       | Spacemacs Keybinding | Description                            | Notes                                                                                                                  |
|------------------|----------------------|----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <kbd>C-p</kbd>   | <kbd>k</kbd>         | move cursor to previous line           |                                                                                                                        |
| <kbd>C-b</kbd>   | <kbd>h</kbd>         | move cursor backward  one character    |                                                                                                                        |
| <kbd>C-f</kbd>   | <kbd>l</kbd>         | move cursor forward one character      |                                                                                                                        |
| <kbd>C-n</kbd>   | <kbd>j</kbd>         | move cursor to next line               |                                                                                                                        |
| <kbd>C-S-p</kbd> | <kbd>5k</kbd>        | move cursor up 5 lines (e.g. faster)   | Custom keybinding courtesy of [magnars](https://github.com/magnars/.emacs.d/blob/master/settings/key-bindings.el#L216) |
| <kbd>C-S-n</kbd> | <kbd>C-e</kbd>       | move cursor down 5 lines (e.g. faster) | Custom keybinding courtesy of [magnars](https://github.com/magnars/.emacs.d/blob/master/settings/key-bindings.el#L216) |
| <kbd>M-b</kbd>   | <kbd>b</kbd>         | move cursor to previous word           |                                                                                                                        |
| <kbd>M-f</kbd>   | <kbd>w</kbd>         | move cursor to next word               |                                                                                                                        |
| <kbd>C-M-b</kbd> | <kbd>(</kbd>         | move cursor to previous  s-expression  |                                                                                                                        |
| <kbd>C-M-f</kbd> | <kbd>)</kbd>         | move cursor to next s-expression       |                                                                                                                        |
| <kbd>C-a</kbd>   | <kbd>0</kbd>         | Go to beginning of line                |                                                                                                                        |
| <kbd>C-e</kbd>   | <kbd>$</kbd>         | Go to end of line                      |                                                                                                                        |

#### Jumping Around

Keybindings for jumping around inside a single buffer.

| Keybinding       | Spacemace Keybinding | Description                            | Notes             |
|------------------|----------------------|----------------------------------------|-------------------|
| <kbd>s-[</kbd>   | <kbd>s-[</kbd>       | Previous cursor position within buffer | Custom keybinding |
| <kbd>s-]</kbd>   | <kbd>s-]</kbd>       | Next cursor position within buffer     | Custom keybinding |
| <kbd>M-<</kbd>   | <kbd>gg</kbd>        | Go to beginning of buffer              |                   |
| <kbd>M-></kbd>   | <kbd>G</kbd>         | Go to end of buffer                    |                   |
| <kbd>M-g g</kbd> | <kbd>:X</kbd>        | Go to line number X                    |                   |
| <kbd>C-l</kbd>   | <kbd>M</kbd>         | Center screen at cursor/point          |                   |
| <kbd>M-v</kbd>   | <kbd>C-u</kbd>       | Scroll to previous screen              |                   |
| <kbd>C-v</kbd>   | <kbd>C-d</kbd>       | Scroll to next screen                  |                   |

#### Jumping Around (Avy)

| Keybinding    | Spacemacs Keybinding | Description                                           |
|---------------|----------------------|-------------------------------------------------------|
| <kbd>jj</kbd> | <kbd>SPC SPC</kbd>   | Jump to the beginning of a word (`avy-goto-char`)     |
| <kbd>jk</kbd> |                      | Jump to character (`avy-goto-char-2`)                 |
| <kbd>jl</kbd> | <kbd>SPC y</kbd>     | Jump to the beginning of a line (`avy-goto-word-1`)   |
| <kbd>xx</kbd> | <kbd>SPC :</kbd>     | Executed extended command(`execute-extended-command`) |

### Across buffers

Keybindings for moving in between open buffers.

| Keybinding             | Spacemacs Keybinding | Description          |
|------------------------|----------------------|----------------------|
| <kbd>C-x <left></kbd>  | <kbd>SPC b p</kbd>   | Previous buffer/file |
| <kbd>C-x <right></kbd> | <kbd>SPC b n</kbd>   | Next buffer/file     |

## Selection/Copy/Paste

Commands for selecting, cutting, copying and pasting regions of text.

| Keybinding         | Spacemacs keybinding | Description                                      |
|--------------------|----------------------|--------------------------------------------------|
| <kbd>C-SPACE</kbd> | <kbd>SPC v</kbd>     | Mark the beginning of a selection                |
| <kbd>C-x C-x</kbd> | <kbd>o</kbd>         | Toggle between beginning and ending of selection |
| <kbd>M-w</kbd>     | <kbd>y</kbd>         | Copy selection                                   |
| <kbd>C-w</kbd>     | <kbd>d</kbd>         | Cut and copy selection                           |
| <kbd>C-y</kbd>     | <kbd>p</kbd>         | Paste (yank from kill ring)                      |
| <kbd>C-x h</kbd>   |                      | Select entire buffer region                      |

## Expand Region

| Keybinding     | Spacemacs keybinding | Description                           |
|----------------|----------------------|---------------------------------------|
| <kbd>C-=</kbd> | <kbd>SPC v</kbd>     | Initiate expand region                |
| <kbd>C-=</kbd> | <kbd>v</kbd>         | Expend region by semantic unit        |
| <kbd>C--<kbd>  | <kbd>V</kbd>         | Contract region by semantic unit      |
|                | <kbd>r</kbd>         | Reset the region to initial selection |
| <kbd>C-g</kbd> | <kbd>ESC</kbd>       | Leave expand-region mode              |

### Selection advanced

| Keybinding       | Spacemacs Keybinding | Description         | Notes |
|------------------|----------------------|---------------------|-------|
| <kbd>C-M-@</kbd> |                      | Select s-expression |       |
| <kbd>C-M-h</kbd> |                      | Select function     |       |

## Editing

Keybindings for making changes within a buffer.

| Keybinding             | Spacemacs Keybinding | Description                                              | Notes                                                                 |
|------------------------|----------------------|----------------------------------------------------------|-----------------------------------------------------------------------|
| <kbd>C-/</kbd>         | <kbd>u</kbd>         | Undo                                                     |                                                                       |
| <kbd>C-S-/</kbd>       | <kbd>C-r</kbd>       | Redo                                                     |                                                                       |
| <kbd>C-x u</kbd>       | <kbd>SPC a u</kbd>   | Undo tree visualize                                      |                                                                       |
| <kbd>C-Shift-Del</kbd> | <kbd>dd</kbd>        | Delete current line                                      |                                                                       |
| <kbd>C-k</kbd>         | <kbd>d$</kbd>        | Delete rest of line from cursor                          |                                                                       |
| <kbd>M-0 C-k</kbd>     | <kbd>d0</kbd>        | Delete from cursor to beginning of line                  |                                                                       |
| <kbd>M-Del</kbd>       | <kbd>db</kbd>        | Delete previous word                                     |                                                                       |
| <kbd>M-d</kbd>         | <kbd>de</kbd>        | Delete next word                                         |                                                                       |
|                        | <kbd>daw</kbd>       | Delete current word                                      |                                                                       |
| <kbd>C-c d</kbd>       | <kbd>yyp</kbd>       | Duplicate current line                                   |                                                                       |
| <kbd>C-x C-t</kbd>     | <kbd>SPC x t l</kbd> | Swap line with line above                                |                                                                       |
| <kbd>M-z</kbd>         | <kbd>df</kbd>        | delete up to char                                        | Keep hitting char to go to next occurrence. <kbd>C-K</kbd> to delete. |
| <kbd>M-\\</kbd>        |                      | delete all surrounding whitespace and tabs around cursor |                                                                       |

## Editing (Evil)

| Keybinding    | Description                   |
|---------------|-------------------------------|
| <kbd>r</kbd>  | Replace a single character    |
| <kbd>cc</kbd> | Change/replace entire line    |
| <kbd>cw</kbd> | Change/replace to end of word |
| <kbd>c$</kbd> | Change/replace to end of line |

## Visual (Evil)

| Keybinding    | Description             |
|---------------|-------------------------|
| <kbd>aw</kbd> | Select a word           |
| <kbd>ab</kbd> | Select a `()` block     |
| <kbd>aB</kbd> | Select a `{}` block     |
| <kbd>ib</kbd> | Select inner `()` block |
| <kbd>iB</kbd> | Select inner `{}` block |

### Transposing

| Keybinding       | Spacemacs Keybinding | Description             |
|------------------|----------------------|-------------------------|
| <kbd>M-t l</kbd> | <kbd>SPC x t l</kbd> | Transpose lines         |
| <kbd>M-t w</kbd> |                      | Transpose words         |
| <kbd>M-t s</kbd> |                      | Transpose s-expressions |
| <kbd>M-t p</kbd> |                      | Transpose params        |


## Searching/Replacing

| Keybinding       | Spacemacs Keybinding               | Description                                |
|------------------|------------------------------------|--------------------------------------------|
| <kbd>C-s</kbd>   | <kbd>SPC s b</kbd>                 | Find next occurrence in buffer             |
|                  | <kbd>SPC s p</kbd>                 | Search within project                      |
| <kbd>C-r</kbd>   |                                    | Find previous occurrence in buffer         |
| <kbd>C-M-s</kbd> |                                    | Find next occurrence using regex in buffer |
| <kbd>C-M-r</kbd> |                                    | Find previous occurrence in buffer         |


## File Management

| Keybinding                    | Spacemacs Keybinding         | Description                       | Notes             |
|-------------------------------|------------------------------|-----------------------------------|-------------------|
| <kbd>C-x b <name> RET</kbd>   | <kbd>SPC b b</kbd>           | Create a new/open recent buffer   |                   |
| <kbd>C-x 4 b <name> RET</kbd> |                              | Create a new buffer in new window |                   |
| <kbd>C-x C-f</kbd>            | <kbd>SPC f f</kbd>           | Open a file                       |                   |
| <kbd>C-x f</kbd>              | <kbd>SPC f r</kbd>           | Open recent file                  |                   |
| <kbd>C-x k RET</kbd>          | <kbd>SPC b d</kbd>           | Close buffer                      |                   |
| <kbd>C-x C-s</kbd>            | <kbd>SPC f s</kbd>           | Save buffer                       |                   |
| <kbd>C-x C-w <name> RET</kbd> | <kbd>SPC f s</kbd>           | Save buffer to file               |                   |
| <kbd>C-c D</kbd>              | <kbd>SPC f D</kbd>           | Delete current buffer & file      | custom keybinding |
| <kbd>M-x <mode-name></kbd>    | <kbd>SPC : <mode-name></kbd> | Enable mode in file               |                   |

## Directory Management

| Keybinding                            | Spacemacs Keybinding | Description                                       |
|---------------------------------------|----------------------|---------------------------------------------------|
| <kbd>C-x d</kbd>                      | <kbd>SPC a d</kbd>   | Open Dired                                        |
| <kbd><</kbd>                          |                      | Previous directory in listing (skips files)       |
| <kbd>></kbd>                          |                      | Next directory in listing (skips files)           |
| <kbd>f</kbd>                          |                      | Open file                                         |
| <kbd>v</kbd>                          |                      | View file                                         |
| <kbd>^</kbd>                          |                      | Go up to parent directory                         |
| <kbd>d</kbd>                          |                      | Mark file for deletion                            |
| <kbd>x</kbd>                          |                      | Delete files marked for deletion                  |
| <kbd>q</kbd>                          |                      | Quit                                              |
| <kbd>+</kbd>                          |                      | Create directory                                  |
| <kbd>=</kbd>                          |                      | Compare file at point with previously marked file |
| <kbd>m</kbd>                          |                      | Mark a file for action                            |
| <kbd>u</kbd>                          |                      | Unmark a file for action                          |
| <kbd>t</kbd>                          |                      | Toggle marking                                    |
| <kbd>! \<shell command string\></kbd> |                      | Run shell command on file at cursor               |

## Window Management

| Keybinding                  | Spacemacs Keybinding        | Description                                   |
|-----------------------------|-----------------------------|-----------------------------------------------|
| <kbd>C-x 1</kbd>            | <kbd>SPC w m</kbd>          | Close all other windows except current window |
| <kbd>C-x 2</kbd>            | <kbd>SPC w s</kbd>          | Split current window horizontally             |
| <kbd>C-x 3</kbd>            | <kbd>SPC w v</kbd>          | Split current window vertically               |
| <kbd>C-x 0</kbd>            | <kbd>SPC w c</kbd>          | Close current window                          |
| <kbd>C-x o</kbd>            | <kbd>SPC TAB</kbd>          | Switch to next window                         |
| <kbd>M-- C-x o</kbd>        |                             | Switch to previous window                     |
| <kbd>M-<number> C-x o</kbd> |                             | Jump ahead # of windows                       |
| <kbd>C-M-Shift-v</kbd>      |                             | Scroll backward other window                  |
| <kbd>C-M-v</kbd>            |                             | Scroll forward other window                   |
| <kbd>C-x {</kbd>            |                             | Shrink window narrower                        |
| <kbd>C-x }</kbd>            |                             | Grow window wider                             |
|                             | <kbd>SPC w =</kbd>          | Balance split windows                         |
|                             | <kbd>SPC <window_num></kbd> | Jump to window number                         |

### Windmove

| Keybinding             | Spacemacs Keybinding | Description                                   |
|------------------------|----------------------|-----------------------------------------------|
| <kbd>S-\<left\></kbd>  |                      | Move to window to the left of current window  |
| <kbd>S-\<right\></kbd> |                      | Move to window to the right of current window |
| <kbd>S-\<up\></kbd>    |                      | Move to window above current window           |
| <kbd>S-\<down\></kbd>  |                      | Move to window below current window           |

## Frame Management

| Keybinding         | Spacemacs Keybinding | Description                                 |
|--------------------|----------------------|---------------------------------------------|
| <kbd>C-x 5 1</kbd> |                      | Close all other frames except current frame |
| <kbd>C-x 5 2</kbd> |                      | Split current frame horizontally            |
| <kbd>C-x 5 0</kbd> |                      | Close current frame                         |
| <kbd>C-x 5 o</kbd> |                      | Switch to next frame                        |
| <kbd>C-x C-n</kbd> |                      | Create new frame                            |

## Projectile

Project navigation. An alternate prefix is Command-P.

| Keybinding                                         | Spacemacs Keybinding | Description                                 | Notes             |
|----------------------------------------------------|----------------------|---------------------------------------------|-------------------|
| <kbd>M-S-o</kbd> (default is <kbd>C-c p f</kbd>)   | <kbd>SPC p f</kbd>   | Open file in project with completion        | Custom keybinding |
| <kbd>M-S-f</kbd> (default is <kbd>C-c p s s</kbd>) | <kbd>SPC p s</kbd>   | Search all files in project using regex     | Custom keybinding |
| <kbd>M-e</kbd> (default is <kbd>C-c p e</kbd>)     | <kbd>SPC p r</kbd>   | Show all recent opened files in project     | Custom keybinding |
| <kbd>C-c p F</kbd>                                 |                      | Open file in ANY project with completion    |                   |
| <kbd>C-c p r</kbd>                                 |                      | Find/replace all files in project           |                   |
| <kbd>C-c p b</kbd>                                 |                      | Show all open project buffers               |                   |
| <kbd>C-c p p</kbd>                                 | <kbd>SPC p p</kbd>   | Switch between known projects               |                   |
| <kbd>C-c p D</kbd>                                 |                      | Open root project in dired                  |                   |
| <kbd>C-c p k</kbd>                                 |                      | Kill all buffers in project                 |                   |
| <kbd>C-c p !</kbd>                                 |                      | Run shell on root of project as current dir |                   |
| <kbd>C-c p p</kbd>                                 |                      | Show all known projects                     |                   |

## File Navigation (NeoTree)

| Keybinding         | Spacemacs Keybinding | Description                                        | Notes                    |
|--------------------|----------------------|----------------------------------------------------|--------------------------|
| <kbd>\<f8\></kbd>  | <kbd>SPC f t</kbd>   | Toggle project explorer                            |                          |
| <kbd>RET</kbd>     | <kbd>RET</kbd>       | Open file in main window                           | (when in neotree buffer) |
|                    | <kbd># RET</kbd>     | Open file in window #                              | (when in neotree buffer) |
| <kbd>&#124;</kbd>  | <kbd>&#124;</kbd>    | Open file in vertical split                        | (when in neotree buffer) |
| <kbd>-</kbd>       | <kbd>-</kbd>         | Open file in horizontal split                      | (when in neotree buffer) |
| <kbd>C-c C-n</kbd> |                      | Create a new file or dir if filename ends with '/' | (when in neotree buffer) |
| <kbd>C-c C-d</kbd> |                      | Delete a file or a directory                       | (when in neotree buffer) |
| <kbd>C-c C-r</kbd> |                      | Rename a file or a directory                       | (when in neotree buffer) |
| <kbd>g</kbd>       |                      | Refresh project explorer                           | (when in neotree buffer) |
| <kbd>U</kbd>       |                      | Go up one node in tree                             | (when in neotree buffer) |
| <kbd>D</kbd>       |                      | Go down one node in tree                           | (when in neotree buffer) |
| <kbd>A</kbd>       |                      | Toggle widening explorer window                    | (when in neotree buffer) |
| <kbd>S</kbd>       | <kbd>H</kbd>         | Go to previous sibling node in tree                | (when in neotree buffer) |
| <kbd>s</kbd>       | <kbd>L</kbd>         | Go to next sibling node in tree                    | (when in neotree buffer) |
| <kbd>H</kbd>       |                      | Toggle showing hidden files                        | (when in neotree buffer) |

## Multiple Cursors

See [https://github.com/magnars/multiple-cursors.el](https://github.com/magnars/multiple-cursors.el)

| Keybindings            | Description                                  | Notes              |
|------------------------|----------------------------------------------|--------------------|
| <kbd>C-S-c C-S-c</kbd> | Mark consecutive lines with multiple cursors | First select lines |
| <kbd>C-<</kbd>         | Mark previous occurrence of word             | First select word  |
| <kbd>C-></kbd>         | Mark next occurrence of word                 | First select word  |
| <kbd>C-c C-<</kbd>     | Mark all occurrences like selection          |                    |

## Commenting

| Spacemacs Keybinding | Description            |
|----------------------|------------------------|
| <kbd>SPC ;</kbd>     | Comment to end of line |
| <kbd>SPC c l</kbd>   | Comment lines          |
| <kbd>SPC c L</kbd>   | Invert Comment lines   |

## Coding

| Keybinding         | Spacemacs Keybinding | Description                                 | IntelliJ IDEA    |
|--------------------|----------------------|---------------------------------------------|------------------|
| <kbd>C-,</kbd>     |                      | Auto-complete at point                      | <kbd>M-SPC</kbd> |
| <kbd>C-x C-i</kbd> | <kbd>SPC s j</kbd>   | List definitions in file and jump           | <kbd>M-F12</kbd> |
| <kbd>C-c p c</kbd> | <kbd>SPC c C</kbd>   | Run compile on project                      |                  |
| <kbd>C-c p P</kbd> |                      | Run tests on project                        |                  |
| <kbd>C-c p t</kbd> | <kbd>SPC p a</kbd>   | Toggle between implementation and test file |                  |

## Smartparens

Using base keybindings for paredit. Smartparens annoyingly hijacks various emacs keybindings in a way I don't like (e.g. M-DEL for kill word backwards)

### Smartparens Navigation

| Keybinding       | Spacemacs Keybinding | Description                              | Notes                                                                                                  |
|------------------|----------------------|------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <kbd>C-M-b</kbd> |                      | Move backward one s-expression           | Must be on a paren, otherwise behaves like backward word                                               |
| <kbd>C-M-f</kbd> |                      | Move forward one s-expression            | Must be on a paren, otherwise behaves like forward word                                                |
| <kbd>C-M-d</kbd> |                      | Move down to next nested s-expression    |                                                                                                        |
| <kbd>C-M-n</kbd> |                      | Move up s-expression                     |                                                                                                        |
| <kbd>C-M-u</kbd> |                      | Move up one level in nested s-expression | Requires fix for OSX interception of the keybinding (see http://emacs.stackexchange.com/a/20544/11397) |


### Smartparens Editing

| Keybinding                    | Spacemacs Keybinding | Description                                                                     | Notes                    |
|-------------------------------|----------------------|---------------------------------------------------------------------------------|--------------------------|
| <kbd>(</kbd>                  |                      | Wrap currently selected region with parens                                      | Use with `expand-region` |
| <kbd>M-s</kbd>                |                      | Remove parens immediately surrounding cursor point                              |                          |
| <kbd>C-(</kbd>,<kbd>C-{</kbd> |                      | Pull in or out previous word/s-expression into current s-expression             |                          |
| <kbd>C-)</kbd>,<kbd>C-}</kbd> |                      | Pull in or out next word/s-expression into current s-expression                 |                          |
| <kbd>M-\<up\></kbd>           |                      | Remove all chars before cursor point inside s-expression and surrounding parens |                          |
| <kbd>M-\<down\></kbd>         |                      | Remove all chars after cursor point inside s-expression and surrounding parens  |                          |
| <kbd>M-r</kbd>                |                      | Remove all chars around cursor point inside s-expression and surrounding parens |                          |
| <kbd>M-S</kbd>                |                      | Split current s-expression into two separate ones with cursor as split point    |                          |
| <kbd>C-M-t</kbd>              |                      | When cursor is placed between s-expressions, swaps (transposes) their positions |                          |


## Clojure

| Keybinding                        | Spacemacs Keybinding | Description                | Notes                                                                 |
|-----------------------------------|----------------------|----------------------------|-----------------------------------------------------------------------|
| <kbd>C-c RET</kbd>                |                      | clj refactor prefix        | See [commands](https://github.com/clojure-emacs/clj-refactor.el/wiki) |
| <kbd>M-x clojure-cheatsheet</kbd> |                      | Clojure command cheatsheet |                                                                       |

## CIDER

| Keybinding           | Spacemacs Keybinding | Description                                                                    | Notes |
|----------------------|----------------------|--------------------------------------------------------------------------------|-------|
| <kbd>C-c M-j</kbd>   |                      | Cider jack-in, opens nREPL in a clojure project                                |       |
| <kbd>C-c C-k</kbd>   |                      | Load (eval) the current buffer                                                 |       |
| <kbd>C-c C-e</kbd>   |                      | Eval form before current cursor position                                       |       |
| <kbd>C-c C-v v</kbd> |                      | Eval form around current cursor position                                       |       |
| <kbd>C-c C-v r</kbd> |                      | Eval the region and display result in echo area                                |       |
| <kbd>C-c C-v n</kbd> |                      | Eval the entire current namespace                                              |       |
| <kbd>C-c C-z</kbd>   |                      | Switch the REPL buffer                                                         |       |
| <kbd>C-c M-z</kbd>   |                      | Load (eval) the current buffer and switch to the REPL buffer                   |       |
| <kbd>C-c M-n</kbd>   |                      | Switch the namespace of the REPL buffer to the namespace of the current buffer |       |
| <kbd>C-c C-x</kbd>   |                      | Reload all modified files on the classpath                                     |       |
| <kbd>C-c C-t n</kbd> |                      | Run tests in current ns                                                        |       |
| <kbd>C-c C-t t</kbd> |                      | Run a test at the cursor position                                              |       |
| <kbd>C-u C-M-x</kbd> |                      | Start debug session                                                            |       |
| <kbd>C-c C-d d</kbd> |                      | Display doc string for the symbol at point                                     |       |
| <kbd>C-c C-.</kbd>   |                      | Jump to some namespace on the classpath                                        |       |
| <kbd>,</kbd>         |                      | Once repl is open, get command keybindings                                     |       |
| <kbd>C-c C-q</kbd>   |                      | Quit current REPL session                                                      |       |

## Version Control (Magit)

| Keybinding                                 | Spacemacs Keybinding                       | Description                          |
|--------------------------------------------|--------------------------------------------|--------------------------------------|
| <kbd>C-x m</kbd>                           | <kbd>SPC g s</kbd>                         | See current git status/changed files |
| <kbd>g</kbd>                               |                                            | Reload status buffer                 |
| <kbd>c c, \<write message\>, C-c C-c</kbd> | <kbd>c c, \<write message\>, C-c C-c</kbd> | Commit file                          |
| <kbd>P u</kbd>                             | <kbd>P u</kbd>                             | Push changes to remote               |
| <kbd>F u</kbd>                             | <kbd>F u</kbd>                             | Pull latest changes                  |
| <kbd>s</kbd>                               |                                            | Stage file                           |
| <kbd>u</kbd>                               |                                            | Unstage file                         |
| <kbd>b b</kbd>                             |                                            | Switch branch                        |
| navigate to file, then <kbd>TAB</kbd>      |                                            | Version diff                         |
| <kbd>k</kbd>                               |                                            | revert changes                       |
| <kbd>l l</kbd>                             |                                            | Show log                             |
| <kbd>b</kbd>                               |                                            | Switch to branch                     |
| <kbd>B</kbd>                               |                                            | Create a new branch                  |
| <kbd>z</kbd>                               |                                            | Stash changes                        |
| <kbd>A</kbd>                               |                                            | Unstash changes                      |
| <kbd>I</kbd>                               |                                            | Exclude file(s)                      |
| <kbd>M-x magit-clone</kbd>                 |                                            | Clone a repo                         |
| <kbd>q</kbd>                               | <kbd>q</kbd>                               | Quit                                 |

## Eshell

| Keybinding         | Spacemacs Keybinding | Description                                   |
|--------------------|----------------------|-----------------------------------------------|
| <kbd>C-z</kbd>     |                      | Open eshell                                   |
| <kbd>M-p</kbd>     |                      | Go back in command history                    |
| <kbd>M-n</kbd>     |                      | Go forward in command history                 |
| <kbd>C-c C-r</kbd> |                      | Clear the shell buffer                        |
| <kbd>M-r</kbd>     |                      | search backwars in command history with regex |
| <kbd>M-s</kbd>     |                      | search forward in command history with regex  |
| <kbd>!!</kbd>      |                      | Repeats the last command                      |
| <kbd>!ls</kbd>     |                      | Repeats the last commnd starting with ls      |

## Org mode

### TODO Lists

| Keybinding                                | Spacemacs Keybinding | Description                                     |
|-------------------------------------------|----------------------|-------------------------------------------------|
| <kbd>C-c C-p</kbd>                        |                      | Move up a heading                               |
| <kbd>C-c C-n</kbd>                        |                      | Move down a heading                             |
| <kbd>C-c C-b</kbd>                        |                      | Move up a heading, same level                   |
| <kbd>C-c C-f</kbd>                        |                      | Move down a heading, same level                 |
| <kbd>TAB</kbd>                            |                      | Toggle heading open/closed states               |
| <kbd>S-TAB</kbd>                          |                      | Toggle entire buffer heading open/closed states |
| <kbd>M-\<down\></kbd>                     |                      | Move heading down                               |
| <kbd>M-\<up\></kbd>                       |                      | Move heading up                                 |
| <kbd>M-\<left\></kbd>                     |                      | Promote heading                                 |
| <kbd>M-\<right\></kbd>                    |                      | Demote heading                                  |
| <kbd>C-RET</kbd>                          |                      | New heading                                     |
| <kbd>M-RET</kbd>                          |                      | New list item entry                             |
| <kbd>/</kbd>                              |                      | Search inside org mode                          |
| <kbd>C-c -</kbd>                          |                      | Cycle item type                                 |
| <kbd>S-<left></kbd>, <kbd>S-<right></kbd> |                      | Cycle state of `TODO` item                      |

### Table Editing

| Keybinding               | Spacemacs Keybinding   | Description                                       |
|--------------------------|------------------------|---------------------------------------------------|
| <kbd>C-c &#124;</kbd>    |                        | Convert active region into a table                |
| <kbd>C-c C-c             |                        | Re-align table                                    |
| <kbd>TAB</kbd>           | <kbd>SPC m t l</kbd>   | Re-align the table and move to the next field     |
| <kbd>S-TAB</kbd>         | <kbd>SPC m t h</kbd>   | Re-align the table and move to the previous field |
| <kbd>&#124; RET</kbd>    | <kbd>SPC m t i c</kbd> | Insert new column to the right                    |
| <kbd>RET</kbd>           | <kbd>RET</kbd>         | Re-align the table and move to the next row       |
| <kbd>C-c SPC</kbd>       | <kbd>SPC m t b</kbd>   | Blank the table cell at cursor                    |
| <kbd>C-c -</kbd>         | <kbd>SPC m t i h</kbd> | Insert a horizontal rule on next line             |
| <kbd>M-\<left\></kbd>    | <kbd>SPC m t H</kbd>   | Move column at cursor to the left                 |
| <kbd>M-\<right\></kbd>   | <kbd>SPC m t L</kbd>   | Move column at cursor to the right                |
| <kbd>M-S-\<left\></kbd>  | <kbd>SPC m t d c</kbd> | kill current column                               |
| <kbd>M-S-\<right\></kbd> | <kbd>SPC m t i c</kbd> | Insert a new column to the left of the cursor     |
| <kbd>M-S-\<up\></kbd>    | <kbd>SPC m t d r</kbd> | Kill the current table row                        |
| <kbd>M-S-\<down\></kbd>  | <kbd>SPC m t i r</kbd> | Insert new row above current row                  |

## Help

| Keybinding                                | Spacemacs Keybinding                      | Description                                                   | Notes             |
|-------------------------------------------|-------------------------------------------|---------------------------------------------------------------|-------------------|
| <kbd>M-x describe-key</kbd>               | <kbd>SPC h d k</kbd>                      | Tell which function is bound to key combo                     |                   |
| <kbd>C-h b</kbd>                          | <kbd>SPC ?</kbd>                          | All active keybindings with flx-ido narrowing                 | Custom keybinding |
| <kbd>C-h a \<topics\> RET</kbd>           |                                           | Search help system for matches to <topics>                    |                   |
| <kbd>type key prefix</kbd> and wait 1 sec | <kbd>type key prefix</kbd> and wait 1 sec | Get remaining completion options                              | via `which-key`   |
| <kbd>C-h m</kbd>                          |                                           | Display documentation of the current major mode               |                   |
| <kbd>C-h f</kbd>                          |                                           | Run `help-apropos`, an interactive version of apropos-command |                   |

## Workgroups

| Keybinding           | Spacemacs Keybinding | Description                          | Notes |
|----------------------|----------------------|--------------------------------------|-------|
| <kbd>C-c z C-s</kbd> | <kbd></kbd>          | Save current session for workgroup   |       |
| <kbd>C-c z C-f</kbd> |                      | Load a session for a given workgroup |       |
| <kbd>C-c z c</kbd>   |                      | Create a new workgroup               |       |
| <kbd>C-c z v</kbd>   |                      | Switch to a workgroup                |       |

## Markdown

Reference: http://ddloeffler.blogspot.ca/2013/04/keybindings-for-emacs-markdown-mode.html

| Keybinding           | Spacemacs Keybinding | Description                | Notes |
|----------------------|----------------------|----------------------------|-------|
| <kbd>C-c C-t h</kbd> | <kbd></kbd>          | Create heading             |       |
| <kbd>C-c C-a l</kbd> |                      | Create link                |       |
| <kbd>C-c C-a L</kbd> |                      | Create anchor link         |       |
| <kbd>C-c C-s e</kbd> |                      | Italisize selection/region |       |
| <kbd>C-c C-s s</kbd> |                      | Bold selection/region      |       |
| <kbd>C-c -</kbd>     |                      | Horizontal rule            |       |

## Minibuffer

Keybindings for use inside the minibuffer.

| Keybinding                               | Spacemacs Keybinding | Description                                   | Notes |
|------------------------------------------|----------------------|-----------------------------------------------|-------|
| <kbd>TAB</kbd>                           | <kbd></kbd>          | Auto-complete as much as possible             |       |
| <kbd>SPACE</kbd>                         |                      | Complete up to one word                       |       |
| <kbd>RET</kbd>                           |                      | Complete and execute                          |       |
| <kbd>?</kbd>                             |                      | Show completion possibilities                 |       |
| <kbd>M-r</kbd>                           |                      | Regex search backward through command history |       |
| <kbd>M-s</kbd>                           |                      | Regex search forward through command history  |       |
| <kbd>C-g</kbd> or <kbd>Esc Esc Esc</kbd> | <kbd>fd</kbd>        | Abort current command                         |       |

## Miscellaneous

| Keybinding                                  | Spacemacs Keybinding | Description                      | Notes                                        |
|---------------------------------------------|----------------------|----------------------------------|----------------------------------------------|
| <kbd>M-x ediff</kbd>                        | <kbd></kbd>          | Diff Files                       |                                              |
| <kbd>C-x v =</kbd>                          | <kbd></kbd>          | View diff of current file        |                                              |
| <kbd>M-x procd</kbd>                        | <kbd></kbd>          | View processes (like top)        | OR <kbd>C-x</kbd> p (with global keybinding) |
| <kbd>C-x d</kbd>                            | <kbd></kbd>          | File browser (dired)             |                                              |
| <kbd>C-x g</kbd>                            | <kbd></kbd>          | Search in Web hooks              | custom binding                               |
| <kbd>C-c u</kbd>                            | <kbd></kbd>          | View URL                         |                                              |
| <kbd>C-x C-f /remotehost:filename RET</kbd> | <kbd></kbd>          | TRAMP remote file editing        | Open a directory to get a Dired buffer!      |
| <kbd>M-$</kbd>                              | <kbd></kbd>          | Check and fix spelling at cursor |                                              |

## Credits

- [Magnar Sveen](https://github.com/magnars/.emacs.d)
- [Bozhidar Batsov's favourite keybindings](http://stackoverflow.com/a/3125243/3166303)
- [Awesome Emacs](https://github.com/emacs-tw/awesome-emacs)
