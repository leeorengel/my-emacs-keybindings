# Emacs Keybindings with IntelliJ IDEA Analogs

Handy keybindings to help users learning emacs coming from intelliJ IDEA or the Jetbrains family of IDE's.

**Table of Contents**

- [Minibuffer](#minibuffer)
- [Navigation](#navigation)
  - [Within buffer](#within-buffer)
    - [Basic Motion](#basic-motion)
    - [Jumping Around](#jumping-around)
  - [Across buffers](#across-buffers)
- [Selection/Copy/Paste](#selection/copy/paste)
- [Editing](#editing)
- [File Management](#file-management)
- [Directory Management](#directory-management)
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

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |
<kbd></kbd>               |        |



## File Management

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------


## Directory Management

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------

## Version Control
Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------



## Credits

- [Bozhidar Batsov's favourite keybindings](http://stackoverflow.com/a/3125243/3166303)
