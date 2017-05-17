# config
# Make vim to be python IDE
* vim extension: vundle
```
$ git clone https://github.com/gmarik/Vundle.vim.git ~/.vim/bundle/Vundle.vim
```
.vimrc 
```
set nocompatible              " required
filetype off                  " required

" set the runtime path to include Vundle and initialize
set rtp+=~/.vim/bundle/Vundle.vim
call vundle#begin()

" alternatively, pass a path where Vundle should install plugins
"call vundle#begin('~/some/path/here')

" let Vundle manage Vundle, required
Plugin 'gmarik/Vundle.vim'

" Add all your plugins here (note older versions of Vundle used Bundle instead of Plugin)


" All of your Plugins must be added before the following line
call vundle#end()            " required
filetype plugin indent on    " required
```
* Code Folding
```
Plugin 'tmhedberg/SimpylFold'
```
```
" Enable folding
set foldmethod=indent
set foldlevel=99
```
```
" Enable folding with the spacebar
nnoremap <space> za
```
* Python Indentation
    * PEP8 
    ```
    au BufNewFile,BufRead *.py
    \ set tabstop=4 |
    \ set softtabstop=4 |
    \ set shiftwidth=4 |
    \ set textwidth=79 |
    \ set expandtab |
    \ set autoindent |
    \ set fileformat=unix
    ```
* Auto-Indentation
```
Plugin 'vim-scripts/indentpython.vim'
```
* Flagging Unnecessary Whitespace
```
highlight BadWhitespace ctermbg=red guibg=#BBBB00
au BufRead,BufNewFile *.py,*.pyw,*.c,*.h match BadWhitespace /\s\+$/
```
* UTF8 Support
```
set encoding=utf-8
```
* Auto-complete
```
Bundle 'Valloric/YouCompleteMe'
```
* ensure autocomplete window go away
```
let g:ycm_autoclose_preview_window_after_completion=1 
map <leader>g  :YcmCompleter GoToDefinitionElseDeclaration<CR>
```
* use brew doctor to debug
* Syntax Checking/Highlighting
```
Plugin 'scrooloose/syntastic'
```
```
Plugin 'nvie/vim-flake8'
```
* File Browsing
```
Plugin 'scrooloose/nerdtree'
```
* Super Searching
```
Plugin 'kien/ctrlp.vim'
```
* Git Integration
```
Plugin 'tpope/vim-fugitive'
```
# Reference
[VIM and Python - a match made in headven](https://realpython.com/blog/python/vim-and-python-a-match-made-in-heaven/)

###### tags:`python`, `vim`
