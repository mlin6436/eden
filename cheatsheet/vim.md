# Vim Cheat Sheet

| Navigating File | Explanation |
| --------------- | ----------- |
| h | move left a column |
| j | move down a row |
| k | move up a row |
| l | move right a column |
| w | forward one word |
| b | back to start of word |
| 0 | start of line |
| $ | end of line |
| nG | go to line n	|
| G | go to last line |

| Inserting Text (§) ESC to finish | Explanation |
| -------------------------------- | ----------- |
| i | insert before cursor (§) |
| o | open new line below (§) |
| O | open new line above (§) |
| A | append at the end of line (§) |
| C | change to end of line (§) |
| D | delete to end of line |

| Editing | 1 char | 1 word | n words | 1 line | n lines |
 -------- | :----: | :----: | :-----: | :----: | ------: |
| delete | x | dw | ndw | dd | ndd |
| change | r | cw(§) | ncw(§) | cc(§) | ncc(§) |
| copy (yank) into buffer | yw | nyw | yy | nyy |
| p       | paste buffer after/below cursor              |
| P       | paste buffer before/above cursor             |
| delete -> move cursor -> paste = cut & paste           |
| copy -> move cursor -> paste = duplicate               |

| Searching for Text | Explanation |
| ------------------ | ----------- |
| / | pattern search for pattern |
| n | repeat last search |
| :n,ms/old/new/ | between lines n and m substitute old with new |

| Miscellaneous | Explanation |
| ------------- | ----------- |
| . | repeat last edit command |
| >> | indent line |
| u | undo last edit command |
| U | undo all changes to current line |
| J | join lines |
| ^L | redraw screen |


| Writing the file/Quitting vi | Explanation |
| ------------- | ----------- |
| :r | file read contents of file and place after current line |
| :n,mw | file write portion of file between lines n and m to file |
| :w | save |
| :w | file save to file |
| :w! | force save (often as root) |
| :q | quit |
| :wq | save & quit |
| :q! | force quit (no save) |

| Escaping into shell | Explanation |
| ------------------- | ----------- |
| :!ksh | run interative shell; press ^D to return to vi |
| :!cmd | run cmd; press <CR> to return to vi |
| !!cmd | run cmd; put its output into file being edited |
