# Buffers

## [b]uffer - Work with more than one data source.

- List buffers  
  `:ls`
- Jump to buffer number or name
  `:b <buffer-number>`  
  `:b <partial-filename>`
- Next buffer
  `:bn`
- Previous buffer  
  `:bp`
- Toggle last show buffer  
  `:b#` 

---

## Open a new blank buffer from within vim:  

- `:enew` - in current window
- `:new` - as a horizontal split
- `:vnew` - as vertical split

---

## Splits

Split window vertical

- `:vsplit`
- `:vsp`

Split window horizontal

- `:split`
- `:sp`

---

## Navigate between buffers

If mouse is enabled, you can click to move between splits/tabs
Reordering tabs with dragging also works

- `<Ctrl+w> <direction>` Navigate between splits
- `tabnext` Next tab
- `tabpreb` Previous tab
