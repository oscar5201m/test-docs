# .vimrc

```vim
set number
set backspace=indent,eol,start
set whichwrap=b,s,h,l,<,>,[,],~

set showcmd
set showmatch
set title
set noswapfile

set laststatus=2
set statusline=%F%m\ %=\ [ENC=%{&fenc!=''?&fenc:&enc}]\ [TYPE=%Y]\ [CODE=0x%02B]\ [POS=%l/%L(%02v)]

set tabstop=4
set shiftwidth=4
set expandtab

"set tags+=/usr/src/tags

" Highlight Zenkaku Space
function! ZenkakuSpace()
    highlight ZenkakuSpace cterm=reverse ctermfg=DarkMagenta gui=reverse guifg=DarkMagenta
endfunction
if has('syntax')
    augroup ZenkakuSpace
        autocmd!
        autocmd ColorScheme * call ZenkakuSpace()
        autocmd VimEnter,WinEnter * match ZenkakuSpace /　/
    augroup END
    call ZenkakuSpace()
endif

inoremap { {}<LEFT>
"inoremap [ []<LEFT>
"inoremap ' ''<LEFT>
"inoremap " ""<LEFT>

command W w
command Q q
command Wq wq

call plug#begin()
    Plug 'preservim/nerdtree'
    Plug 'tpope/vim-commentary'
    Plug 'ctrlpvim/ctrlp.vim'
    Plug 'simeji/winresizer'
    Plug 'pechorin/any-jump.vim'
    Plug 'nathanaelkane/vim-indent-guides'
    Plug 'tomasiser/vim-code-dark'
call plug#end()

nnoremap <C-t> :NERDTreeToggle<CR>

nmap <C-k> gcc
vmap <C-k> gc
imap <C-k> <Esc>VgccA

let g:indent_guides_enable_on_vim_startup=1
let g:indent_guides_auto_colors=0
autocmd VimEnter,Colorscheme * :hi IndentGuidesOdd ctermbg=235
autocmd VimEnter,Colorscheme * :hi IndentGuidesEven ctermbg=235
let g:indent_guides_guide_size=1
let g:indent_guides_start_level=1

syntax enable
colorscheme codedark
```

