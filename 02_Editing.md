## Text Objects

Words, Sentences, Paragraphs

- `w` Forward one word
- `b` Backward one word
- `e` Goto end of word

`<number><command><text object or motion>`

Examples: 

- `2dw` Delete two words
- `dip` Delete inner paragraph
- `dap` Delete all paragraph (include surrounding whitespace)

---

# Text Selection

Use `v` / `<Shift-v>` / `<Ctrl+v>` to enter VISUAL

- `V` VISUAL LINE select current line
- `viw` VISUAL select current word 
- `vaw` VISUAL select current word (including whitespace)
- `vip` VISUAL select current paragraph
- `vi<wrapper>` VISUAL select text within wrapper
- `va<wrapper>` VISUAL select text including wrapper
  > "You can use quotes (or brackets) to wrap text"
- `ggVG` Select All (when in NORMAL mode)

This should make more sense now. 
  1. Goto the begining of the file
  2. Enter Visual line mode
  3. Goto end of file (defining end of selection)

- You can also use the mouse to made a VISUAL selection.  
  Config settings for mouse - requires specific compliation flags  
  `:set mouse=a				" enable mouse (disble with mouse= )`

VISUAL BLOCK

- `I` Places cursor at the end of block on the first line.
  Make your changes and hit `<ESC>` to return to repeat for all lines
  and return to NORMAL.
- `A` Same as `I` only at the end of the block

---

# Cut / Copy / Paste

From a visual selection, you can:

- `c`   Cut/Change the text. This will delete the text and
        place you in INSERT mode (in order to change it).
- `d`   Delete the text. This will delete the text and
        return you to normal mode.
- `y`   Yank/Copy the text. This will place the contents of the
        selection in a register.
- `Y`   Yank entire line.
- `p`   Put/Paste the text. This will place the text that was recently
        yanked/changed/deleted into the file at the position of the cursor.

---

# Find and replace

[s]ubstitute

- Single Line
  `:s/fiver/fiverr/`

- Entire file
  `:%s/fiver/fiverr/g`

- From within a visual selection  
  `:'<,'>s/fiver/fiverr/g`
  Press `:` when in VISUAL

It's possible to enter search/repalce commands without even
entering visual mode. Just pass the line numbers:
`9,12s/foo/bar/`

Confirm action - add the `c` flag to the substitution.
`%s/this/that/gc`

---

# Repeat

- `.` Repeats the last change made in NORMAL  
  Example: `dw..` Delete one word and repeat it twice.  

---

# Undo / Redo

> Vim added multilevel undo/redo

- `u` Undo last action  
- `<Ctrl-r>` Redo last action

---

# Auto Indent

- `=` With a VISUAL selection, pressing this key will attempt to autoindent the file
  according to it's filetype
