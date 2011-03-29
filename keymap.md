# Cut/Copy/Paste/Modify

## Cut/Delete
+ dd Delete current line
+ \#dd Delete # lines
+ dw Delete current word
+ d$ Delete to end of line
+ D Delete to end of line
+ :#,&d Delete from line # to &
+ "[a-zA-Z0-9]dd Delete line into register [a-zA-Z0-9]
+ "+dd Delete line into host clipboard

## Copy/Yank
+ yy Yank current line
+ Y Yank current line
+ \#yy Yank # lines
+ yw Yank current word
+ y$ Yank to end of line
+ y^ Yank to beginning of line
+ :#,&y Yank from line # to &
+ "[a-zA-Z0-9]yy Yank line into register [a-zA-Z0-9]
+ "+yy Yank line into host clipboard

## Paste/Put
+ p Put current register at cursor
+ P Put current register before cursor
+ "[a-zA-Z0-9]p Put register [a-zA-Z0-9] at cursor
+ "+p put text from clipboard at cursor
+ ]p Put current register WRT indent

## Modify
+ gUw Switch case of word to CAPS
+ guw Switch case of word to lower
+ ~ Switch case of character under cursor
+ g~w Invert case on word
+ r# Replace character under cursor with #
+ ce Replace from cursor to end of word
+ c$ Replace from cursor to end of line
+ c#w Replace # words
+ ci" Replace between double quote pair
+ ci' Replace between single quote pair
+ ci) Replace between () pair
+ ci] Replace between [] pair
+ ci} Replace between {} pair
+ ci> Replace between <> pair
+ cit Replace beetween XML/HTML tag pair
+ <ctrl>A Increment number under cursor
+ <ctrl>X Decrement number under cursor
+ x Delete character under cursor
+ X Delete character before cursor
+ \>\> Indent entire line
+ << Unindent entire line
+ == Autoindent entire line
+ :reg View contents of registers

# Code folding
+ zo Open fold
+ zc Close fold
+ zr Reduce fold level
+ zm Increase fold level
+ zR Reduce all folds
+ zM Increase all folds
+ zj Move to next fold downwards
+ zk Move to next fold upward
+ zd Delte folding
+ zE Delete all folds
+ zf#j Create fold of # lines below cursor
+ :#,& fold Create fold beetween line # and &
+ zfap Create fold of paragpraph
+ zfa} Create fold in {} brackets
+ zfa) Create fold in () brackets
+ zfa] Create fold in [] brackets
+ zfa> Create fold in <> brackets

# Search and Replace
+ /# Find # searching forward
+ ?# Find # searching backward
+ n Continue search downwards
+ N Continue search upwards
+ % Move to matching bracket from under cursor
+ :s/old/new/g Substitude old for new on line with no prompt
+ :#,&s/old/new/g Substitude old for new on lines # to & with no prompt
+ :%s/old/new/g Globally substitude old for new with no prompt
+ :%s/old/new/gc Globally substitude old for new with prompt
