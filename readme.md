
# select-one

`select-one` is a versatile little python script I wrote when I found myself grepping through code, selecting a line of output, and running 'subl3 *line*' to open it in my IDE.

`select-one` reads lines from stdin and displays a curses selection UI to select a line, then it launches a command replacing `{}` in the arguments with the selected line (similar to the `find -exec` flag).

An example of how I routinely use it:

    grep -rin 'todo' | select-one subl3 {}

A smaller demo:

    seq 0 10 | select-one notify-send 'You chose' 'This one: {}'

Another common use (select a music file and play in mpv):

    find ./music -name '*.mp3' | select-one mpv {}


# Dependencies

 - python3


