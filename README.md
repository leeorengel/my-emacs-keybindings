# Emacs Keybindings with IntelliJ IDEA Analogs
Handy key maps to help users learning emacs coming from intelliJ IDEA

**Table of Contents**

- [Minibuffer](#minibuffer)
- [Navigation](#navigation)
  - [Within buffer](#within-buffer)
  - [Across buffers](#across-buffers)
- [Editing](#editing)
- [File Management](#file-management)
- [Directory Management](#directory-management)
-

## Minibuffer

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

Keybinding                                | Description                              | Notes
------------------------------------------|------------------------------------------|--------------------------
<kbd>C-u C-SPACE</kbd>                    | Previous cursor position within buffer   |
<kbd>C-u C-@</kbd>                        | Next cursor position within buffer       |
<kbd>M-<</kbd>                            | Go to beginning of buffer                |
<kbd>M-></kbd>                            | Go to end of buffer                      |
<kbd>M-g g</kbd>                          | Go to line number                        |
<kbd>C-l</kbd>                            | Center screen at cursor/point            |
<kbd>M-v</kbd>                            | Scroll to previous screen                |
<kbd>C-v</kbd>                            | Scroll to next screen                    |



### Across buffers

Keybinding                                | Description                     | Notes
------------------------------------------|---------------------------------|-------------------------------------
<kbd>C-x [left arrow]</kbd>               | Previous buffer/file            |
<kbd>C-x [right arrow]</kbd>              | Next buffer/file                |
<kbd>C-TAB</kbd>                          | Cycle buffers                   | via global keybinding `(global-set-key (kbd "<C-tab>") 'bury-buffer)`


## Editing



## Version Control
