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

1. Normal mode: default mode where you should be if you are not editing text.
2. Insert mode: only be in this if you are editing text. As soon as you finish,
   go back to Normal mode.
3. Last line mode/command mode: this is where we write Vim commands.

Beginner's note: use :code:`u` to undo.

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
