reload .vimrc
  :so $MYVIMRC
cheat sheet:
http://www.worldtimzone.com/res/vi.html


:a edit
:? search
:x! (save and exit)
:q! (force exit no save)
:v highlight (x to cut, y to copy)
p: paste copied text after cursor
:set nu (show line numbers)
:f (file name)

:u undo
ctrl+r redo



select all
---------
ggVG

copy/cut all
------------
:%y (copy)
:%d (cut)




:%s/foo/bar/g
Find each occurrence of 'foo' (in all lines), and replace it with 'bar'.

:s/foo/bar/g
Find each occurrence of 'foo' (in the current line only), and replace it with 'bar'.

:%s/foo/bar/gc
Change each 'foo' to 'bar', but ask for confirmation first.

:%s/\<foo\>/bar/gc
Change only whole words exactly matching 'foo' to 'bar'; ask for confirmation.

:%s/foo/bar/gci
Change each 'foo' (case insensitive) to 'bar'; ask for confirmation.
This may be wanted after using :set noignorecase to make searches case sensitive (the default).

:%s/foo/bar/gcI
Change each 'foo' (case sensitive) to 'bar'; ask for confirmation.
This may be wanted after using :set ignorecase to make searches case insensitive.
