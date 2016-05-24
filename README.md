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

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Frame Management

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Projectile

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Coding

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Clojure/CIDER

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Version Control
Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Miscellaneous

## Credits

- [Bozhidar Batsov's favourite keybindings](http://stackoverflow.com/a/3125243/3166303)
