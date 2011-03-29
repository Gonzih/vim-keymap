# Cut/Copy/Paste/Modify

## Cut/Delete
+ `dd` Delete current line
+ `#dd` Delete # lines
+ `dw` Delete current word
+ `d$` Delete to end of line
+ `D` Delete to end of line
+ `:#,&d` Delete from line # to &
+ `"[a-zA-Z0-9]dd` Delete line into register [a-zA-Z0-9]
+ `"+dd` Delete line into host clipboard

## Copy/Yank
+ `yy` Yank current line
+ `Y` Yank current line
+ `#yy` Yank # lines
+ `yw` Yank current word
+ `y$` Yank to end of line
+ `y^` Yank to beginning of line
+ `:#,&y` Yank from line # to &
+ `"[a-zA-Z0-9]yy` Yank line into register [a-zA-Z0-9]
+ `"+yy` Yank line into host clipboard

## Paste/Put
+ `p` Put current register at cursor
+ `P` Put current register before cursor
+ `"[a-zA-Z0-9]p` Put register [a-zA-Z0-9] at cursor
+ `"+p` Put text from clipboard at cursor
+ `]p` Put current register WRT indent

## Modify
+ `gUw` Switch case of word to CAPS
+ `guw` Switch case of word to lower
+ `~` Switch case of character under cursor
+ `g~w` Invert case on word
+ `r#` Replace character under cursor with #
+ `ce` Replace from cursor to end of word
+ `c$` Replace from cursor to end of line
+ `C` Replace from cursor to end of line
+ `c#w` Replace # words
+ `ci"` Replace between double quote pair
+ `ci'` Replace between single quote pair
+ `ci)` Replace between () pair
+ `ci]` Replace between [] pair
+ `ci}` Replace between {} pair
+ `ci>` Replace between <> pair
+ `cit` Replace beetween XML/HTML tag pair
+ `<ctrl> A` Increment number under cursor
+ `<ctrl> X` Decrement number under cursor
+ `x` Delete character under cursor
+ `X` Delete character before cursor
+ `>>` Indent entire line
+ `<<` Unindent entire line
+ `==` Autoindent entire line
+ `:reg` View contents of registers

# Code folding
+ `zo` Open fold
+ `zc` Close fold
+ `zr` Reduce fold level
+ `zm` Increase fold level
+ `zR` Reduce all folds
+ `zM` Increase all folds
+ `zj` Move to next fold downwards
+ `zk` Move to next fold upward
+ `zd` Delte folding
+ `zE` Delete all folds
+ `zf#j` Create fold of # lines below cursor
+ `:#,& fold` Create fold beetween line # and &
+ `zfap` Create fold of paragpraph
+ `zfa}` Create fold in {} brackets
+ `zfa)` Create fold in () brackets
+ `zfa]` Create fold in [] brackets
+ `zfa>` Create fold in <> brackets

# Search and Replace
+ `/#` Find # searching forward
+ `?#` Find # searching backward
+ `n` Continue search downwards
+ `N` Continue search upwards
+ `%` Move to matching bracket from under cursor
+ `:s/old/new/g` Substitude old for new on line with no prompt
+ `:#,&s/old/new/g` Substitude old for new on lines # to & with no prompt
+ `:%s/old/new/g` Globally substitude old for new with no prompt
+ `:%s/old/new/gc` Globally substitude old for new with prompt

# External Calls
+ `:! <command>` Execute an external command in the shell
+ `:r <file>` Insert the contents of file at cursor position
+ `:r !<command>` Insert ouptut of command at cursor position

# Tabs
+ `:tabnew` Open a new tab
+ `:tabe <file>` Open file in a new tab
+ `<ctrl> PgUp` Switch to tab on Right
+ `<ctrl> PgDn` Switch to tab on Left
+ `:tabdo <command>` Run command in all tabs

#Panes
+ `:vnew` Split window/pane vertically
+ `:new` Split window/pane horizontally
+ `<ctrl> W + H` Switch to pane to the left
+ `<ctrl> W + L` Switch to pane to the right
+ `<ctrl> W + J` Switch to pane to the below
+ `<ctrl> W + K` Switch to pane to the above
+ `<ctrl> W + _` Give all vertical space to current pane
+ `<ctrl> W + |` Give all horizontal space to current pane
+ `<ctrl> W + =` Evenly distribute space for all panes
+ `<ctrl> W + +` Increase current pane height
+ `<ctrl> W + -` Descrease current pane height
+ `<ctrl> W + >` Increase current pane width
+ `<ctrl> W + <` Descrease current pane width

# File
+ `:e <file>` Open file
+ `:enew` New file
+ `:w` Save current file
+ `:w <file>` Save current file as filename
+ `:wq` Save and quit
+ `:x` Save and quit
+ `:q` Quit
+ `:q!` Force quit
+ `:bd` Delete/close buffer
+ `:hardcopy` Print file

# Location
+ `<crtl> G` Show current position in file
+ `:f` Show line numbers
+ `m[a-zA-Z]` Place mark [a-zA-Z] at cursor
+ `` `[a-zA-Z]`` Goto mark [a-zA-Z]
+ `:marks` Show all marks

# Text Insertion
+ `i` Insert text before cursor
+ `I` Insert text at beginning of line
+ `R` Start overtype mode
+ `a` Insert text after cursor
+ `A` Insert text af end of line
+ `o` Open new line following current line
+ `O` Open new line before current line
+ `v` Switch to visual selection mode
+ `V` Switch to visual line selection mode
+ `<crtl> v` Switch to visual block selection mode

# Movement
+ `h` Move cursor left
+ `l` Move cursor right
+ `j` Move cursor down
+ `k` Move cursor up
+ `gj` Move cursor down one display line
+ `gk` Move cursor up one display line
+ `H` Move cursor to top of display
+ `M` Move cursor to middle of display
+ `L` Move cursor to bottom of display
+ `w` Move cursor forward to start of next word
+ `e` Move cursor to end of next word
+ `b` Move cursor backward one word
+ `)` Move cursor forward one sentence
+ `(` Move cursor backward one sentence
+ `0` Move cursor to start of line
+ `^` Move cursor to first character of line
+ `$` Move cursor to end of line
+ `<ctrl> F` Move cursor forward one screenful
+ `<ctrl> B` Move cursor backward one screenful
+ `<ctrl> U` Move cursor up half a screenful
+ `<ctrl> D` Move cursor down half a screenful
+ `gg` Move cursor to top of file
+ `G` Move cursor to bottom of file
+ `#G` Move cursor to line #
+ `#gg` Move cursor to line #
+ `f#` Move cursor forward to next character # on line
+ `F#` Move cursor backwards character # on line
+ `t#` Move cursor forward to character before the next character # on line
+ `T#` Move cursor backward to character after the next character # on line

# Macros
+ `q[a-zA-Z0-9]` Start recording macro into register [a-zA-Z0-9]
+ `q` End recording of current macro
+ `@[a-zA-Z0-9]` Playback macro from register [a-zA-Z0-9]
+ `n@[a-zA-Z0-9]` Playback macro from register [a-zA-Z0-9] n times
