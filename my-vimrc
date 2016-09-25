"
" My vimrc 
" some settings are from mhinz/vim-galore minimal-vimrc

" You want Vim, not vi. When Vim finds a vimrc, 'nocompatible' is set anyway.
" We set it explicitely to make our position clear!
set nocompatible

" show line number
set number

filetype plugin indent on  " Load plugins according to detected filetype.
syntax on                  " Enable syntax highlighting.

set autoindent             " Indent according to previous line.
set expandtab              " Use spaces instead of tabs.
set softtabstop =4         " Tab key indents by 4 spaces.
set shiftwidth  =4         " >> indents by 4 spaces.
set shiftround             " >> indents to next multiple of 'shiftwidth'.

set backspace   =indent,eol,start  " Make backspace work as you would expect.
set hidden                 " Switch between buffers without having to save first.
set laststatus  =2         " Always show statusline.
set display     =lastline  " Show as much as possible of the last line.

set showmode               " Show current mode in command-line.
set showcmd                " Show already typed keys when more are expected.

set incsearch              " Highlight while searching with / or ?.
set hlsearch               " Keep matches highlighted.

set ttyfast                " Faster redrawing.
set lazyredraw             " Only redraw when necessary.

set splitbelow             " Open new windows below the current window.
set splitright             " Open new windows right of the current window.

set cursorline             " Find the current line quickly.
set wrapscan               " Searches wrap around end-of-file.
set report      =0         " Always report changed lines.
set synmaxcol   =200       " Only highlight the first 200 columns.

set list                   " Show non-printable characters.
if has('multi_byte') && &encoding ==# 'utf-8'
  let &listchars = 'tab:? ,extends:?,precedes:?,nbsp:±'
else
  let &listchars = 'tab:> ,extends:>,precedes:<,nbsp:.'
endif

" The fish shell is not very compatible to other shells and unexpectedly
" breaks things that use 'shell'.
if &shell =~# 'fish$'
  set shell=/bin/bash
endif

" change default font for gvim
" use <F12> to maximize gvim window 
if has("gui_running")
    set guifont=Droid\ Sans\ Mono\ 11
endif

" set default color scheme
color desert

" VIM-PLUG
call plug#begin()

" plugins
" example: Plug 'nsf/gocode'

Plug 'scrooloose/nerdtree'
Plug 'scrooloose/nerdcommenter'

" updates &runtimepath and initialize plugin system
call plug#end()

" use , as leader
let mapleader=","

" use 'jk' as <esc>
inoremap jk <esc>

" using vim better
inoremap <Down> <nop>
inoremap <Up> <nop>
inoremap <Right> <nop>
inoremap <Left> <nop>

" use <F2> to open or close NERDTree
noremap <F2> :NERDTreeToggle<CR>

" MAKE settings
" use mingw32-make as make program
" set '-f Makefile all' as default option
set makeprg=make
" save the current file
" look for Makefile in the current file directory
" use <F5> to make ('all' target)
noremap <F5> :w \| :lcd %:p:h \| :make all<CR>
" use <F6> to make and run using ('run' target)
noremap <F6> :w \| :lcd %:p:h \| :make all run<CR> 

" VIMRC editing inside VIM
" use ,ev to open vimrc
noremap <Leader>ev :vsplit $MYVIMRC<CR>
" use ,sv to update the vimrc
noremap <Leader>sv :w \| :source $MYVIMRC<CR>

" use ,n to toggle line numbers
noremap <Leader>n :set number!<CR>

noremap <Leader>c :close<CR>
" use - and _ to move a lines down/up
noremap _ ddkP
noremap - ddp

" selecting mappings
nnoremap <space> viw
vnoremap <space> e
nnoremap <S-space> gEviw
vnoremap <S-space> b
" converts to uppercase
inoremap <c-u> <esc>viwUA
nnoremap <c-u> viwUe

" windows movements
nnoremap <Leader>h <c-w>h
nnoremap <Leader>j <c-w>j
nnoremap <Leader>k <c-w>k
nnoremap <Leader>l <c-w>l

nnoremap <Leader>H <c-w>H
nnoremap <Leader>J <c-w>J
nnoremap <Leader>K <c-w>K
nnoremap <Leader>L <c-w>L
