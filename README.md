# coc-vimrc

**Configuration of my coc-nvim &amp; Vimrc**

<!-- vim-markdown-toc GFM -->

* [Installation](#installation)
* [Plug.vim install](#plugvim-install)
				* [Unix](#unix)
				* [Windows (PowerShell)](#windows-powershell)
* [Plugin explanation & key mapping](#plugin-explanation--key-mapping)
	* [coc.nvim](#cocnvim)
	* [kotlin-vim](#kotlin-vim)
	* [vim-visual-multi](#vim-visual-multi)
	* [undotree](#undotree)
	* [vim-easy-align](#vim-easy-align)
	* [calendar.vim](#calendarvim)
	* [vim-autoformat](#vim-autoformat)
	* [vim-gitgutter](#vim-gitgutter)
	* [vim-surround](#vim-surround)
	* [vim-markdown-toc](#vim-markdown-toc)
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
## Plugin explanation & key mapping


### coc.nvim

Repo link: [coc.nvim](https://github.com/neoclide/coc.nvim)

### kotlin-vim

Repo link: [kotlin-vim](https://github.com/udalov/kotlin-vim)

### vim-visual-multi

Repo link: [vim-visual-multi](https://github.com/mg979/vim-visual-multi)

### undotree

Repo link: [undotree](https://github.com/mbbill/undotree)

### vim-easy-align

Repo link: [vim-easy-align](https://github.com/junegunn/vim-easy-align)

### calendar.vim

Repo link: [calendar.vim](https://github.com/itchyny/calendar.vim)

### vim-autoformat

Repo link: [vim-autoformat](https://github.com/Chiel92/vim-autoformat)

### vim-gitgutter

Repo link: [vim-gitgutter](https://github.com/airblade/vim-gitgutter)

### vim-surround

Repo link: [vim-surround](https://github.com/tpope/vim-surround)

### vim-markdown-toc

Repo link: [vim-markdown-toc](https://github.com/mzlogin/vim-markdown-toc)

## vim configuration
1. Copy vim and coc Scripts to ~/.vimrc & ~/.vim/coc-settings.json

2. Reopen VIM.

3. Wait Coc Extension installing finished

4. Execute :PlugInstall to Finish VIM Plugin install

5. Configure the rest components
