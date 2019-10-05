---
title: GVim Resource Configuration File
published: true
---   

# GVim 8.x RC File by Pil-Jin.Kwon    

`$ vi ~/.vimrc`    


```rc
set hls
set expandtab
set ic
set nobackup
set nu
set ts=4
set softtabstop=4
set shiftwidth=4
set formatoptions=croql
set ruler
set showmode
set smartindent
set ff=dos
set statusline=\ %<%l:%v\ [%P]%=%a\ %h%m%r\ %F\
"syntax on
"filetype indent on

map <F7> :w<cr>:!gcc -Wall % -o %< && ./%<<cr>
map <F5> :<CR>:!./%<<CR>


map ,n :cn<ENTER>
map ,p :cp<ENTER>
map ,l :cl<ENTER>
map ,w :cw<ENTER>


vmap ,c :s/^/\/\//g<ENTER>
vmap ,uc :s/^\/\///g<ENTER>


ab pf printf(


"map <F5> :so $VIMRUNTIME/syntax/2html.vim<CR>
"colorscheme slate
set encoding=utf-8
set termencoding=utf-8
```   

