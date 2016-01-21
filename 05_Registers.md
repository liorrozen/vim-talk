# Registers

`:reg[isters]` View contents of all registers

All registers begin with the `"` character
Registers are persisted in the `.viminfo` file.

- The unnamed register `""`
    Always contains last deleted/changed/yanked text (last used register)
- 10 numbered registers `"0` to `"9`
    Register `"0` is used for most recent yank command
    Register `"1-9` is used for most recent delete/change command - shifts down and forgotten after 9
- The small delete register `"-`
    Used for deleted text that is less than one line
- 26 named registers `"a` to `"z`
    Any yank/delete/change command can be directed to a named register that will not be overridden
- Three read-only registers `":`, `"-`, `"%`
    `":` Last command line command
    `"-` Last inserted text (last insert mode)
    `"%` Current file/buffer name
- Alternate buffer register `"#`
    Another file in the buffer list - last opened file
- The expression register `"=`
    Evaluate commands- Cursor jumps to command line and is calculated on p[ut]
- The selection and drop registers `"*`, `"+` and `"~`
    Clipboard registers - not relevant for remote connections without clipboard support
- The black hole register `"_`
    /dev/null of registers - Use to not modify numbered registers
- Last search pattern register `"/`
     Last searched text

---

# Macros

Macros are combinations of commands that are recorded into one of the names registers.

- `q` Start recording, press again to stop.
- `qa` Save into the `"a` register.
- `@a` Replay the macro.
- `6@a` Replay the macro 6 times.
