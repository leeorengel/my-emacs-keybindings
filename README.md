# Emacs Keybindings with IntelliJ IDEA Analogs

Essential keybindings to help users learning emacs coming from intelliJ IDEA or the Jetbrains family of IDE's.

This page assumes you are using the prelude distribution of emacs.

This page has been organized roughly in order of importance in terms of the minimum keybindings you need to know to get going in emacs. Subsequent sections include more advanced groupings of keybindings.

**Table of Contents**

- [Navigation](#navigation)
  - [Within buffer](#within-buffer)
    - [Basic Motion](#basic-motion)
    - [Jumping Around](#jumping-around)
  - [Across buffers](#across-buffers)
- [Selection/Copy/Paste](#selectioncopypaste)
  - [Advanced](#selectionadvanced)
- [Editing](#editing)
- [Searching/Replacing](#searchingreplacing)
- [File Management](#file-management)
- [Directory Management](#directory-management)
- [Window Management](#window-management)
- [Frame Management](#frame-management)
- [Projectile](#projectile)
- [Coding](#coding)
- [Clojure/CIDER](#clojurecider)
- [Minibuffer](#minibuffer)
- [Markdown](#markdown)
- [Miscellaneous](#miscellaneous)
- [Credits](#credits)

## Minibuffer

Keybindings for use inside the minibuffer.

Keybinding                                | Description                                           | Notes
------------------------------------------|-------------------------------------------------------|------------------------------------
<kbd>TAB</kbd>                            | Auto-complete as much as possible                     |
<kbd>SPACE</kbd>                          | Complete up to one word                               |
<kbd>RET</kbd>                            | Complete and execute                                  |
<kbd>?</kbd>                              | Show completion possibilities                         |
<kbd>M-r</kbd>                            | Regex search backward through command history         |
<kbd>M-s</kbd>                            | Regex search forward through command history          |
<kbd>C-g</kbd> or <kbd>Esc Esc Esc</kbd>  | Abort current command                                 |

## Navigation

### Within a buffer

#### Basic Motion

Keybindings for very basic cursor movement.

Keybinding                                | Description                              | IntelliJ IDEA          | Notes
------------------------------------------|------------------------------------------|------------------------|------------------------
<kbd>C-p</kbd>                            | move cursor to previous line             | <kbd>C-p</kbd>         |
<kbd>C-n</kbd>                            | move cursor to next line                 | <kbd>C-n</kbd>         |
<kbd>M-b</kbd>                            | move cursor to previous word             |                        |
<kbd>M-f</kbd>                            | move cursor to next word                 |                        |
<kbd>C-M-b</kbd>                          | move cursor to next s-expression         |                        |
<kbd>C-M-f</kbd>                          | move cursor to next s-expression         |                        |
<kbd>C-a</kbd>                            | Go to beginning of line                  | <kbd>C-a</kbd>         |
<kbd>C-e</kbd>                            | Go to end of line                        | <kbd>C-e</kbd>         |

#### Jumping Around

Keybindings for jumping around inside a single buffer.

Keybinding                                | Description                              | IntelliJ IDEA          | Notes
------------------------------------------|------------------------------------------|------------------------|------------------------
<kbd>C-u C-SPACE</kbd>                    | Previous cursor position within buffer   | <kbd>Command-[</kbd>   | In IntelliJ, this is a general `back` cursor location including across files
<kbd>C-u C-@</kbd>                        | Next cursor position within buffer       | <kbd>Command-]</kbd>   | In IntelliJ, this is a general `forward` cursor location including across files
<kbd>M-<</kbd>                            | Go to beginning of buffer                | <kbd>Command-[</kbd>   | In IntelliJ, this is a general `back` cursor location including across files
<kbd>M-></kbd>                            | Go to end of buffer                      | <kbd>Command-]</kbd>   | In IntelliJ, this is a general `forward` cursor location including across files
<kbd>M-g g</kbd>                          | Go to line number                        | <kbd>Command-l</kbd>   |
<kbd>C-l</kbd>                            | Center screen at cursor/point            |
<kbd>M-v</kbd>                            | Scroll to previous screen                |
<kbd>C-v</kbd>                            | Scroll to next screen                    |

### Across buffers

Keybindings for moving in between open buffers.

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------
<kbd>C-x [left arrow]</kbd>               | Previous buffer/file            |
<kbd>C-x [right arrow]</kbd>              | Next buffer/file                |
<kbd>C-TAB</kbd>                          | Cycle buffers                   | via global keybinding `(global-set-key (kbd "<C-tab>") 'bury-buffer)`

## Selection/Copy/Paste

Commands for selecting, cutting, copying and pasting regions of text.

Keybinding                                | Description                                         | Notes
------------------------------------------|-----------------------------------------------------|-------------------------------------
<kbd>C-SPACE</kbd>                        | Mark the beginning of a selection                   |
<kbd>C-x C-x</kbd>                        | Toggle between beginning and ending of selection    |
<kbd>M-w</kbd>                            | Copy selection                                      |
<kbd>C-w</kbd>                            | Cut and copy selection                              |

### Selection Advanced

Keybinding                                | Description                                         | Notes
------------------------------------------|-----------------------------------------------------|-------------------------------------


## Editing

Keybindings for making changes within a buffer.

Keybinding                                | Description                             | IntelliJ IDEA        | Notes
------------------------------------------|-----------------------------------------|----------------------|--------------
<kbd>C-/</kbd>                            | Undo                                    | <kbd>Command-Z</kbd> |
<kbd>C-Shift-Del</kbd>                    | Delete current line                     |                      |
<kbd>C-k</kbd>                            | Delete rest of line from cursor         |
<kbd>M-0 C-k</kbd>                        | Delete from cursor to beginning of line |
<kbd>M-Del</kbd>                          | Delete previous word                    |
<kbd>M-d</kbd>                            | Delete next word                        |
<kbd>C-c d</kbd>                          | Duplicate current line                  |
<kbd>C-x C-t</kbd>                        | Swap line with line above               |

## Searching/Replacing

Keybinding                                | Description                                 | IntelliJ IDEA                                  | Notes
------------------------------------------|---------------------------------------------|------------------------------------------------|---------------
<kbd>C-s</kbd>                            | Find next occurrence in buffer              | <kbd>Command F</kbd>                           |
<kbd>C-r</kbd>                            | Find previous occurrence in buffer          | <kbd>Command Shift F</kbd>                     |
<kbd>C-M-s</kbd>                          | Find next occurrence using regex in buffer  | <kbd>Command F</kbd> with regex checkbox       |
<kbd>C-M-r</kbd>                          | Find previous occurrence in buffer          | <kbd>Command Shift F</kbd> with regex checkbox |


## File Management

Keybinding                                | Description                         | Notes
------------------------------------------|-------------------------------------|-------------------------------------
<kbd>C-x b <name> RET</kbd>               | Create a new/open recent buffer     |
<kbd>C-x 4 b <name> RET</kbd>             | Create a new buffer in new window   |
<kbd>C-x C-f</kbd>                        | Open a file                         |
<kbd>C-x k RET</kbd>                      | Close buffer                        |
<kbd>C-x C-s</kbd>                        | Save buffer                         |
<kbd>C-x C-w <name> RET</kbd>             | Save buffer to file                 |
<kbd>C-c D</kbd>                          | Delete current buffer & file        | `predule` keybinding
<kbd>C-c r</kbd>                          | Rename current buffer & file        | `predule` keybinding
<kbd>M-x <mode-name></kbd>                | Enable mode in file                 |


## Directory Management

Keybinding                                | Description                                       | Notes
------------------------------------------|---------------------------------------------------|-------------------------------------
<kbd>C-x d</kbd>                          | Open Dired                                        |
<kbd><</kbd>                              | Previous directory in listing (skips files)       |
<kbd>></kbd>                              | Next directory in listing (skips files)           |
<kbd>f</kbd>                              | Open file                                         |
<kbd>v</kbd>                              | View file                                         |
<kbd>^</kbd>                              | Go up to parent directory                         |
<kbd>d</kbd>                              | Mark file for deletion                            |
<kbd>q</kbd>                              | Quit                                              |
<kbd>+</kbd>                              | Create directory                                  |
<kbd>=</kbd>                              | Compare file at point with previously marked file |
<kbd>m</kbd>                              | Mark a file for action                            |
<kbd>u</kbd>                              | Unmark a file for action                          |
<kbd>t</kbd>                              | Toggle marking                                    |


## Window Management

Keybinding                    | Description                                    | Notes
------------------------------|------------------------------------------------|-----------------------------
<kbd>C-x 1</kbd>              | Close all other windows except current window  |                            |
<kbd>C-x 2</kbd>              | Split current window horizontally              |                            |
<kbd>C-x 3</kbd>              | Split current window vertically                |                            |
<kbd>C-x 0</kbd>              | Close current window                           |                            |
<kbd>C-x o</kbd>              | Switch to next window                          |                            |
<kbd>M-- C-x o</kbd>          | Switch to previous window                      |                            |
<kbd>M-<number> C-x o</kbd>   | Jump ahead # of windows                        |                            |
<kbd>C-x +</kbd>              | Balance windows                                |                            |
<kbd>C-M-Shift-v</kbd>        | Scroll backward other window                   |                            |
<kbd>C-M-v</kbd>              | Scroll forward other window                    |                            |

## Frame Management

Keybinding             | Description                                  | Notes
-----------------------|----------------------------------------------|-----------------------|
<kbd>C-x 5 1</kbd>     | Close all other frames except current frame  |                       |
<kbd>C-x 5 2</kbd>     | Split current frame horizontally             |                       |
<kbd>C-x 5 0</kbd>     | Close current frame                          |                       |
<kbd>C-x 5 o</kbd>     | Switch to next frame                         |                       |

## Projectile

Project navigation. An alternate prefix is Command-P.

Keybinding              | Description                                    | Notes
------------------------|------------------------------------------------|-----------------------
<kbd>C-c p f</kbd>      | Open file in project with completion           |                      |
<kbd>C-c p F</kbd>      | Open file in ANY project with completion       |                      |
<kbd>C-c p s g</kbd>    | Search all files in project using regex        |                      |
<kbd>C-c p r</kbd>      | Find/replace all files in project              |                      |
<kbd>C-c p b</kbd>      | Show all open project buffers                  |                      |
<kbd>C-c p D</kbd>      | Open root project in dired                     |                      |
<kbd>C-c p k</kbd>      | Kill all buffers in project                    |                      |
<kbd>C-c p e</kbd>      | Show all recent opened files in project        |                      |
<kbd>C-c p !</kbd>      | Run shell on root of project as current dir    |                      |
<kbd>C-c p p</kbd>      | Show all known projects                        |                      |

## Coding

Keybinding                                | Description                                 | IntelliJ IDEA        |  Notes
------------------------------------------|---------------------------------------------|----------------------|-------------------------
<kbd>Command ;</kbd>                      | Toggle comment lines                        | <kbd>Command /</kbd> | (via global keybinding to custom function)
<kbd>C-c p c</kbd>                        | Run compile on project                      |                      |
<kbd>C-c p P</kbd>                        | Run tests on project                        |                      |
<kbd>C-c p t</kbd>                        | Toggle between implementation and test file |                      |

## Clojure/CIDER

Keybinding                                | Description                                | Notes
------------------------------------------|--------------------------------------------|-------------------------------------
<kbd>C-c M-j</kbd>                        | Open nREPL in a clojure project            |
<kbd>,</kbd>                              | Once repl is open, get command keybindings |
<kbd>C-c C-t n</kbd>                      | Run tests in current ns                    |
<kbd>C-c C-t t</kbd>                      | Run a test at the cursor position          |
<kbd>C-u C-M-x</kbd>                      | Start debug session                        |
<kbd>M-x clojure-cheatsheet</kbd>         | Clojure command cheatsheet                 |

## Version Control

Keybinding                                  | Description                            | IntelliJ IDEA            |  Notes
--------------------------------------------|----------------------------------------|--------------------------|--------------
<kbd>C-x v d</kbd>                          | See current git status/changed files   | Open/switch to VCS tab   |
<kbd>C-x v v, write message, C-c C-c</kbd>  | Commit file                            |                          |
<kbd>C-x v i</kbd>                          | Add/stage file                         |                          |
<kbd>C-x v g</kbd>                          | Annotate/blame on current buffer       |                          |
<kbd>C-x v +</kbd>                          | Pull latest changes                    |                          |
<kbd>C-x v =</kbd>                          | Version diff                           | <kbd>Command D</kbd>     |
<kbd>C-x v u</kbd>                          | Revert changes                         |                          |
<kbd>C-x v l</kbd>                          | Show log                               |                          |

## Magit

Keybinding                                | Description                            | Notes
------------------------------------------|----------------------------------------|--------------------
<kbd>C-x g</kbd>                          | See current git status/changed files   |
<kbd>g</kbd>                              | Reload status buffer                   |
<kbd>c c, <write message>, C-c C-c</kbd>  | Commit file                            |
<kbd>P u</kbd>                            | Push changes to remote                 |
<kbd>F u</kbd>                            | Pull latest changes                    |
<kbd>s</kbd>                              | Stage file                             |
<kbd>u</kbd>                              | Unstage file                           |
<kbd>b b</kbd>                            | Switch branch                          |
navigate to file, then <kbd>TAB</kbd>     | Version diff                           |
<kbd>k</kbd>                              | revert changes                         |
<kbd>l l</kbd>                            | Show log                               |
<kbd>q</kbd>                              | quit magix                             |


## Help

Keybinding                                   | Description                                     | Notes
---------------------------------------------|-------------------------------------------------|----------------------------
<kbd><M-x describe-key</kbd>                 | Tell which function is bound to key combo       |
<kbd>C-h a <topics> RET</kbd>                | Search help system for matches to <topics>      |
<kbd>C-h b</kbd>                             | Display all key bindings in active modes        |
<kbd>type key prefix</kbd> and wait 1 second | Get remaining completion options                | via `which-key`
<kbd>C-h m</kbd>                             | Display documentation of the current major mode |


## Miscellaneous

Keybinding                                   | Description                             | IntelliJ IDEA              | Notes
---------------------------------------------|-----------------------------------------|----------------------------|--------------------------------------
<kbd>M-x ediff</kbd>                         | Diff Files                              | <kbd>Command D</kbd>       |
<kbd>C-x v =</kbd>                           | View diff of current file               |                            |
<kbd>M-x procd</kbd>                         | View processes (like top)               |                            | OR <kbd>C-x</kbd> p (with global keybinding)
<kbd>C-x M</kbd>                             | Open a shell/terminal (eshell in emacs) |                            |
<kbd>C-x d</kbd>                             | File browser (dired)                    |                            |
<kbd>C-c g</kbd>                             | Search in Google                        |                            | (via `prelude` with global keybinding)
<kbd>C-c u</kbd>                             | View URL                                |                            |
<kbd>C-c t</kbd>                             | Open terminal buffer                    | via Terminal tab           | (via `prelude` with global keybinding)
<kbd>C-x C-f /remotehost:filename RET</kbd>  | TRAMP remote file editing               |                            | Open a directory to get a Dired buffer!
<kbd>M-$</kbd>                               | Check and fix spelling at cursor        |                            |


## Credits

- [Bozhidar Batsov's favourite keybindings](http://stackoverflow.com/a/3125243/3166303)
