20191016 Vim session
---------------------

Notes for the Vim session at the `UH Biocomputation Group <https://biocomputation.herts.ac.uk>`__.

Part 1: The Vim way: design, concepts, usage
=============================================

In this part, we use Vim without any plug-ins. The idea is to show how Vim is
meant to be used in its standard form.

:code:`gvim -u NONE`

Then remember to use :code:`:set showcmd` so we can see the key-presses.

Download a test file to try out these commands. For example, this document, or
the `GNU GPLv3 license text <https://www.gnu.org/licenses/gpl-3.0.txt>`__ for a
longer one.


Vim modes
##########

These are a few of the available modes in VIM.
Please look at :code:`help vim-modes-intro` for a complete description.

1. Normal mode: default mode where you should be if you are not editing text.
2. Insert mode: only be in this if you are editing text. As soon as you finish,
   go back to Normal mode.
3. Last line mode/command line mode: this is where we write Vim commands.
4. Visual mode: for selecting text. :code:`:help visual-mode`

Beginner's note: use :code:`u` in Normal mode to undo any changes.

Simple cursor movement
########################

Designed for `touch-typing <https://en.wikipedia.org/wiki/Touch_typing>`__.

Open a new file, try out these commands in normal mode: :code:`h, j, k, l, Ctrl f, Ctrl b, ctrl u, ctrl d, gg, G, H, M, L, 0, $, ^, zz, (, ), {, }`.

Searching: :code:`/, ?, n, N`.

Command construction
#####################

Commands: mnemonics, easy to remember.
Command composition: :code:`<number><command><text object or motion>`

Try: :code:`w, W, e, E, b, B`.
Then, add numbers before them: :code:`5w, 5E`, and so on.
Try the before commands in the same way where it makes sense: :code:`5h, 5l`.

New command: :code:`5G`.

Now add suffixes: :code:`f<character>, F<character>, t<character>, T<character>`
Add both: :code:`<number>f<character>`

Entering insert mode
#####################

Use :code:`i, I, a, A`.
Use :code:`Escape` or :code:`Ctrl C` to return to Normal mode.

Only remain in insert mode as long as you have to. Return to Normal model ASAP.  Normal mode should be your default mode. This is different from other editors where insert mode is generally default.

More mnemonics: :code:`c, C, d, D, r, R, x, s, o, O`.

Combined commands: :code:`cw, 3cW, c$, C`.

More text objects
#################

:code:`aw, iw, as, is, ap, ip, a", i", a', i', a), i), a}, i}, a], i]`.

Combine with :code:`d, c`, for example.


Insert mode!
############

Write, exit.

Some short-cuts too:

:code:`ctrl w, ctrl h, ctrl u`


Command/Last line mode
#######################

:code:`:..`, for example: :code:`:help, :w, :q, :wq` and lots more.
Command history: :code:`q:`

Buffers, windows (views), tabs (layouts)
#########################################

Yes, VIM does windows and layouts, but you probably don't need them.

Buffers: are files that are in memory. Open a new file with :code:`e`. Open as many files as you wish---they all open as buffers.
Buffer related commands :code:`:ls, :bnext, :bprev`. You can even add another file to the buffer list without loading it: :code:`:badd`. Delete a buffer with :code:`:bdel`.
Other tricks: :code:`ctrl ^` switches between the most recently used buffer.

Windows are viewports where buffers can be opened. A buffer may be opened in as
many viewports as you wish. Try: :code:`vsplit, split`.

Tabs are not really tabs---they are layouts. In each layout, you can arrange
your viewports. So these come in handy when you are working on different
projects, for example. They are not designed to be used the way tabs in
web-browsers work, even though you can use them that way.

- https://joshldavis.com/2014/04/05/vim-tab-madness-buffers-vs-tabs/
- https://stackoverflow.com/questions/26708822/why-do-vim-experts-prefer-buffers-over-tabs


Folding, indenting, syntax highlighting, completion
####################################################

:code:`z` looks like a fold, so :code:`zo, zc, zO, zC` and so on.

There are different indentation modes, and more can be added using plug-ins.
Same for syntax highlighting.

There's built in completion: :code:`ctrl n, ctrl p, ctrl x ctrl o`.


Part 2: Customising and adding plug-ins
=========================================

Now, we stop using Vanilla VIM and move to my set up. My vimrc file can be
found here: https://github.com/sanjayankur31/vimfiles

Install plug-ins using `vim-plug <https://github.com/junegunn/vim-plug>`__.
Plug-ins live on Github and are able to extend VIM in multiple ways.
Best to use vim-awesome to find a plug-in when you need one.

Some suggested general plugins:

- vim-fugitive
- syntastic
- YouCompleteMe
- nerdcommenter
- ctrlp.vim
- auto-pairs
- tagbar


Also best not to customise from the start. Customise when needed. It is likely
that someone tried it before and wrote up a solution.

Demos
######

Python.
LaTeX.
Markdown.
Rst.

Practising
===========

Use daily. If there's something you want to do, search---someone has probably
already solved your query.

Try `vimgolf <http://www.vimgolf.com/>`__ when you are bored. Lots of fun
exercises, and lots to learn.


References
===========

- https://www.gnu.org/software/gtypist/
- vimtutor
- :help motion
- https://vim.rtorr.com/
- https://blog.carbonfive.com/2011/10/17/vim-text-objects-the-definitive-guide/
- https://vimawesome.com/
