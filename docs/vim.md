
# Vim Cheatsheet

## Set up
### .vimrc file
sources:

https://stackoverflow.com/questions/2600783/how-does-the-vim-write-with-sudo-trick-work

https://blogs.cuit.columbia.edu/jp3864/2021/02/09/customize-your-vim-how-to-add-line-numbers-colors-and-cursor-to-your-vim/ 

https://linuxhandbook.com/vim-color-schemes/

when :w !sudo tee% fails:
create with text editor in $/Users/your_username/.vimrc
``` 
```

### Preview vim colorschemes
Open a document with vim

```bash 
:colorscheme ctrl + d
```
blue,
darkblue,
default,
delek,
desert,
elflord,
evening,
habamax,
*industry,
koehler,
murphy,
lunaperche, 
*pablo,
morning,
peachpuff,
quiet,
ron,
shine,
*slate,
torte,
zellner

* my favorites
### To preview vim colors
:colo <any from above>

BONUS: will display inline in terminal when file closed so you can see all the colorschemes selected inline.

## My .vimrc settings
```txt
syntax on
set number
colorscheme slate
set mouse=a
```
### On demand in vim

## Turn on syntax highlighting
:syntax on
## Turn on line numbers
:set number
## Set color scheme
:colorscheme slate
## Turn on mouse use
:set mouse=a

## Set Line Numbers
:set number


