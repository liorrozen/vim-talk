# Accessing the shell

The `!` character on the command line essentially releases the rest of the command to the shell
after some basic substitutiions.

- `%` Current file name.
- `%:p:h` Folder name of current file.

### Pipe current buffer to shell command (file doesn’t exist yet):
`:w !grep search-term`

### Read output of command into buffer:
`:r !curl icanhazip.com`

### Pipe current buffer contents to shell command and override range of lines in current buffer with output:
`:% !grep -c meta`

### Execute shell command with :!command %
`:!bundle exec ruby %` Execute current file.

### View output of last commands without leaving vim:
`:!`
