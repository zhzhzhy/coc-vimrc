# coc-vimrc

**Configuration of my coc-nvim &amp; Vimrc**

<!-- vim-markdown-toc GFM -->

* [Installation](#installation)
* [Plug.vim install](#plugvim-install)
				* [Unix](#unix)
				* [Windows (PowerShell)](#windows-powershell)
* [vim configuration](#vim-configuration)

<!-- vim-markdown-toc -->

## Installation
- First Install [coc-nvim](https://github.com/neoclide/coc.nvim)
Don't forget to install `nodejs` and `npm`

```bash
sudo apt-get install nodejs npm
```
OR
```bash
sudo pacman -S nodejs npm
```

Note: If you are in China,change the **npm source**(Taobao registry) by following command
```bash
npm config set registry https://registry.npm.taobao.org
```

## Plug.vim install

- Install [plug.vim](https://github.com/junegunn/vim-plug)

[Download plug.vim](https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim)
and put it in the "autoload" directory.

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

## vim configuration
1. Copy vim and coc Scripts to ~/.vimrc & ~/.vim/coc-settings.json

2. Reopen VIM.

3. Wait Coc Extension installing finished

4. Execute :PlugInstall to Finish VIM Plugin install

5. Configure the rest components
