# mon pages

My lazy implementation of personal `man` pages (hence the french pronoun. Or a kickass Rasta command, your choice). I've created my own actual `man`-ual pages before, and [it's not that hard](https://www.cyberciti.biz/faq/linux-unix-creating-a-manpage/), but this is easier (for me, anyway). I use them in conjunction with the actual `man` pages so I can get both the official help for a command as well as the plain language idiot-proof version that I've written myself for myself.

## Recommended install

- Clone the repo.
- Copy the `mon` directory to your home directory.
- Add the following function to your `.zshrc` or `.bashrc` file:

```
# MON PAGES
# ........................................................................
mon() {
  less ~/mon/"$1"
}
```

## Usage

Type the following in your terminal:

```
mon file
```

where `file` is the name of a file inside the `mon` directory. When you're done reading, hit `q` to quit.

## 'mon' files

The files inside the `mon` directory are just plain text files, written in markdown format, and named logically so that they're easy to remember without having to `ls` the directory every time. The ones currently in this repo are the ones I've created, and you are encouraged to edit/rename/remove/add/hack them however you see fit. The point is for them to serve as useful references for __you__, and everyone is different, so do whatever works for you. This is essentially a handy way to quickly reference notes you've written for yourself.

Note that the `mon` files in this repo will likely change as I update and add to them over time, so feel free to fork your own copy!
