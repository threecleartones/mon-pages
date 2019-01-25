# "mon" pages

NOT actual `man`-ual pages - this is my lazy implementation of personal `man` pages (hence the French pronoun. or a kickass Rasta command, your choice). I've created my own `man` pages before, and [it's not that hard](https://www.cyberciti.biz/faq/linux-unix-creating-a-manpage/), but this is easier (for me, anyway). I use them in conjunction with the actual `man` pages so I can get both the official help for a command as well as the plain language idiot-proof version that I've written myself, for myself.

## Recommended install

1. Clone the repo.
1. Copy the `mon` directory to your home directory.
1. Add the following function to your `.zshrc`\ `.bashrc` file (or corresponding `profile`):

```
# MON PAGES
# ........................................................................
mon() {
  less ~/mon/"$1"
}
```

4. Source the file (or restart your terminal):

```
. ~/.zshrc
```

## Usage

Type the following in your terminal from anywhere:

```
mon file
```

where `file` is the name of a file inside the `mon` directory. When you're done reading, hit `q` to quit.

Example:

```
mon chmod
```

which outputs (via `less`):

```
CHMOD reference
================

7       rwx     111
6       rw-     110
5       r-x     101
4       r--     100
3       -wx     011
2       -w-     010
1       --x     001
0       ---     000

ex.
chmod 666 file.name

results in:
-rw-rw-rw  file.name


/home/jeff/mon/chmod (END)
```

(I really wish the GUN `man` page had this chart, it's the only thing I actually ever need to look up when running `chmod`)
## "mon" files

The files inside the `mon` directory are just plain text files, written in markdown format (or not), and named logically so that they're easy to remember without having to `ls` the directory every time. The ones currently in this repo are the ones I've created so far, and you are encouraged to edit/rename/remove/add/hack them however you see fit. The point is for them to serve as useful references for __you__, and everyone is different, so do whatever works for you. This is essentially a handy way to quickly reference notes you've written for yourself.

Note that the `mon` files in this repo will likely change as I update and add to them over time, so feel free to fork away!

## Uninstall

Just reverse the directions above - remove the `mon` directory from your home directory and the `mon()` function from the zsh/bash file you put it in.

## Next steps

I'm working on a way to add tab completion - at the moment you have to type (and therefore know) the exact name of the mon file. Tab completion looks somewhat straightforward but it differs depending on your shell. Figuring it out for zsh at the moment.
