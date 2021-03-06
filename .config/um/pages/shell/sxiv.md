# sxiv --
{:data-section="shell"}
{:data-date="March 19, 2021"}
{:data-extra="Um Pages"}

## SYNOPSIS
X11 image viewer

## IN APP OPTIONS

`q` = quit

`return` = switch to thumbnail

`0-9` = prefix next command

`g` = first page

`G` = last page or image number *count*

`f` = fullscreen

`b` = toggle visibility of info baar

`A` = toggle visibility of alpha channel

`r` = reload

`R` = reload all thumbnail

`D` = remove current image from list and go to next


## IMAGE KEYBOARD COMMANDS

Only available in **image** mode:


### Navigate image list

`n, Space`
: Go count images forward.

`p, Backspace`
: Go count images backward.

`[`
: Go count * 10 images backward.

`]`
: Go count * 10 images forward.

### Handle multi-frame images

`Ctrl-n`
: Go to the next frame of a multi-frame image.

`Ctrl-p`
: Go to the previous frame of a multi-frame image.

`Ctrl-Space`
: Play/pause animation of a multi-frame image.

### Zooming
`+`
: Zoom in

`-`
: Zoom out.

`=`
: Set zoom level to 100%, or count%.

`w`
: Set zoom level to fit image into window.

`e`
: Set zoom level to fit image width to window width.

`E`
: Set zoom level to fit image height to window height.

### Panning
`h, Left`
: Pan image 1/5 of window width or count pixel left.

`j, Down`
: Pan image 1/5 of window height or count pixel down.

`k, Up`
: Pan image 1/5 of window height or count pixel up.

`l, Right`
: Pan image 1/5 of window width or count pixel right.

`H`
: Pan to left image edge.

`J`
: Pan to bottom image edge.

`K`
: Pan to top image edge.

`L`
: Pan to right image edge.

`Ctrl-h, Ctrl-Left`
: Pan image one window width left.

`Ctrl-j, Ctrl-Down`
: Pan image one window height down.

`Ctrl-k, Ctrl-Up`
: Pan image one window height up.

`Ctrl-l, Ctrl-Right`
: Pan image one window width right.

### Rotation
`<`
: Rotate image counter-clockwise by 90 degrees.

`>`
: Rotate image clockwise by 90 degrees.

### Flip

`\`
: Flip image horizontally.

`|`
: Flip image vertically.

### Miscellaneous

`a`
: Toggle anti-aliasing.

`W`
: Resize window to fit image.

## COMMAND LINE OPTIONS

`-f` = fullscreen

`-n` = start at certain number

`-i` = stdin

`-q` = turn off warnings

`-s` = scale to fit screen

`-t` = thumbnail mode

`-z ZOOM` = set zoom level
