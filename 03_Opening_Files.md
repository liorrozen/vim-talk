# Viewing data

Opening files. Any file that has been read is in it's own buffer
and will stay there until you actually remove it.
For the purpose of this explination, a buffer is loosly equal to a file.

Open several files at the same time in different buffers  

`$ vim file1 file2 file3`

---

# Opening vim with multiple files

- `vim -p file1 file2` Open in tabs
- `vim -o/-O file1 file2` Open in splits

## Known location - close to current working tree (:pwd and :cd)
- `:e[dit]` filename ` Open new buffer in foreground
- `:tabe[dit]` filename ` Open new tab in foreground

## Unknown location - browse tree from current working tree

Launch vim on a folder to :Explore it

- `:E[xplore]`
- `:Vex[plore]`
     <Enter> open file/folder
     <t> open in new tab
     Mouse can work too

## Recently edited files

- `:bro[wse] ol[dfiles] [!]`
  This will display a list of recently edited files and allow the user to select which one to open by number.
  Use [!] to abandon an unsaved buffer.

- `:b#`
  This will toggle between the last opened buffer

## Edit from STDIN

- `vim -` Open data from STDIN
- `cat dev.log | grep ERROR | vim -`
- `ls -lr /Applications | vim -`

Don't forget to set the filetype:
`:set filetype=ruby`
