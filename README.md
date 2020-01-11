# Random Ascii Terrain

This is a python script that generates "random ascii terrains" for terminal
decorative purposes.

It will create blocks of characters like this:

```
$ rmap -b 16
▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄▄
█░ ...▀ ▀▒.░.▒▀░▒░░▓▒. ░░▀ ░▓▒▀█
█▒ ▀ .▄▒. ░▒.▀▀▄▄░.▄ ▒▓▄░▒.░▄▒▓█
█.  ▓▀▓▒▓▓▒░ ░ ▀▒▓▓▀░░▓ .▒▒▄▓▓▄█
█▄▓▄░▒░▒ ▓.░ ░▓ ▄▒▓▄▀▓▄▓ .▄.▄▀ █
█▀▄░▓▒▄░ ▒▀▓▓▒░▀▓.▒▄.▓░.▒▄▒▒▄.░█
█▓ ▒▒▒▓ ▓  ▀▓  ▀▒ ▄▓▄▄  ▓▓ ▄▄▄▒█
█▀.▀▄▒▄░▓▓▓░▒ ▄▄▒▄░▄.▄▀▀▄ ░.▄░▀█
█ ▀.▀░▓▓ .▒▄▓░. ▄▄▓░▀░▓.░..▓ ▀░█
█▄.▒▀▒▀▓.▓▓ ▀.▒░▀▀▒▒░   ▒▒▄▓░░ █
█░▄▓░░▓▄░▀▓▓▀▄▓▀ ▀▀▓▀.▒▒.░▄▒▀▓.█
█▀▄▀ ░▓▓.▀░░▄░▀░▄▓▒▒▀ ░▀▄▓░▀░▀▀█
█▄▀.▒▀▒▀░▓.▓▒.▓▓▄ ░.▀ ░▄▓▓▒▀▄▄▒█
█▓░▄. ░▀▓▀▓▒▒ ▓▀▀▓▀▓▒▓▀▀░ .▒ ▒▄█
█...░░▄▄░▄░▓▄▓▄.▒▓ . ▓.░▓ ▀▀▄▀▀█
▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀▀
```

## Requirements

This script requires python 3

## Installation

Just clone the repo and symlink `rmap` onto your `$PATH`

## Usage

This project provides the script `rmap`. When executed by itself it will
display a random set of blocky characters in a "map" block that will fill up
your current terminal window (rows and cols)

### Setting size

Rmap accepts an argument which will be the size of the square produced in
lines. E.g. `rmap 32` will make a square 32 lines tall.

### Setting width

By default rmap will use the size argument to create a square. You can override
the width to make a more rectangular shape with `-w` or `--width`:

```
$ rmap -w 80 10
█.#█▄▄*#▀#▒█#...▄.▓▓█▀▓#▀.▀▀.█▒▄▒**▒▒.███*.▒▄█#▒*▓██▄#▓*▓...▒##▒▓*▓#██▄█..#▄*▀▓▓
▓*▓▓▄▀▀#▄█▄█▄█#▓█#█▀▀▄▀*.▀#.▓▓.▓▓▄#..▒#▓*█#▓▒▓▓*█▄▓█*▀█*▀▀▒.▄#.█▄#▀▓▄.▄▄*▀**▓.#▀
**▀.▄▄█#▓▓▄#▒.▄.▀▀▀█▄▄*▓#▀.*###█▀▄█.*▀▀▓*▄▒▀█▒▒▒.▄.#██.#▒▄▒▒▓.▓▓*#▀▓▀▄*▓▀.#█▄▒*▀
▀▓.█▓▒▓#*##▀*#.▓▓▀▓▄▀*▀*█*▄█▄*▒▓▓#*#▄▓##▄▄█.▓▀#▀▀.▀*▀▓.█▓*..*#*▓.#█▒▄▀█#▄*▒▒.▓..
*#▒▒▄**▄▒#▀▀#▓▄.▄▀█**▓▀#▄▀▓▄.#▄*▄▒#▒#▄▀*▓▒..##▒▒#▀*▓#▀▒▒█▓##██#▀▓#▀▓.█#█▄...▄▓▓█
#▒▓.▒#▓▒█#▄▒▄**█▓▀▒.*..▒*▀#▒▓▒▓*▒▓*▓#▒▀▄▓▀▓..#*█▓..*▀.▄..▒▓▀█▒.▒▒▀.▀▄▄#▄#▒*#*▀▒▄
▀█▀█*▓▒.▓#▄▒.▓#▀▀*▓#▀#▀█*▒▒.*▒▒*.#██#▒▒**█.▀█*#*██▀*█*#.▒▄▒...▓▄▀#█*#..█▀*▄#*.▓▄
▒▓▄▀*.▒▒▓▓█.*▄▒##▒▓▄▒█▀▒*▄*▀▀▓▒▀▄#*█▓▓.▀.▄.▄▄#▒█.*▀▀▒█▓▀▀▒*.█▀▓.▒▒▓▒▒▓██*▒*.▀▒█▄
*#*▀▄▓▓.▄*▄▓▄#▄▒█▓▒.▀*▓█▄▄▄.█▓▒##▀**▓▓▓*#█▀▓▄*▀▀▓.▀█##▄█##.▀.▄▀▄▄▓▒▓▒..█▄*█**▓▒▄
#▓▄#▄###*▓#▓*█.▄..█▓█▒▀#▓▓█#*▄.▀▄.▀█#▓▄##▀▀#.▀▀.#*.***##.*..▀█▒.*#.#▒▒██#▄▓█▒#▄▓
```

### Adding border

You can add a border by using the flag `-b` or `--border`: `rmap -b 32` will
produce a border around the map.

### Specifying a random seed

By using the `-s` or `--seed` option you can specify the random seed to use.
This will allow you to create consistent terrain maps. Use `rmap -s 1700 16`
for example to specify seed *1700*.

### Specifying your own random chars

By default rmap will create terrains from a set of blocky ascii characters. You
can specify which selection of chars it should use to pick from when randomly
generating. It may not use all of them, only a random subset. Use the `--chars`
option to specify a string of chars to use.

```
$ rmap --chars "xy18$." 16
  y  y x8 x8.   y  8 18 1$  x  x
 y. 1 8 1.   y .x18 y   x   1$
 $x  8 yy$8 $  $ 1. 1  1       x
  1    1   8 1y   . 1   1  .  88
y $$   1  x  x $y$ .8   $81  8 x
 8$  $y $   ..$y.8.y .8 x8 x$$$
.$y1y$$$ 8   1. 1  8$$$   y  x.
  8$y1 8$x$81 1y..    .y x8yy  $
x 1$ .      y y  ..xx yy$ .yy  x
.y$ .   8$  .1   .  $$y y.  8
 1.x.1x  8 $ x $ .. 8 $  x11 $1
 $y  y x $ .y1$  $ $x $8x88   $$
     $ x  y11x   $ $. $ y1x x  $
y    .8 $811x1.$          $ 1.x$
8  1. yy 1xx8  18 xy$$   x  .  1
x8 $.....  y.1  $y  .8 8     1 1
```

### Extended chars

You can extend the chars used with the `--extend` option. It will randomly pick
some more blocky characters to use.

```
$ rmap --extend 16
 ▘ #▏▓▘▕ ▏▝▞░ ▒  ▟.▚ ▕ ▌ ▗
 ▝▙ ▛  ▕▟▘▚▌▙ ▓▓▓▘▚▕■■■▍  #▐ ▛ .
▜ ▖■▄▄ █▚▗▓*  ▝▝   ░ ▄#  █ ▕   ▗
  ▗#▛▐  ▗ ▏▍▕.#▗▜# ▍▚▟▀▖   ▗▛▒
▘ ▝▓░▖.█▚▝▎▏  .▟     ▍#▜▘▐ ▕ ▕▘▗
▏▞■■ ▚▐▌  ▜  ▜▜    ▏ ▗▚▓▏  ▎░  ▞
░▕▏ ▒■▞ #▄ ▌■  ▏▕▟▍▚▚  ▚  ▕▄░▐■■
 ▜ ░ .     ▖▍  ▞▞  ▄ ░  ▓ #▍  ▝▍
▀▟▏▒  ▘▗*▖▏░▄ ▍▟▍■█#▌▚░ ▝▏  ▍▏ ▘
▚ ■▒ ▓▘ ▍▀▏   ▜  .▎ ▝  ▙     ░▄▐
▐▘ ▝ ▍▖  ▞▒▌▝ ▌#░▕ ▐ ▀▚▍▍▛▝# ▄ *
*   ▝▏  ▚  ▜      ▌▐▞   ■  ▓░.▚
■▟▘ ▝    ▕▕ ▚ ▞  ▍.▞▄▞*    . ▜▛
▓ ▗ . ▚▝ ▗▍.▛ ■▌▛▀▐░#▝.▎ ▐▄ *▕▒*
░▐ ▄▙ ▘▓█#▎ ░▘ *▟ ▐▐ ■▟    ▙▘▄█▗
    ▀ ▓▘▀ ■▌▐ ▓▒ ▒▟▌▖* ▙ ▍▒▙
```
