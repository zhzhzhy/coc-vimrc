# coc-vimrc

Configuration of my coc-nvim &amp; Vimrc

1. Installation
- First Install [coc-nvim](https://github.com/neoclide/coc.nvim)

- Install [plug.vim](https://github.com/junegunn/vim-plug)

[Download plug.vim](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim)
and put it in the "autoload" directory.

#### Vim

###### Unix

```sh
curl -fLo ~/.vim/autoload/plug.vim --create-dirs \
    https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim
```

You can automate the process by putting the command in your Vim configuration
file as suggested [here][auto].

[auto]: https://github.com/junegunn/vim-plug/wiki/tips#automatic-installation

###### Windows (PowerShell)

```powershell
iwr -useb https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim |`
    ni $HOME/vimfiles/autoload/plug.vim -Force
```


2. Copy vim and coc Scripts to ~/.vimrc & ~/.vim/coc-settings.json

3. Reopen VIM.

4. Wait Coc Extension installing finished

5. Execute :PlugInstall to Finish VIM Plugin install

6. Configure the rest components
