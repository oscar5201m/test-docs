# vim-plug

A minimalist Vim plugin manager.

Github: [junegunn/vim-plug](https://github.com/junegunn/vim-plug)



<br>

## Installation

### Vim on Unix

```bash
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```


<br>

## Usage

Add a vim-plug section to ``~/.vimrc``.

For example,
```vim
call plug#begin()

" List your plugins here
Plug 'tpope/vim-sensible'

call plug#end()
```

After you add vim-plugs, you can execute a command like
``:PlugInstall`` in any file via vim.


