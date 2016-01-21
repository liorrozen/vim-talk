# Modes - displayed in bottom left under statusline

- NORMAL
- INSERT - Text input as you would expect
- VISUAL - Selecting a range of text
  - `v`
  - Line mode `<Shift-v>`
  - Block mode `<Ctrl-v>`
- Command `:<cmd>` - Execute commands
  This is essentially `ex` mode.
  - `:q` Quit
  - `:w` Write file / Save

`<ESC>` to return to NORMAL

---

# Navigation

NORMAL Mode

- Directional `HJKL` (or arrows - if you have them) - http://i.imgur.com/FFv1LqB.jpg
- `^` - First non-whitespace character on current line
- `$` - Last character on line (includes the newline character)
  - `g_` - Last non-whitespace character
- `w` Forward one word
- `b` Backward one word
- `e` Goto end of word
- `%` Jump to matching brackets
- `gg` Goto begining of file
- `G` Goto end of file
- `<Ctrl-e>` and `<Ctrl-y>` to scroll line-by-line in the file. 

NORMAL into INSERT

- `i` Switch to INSERT (before current character)
- `a` Switch to INSERT (after current character)
- `A` Goto end of line and switch to INSERT
- `I` Goto start of line and switch to INSERT
- `o` Switch to INSERT on a new line below
- `O` Switch to INSERT on a new line above

Command Mode

- Use `:<line-number>` to jump to a specific line number
  - `:` puts you in command mode. Command consisting of numbers
    will place your cursor on first non-whitespace character on that line.

VISUAL Mode

When in VISUAL mode, you can navigate to end of selection
using search tools. Press ENTER to "execute" the search and 
switch back from searching to VISUAL.

- `%` Jump to matching brackets. In VISUAL BLOCK, this will select
  the entire function/hash


---

# Search - fastest way to travel!

- Forward `/`
- Backwards `?`

Next occurance with `n` 
Previous with `N`

- `zz` Center cursor in screen

Config settings related to search:
:set ignorecase		        " case insensitive search
:set smartcase			        " case sensitive if uppercase
:set incsearch			        " move the cursor to first result
