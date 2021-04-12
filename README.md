# coc-vimrc

**Configuration of my coc-nvim &amp; Vimrc**


<!-- vim-markdown-toc GFM -->

* [Installation](#installation)
* [Plug.vim install](#plugvim-install)
				* [Unix](#unix)
				* [Windows (PowerShell)](#windows-powershell)
* [Plugin explanation & key mapping](#plugin-explanation--key-mapping)
	* [vim plugins](#vim-plugins)
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
	* [coc-nvim extensions](#coc-nvim-extensions)
		* [Language servers](#language-servers)
			* [coc-clangd](#coc-clangd)
			* [coc-css](#coc-css)
			* [coc-flutter](#coc-flutter)
			* [coc-html](#coc-html)
			* [coc-json](#coc-json)
			* [coc-python](#coc-python)
			* [coc-tsserver](#coc-tsserver)
			* [coc-vimlsp](#coc-vimlsp)
			* [coc-yaml](#coc-yaml)
	* [other coc extensions](#other-coc-extensions)
		* [coc-marketplace](#coc-marketplace)
			* [Usage](#usage)
		* [coc-prettier](#coc-prettier)
			* [Update your `coc-settings.json` for format on save](#update-your-coc-settingsjson-for-format-on-save)
		* [coc-snippets](#coc-snippets)
		* [coc-explorer](#coc-explorer)
		* [coc-translator](#coc-translator)
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

### vim plugins

#### [coc.nvim](https://github.com/neoclide/coc.nvim)

Follow [Installation](#installation)

#### [kotlin-vim](https://github.com/udalov/kotlin-vim)


#### [vim-visual-multi](https://github.com/mg979/vim-visual-multi)


#### [undotree](https://github.com/mbbill/undotree)


#### [vim-easy-align](https://github.com/junegunn/vim-easy-align)


#### [calendar.vim](https://github.com/itchyny/calendar.vim)


#### [vim-autoformat](https://github.com/Chiel92/vim-autoformat)


#### [vim-gitgutter](https://github.com/airblade/vim-gitgutter)


#### [vim-surround](https://github.com/tpope/vim-surround)


#### [vim-markdown-toc](https://github.com/mzlogin/vim-markdown-toc)

### coc-nvim extensions

#### Language servers
##### [coc-clangd](https://github.com/clangd/coc-clangd)
##### [coc-css](https://github.com/neoclide/coc-css)
##### [coc-flutter](https://github.com/iamcco/coc-flutter)
##### [coc-html](https://github.com/neoclide/coc-html)
##### [coc-json](https://github.com/neoclide/coc-json)
##### [coc-python](https://github.com/neoclide/coc-python)
##### [coc-tsserver](https://github.com/neoclide/coc-tsserver)
##### [coc-vimlsp](https://github.com/iamcco/coc-vimlsp)
##### [coc-yaml](https://github.com/neoclide/coc-yaml)

### other coc extensions
 
#### [coc-marketplace](https://github.com/fannheyward/coc-marketplace)
[coc.nvim](https://github.com/neoclide/coc.nvim)  extensions marketplace.

* search `keywords:coc.nvim` from npmjs.com, display extensions in `coc-lists`
* extension name starts with `√` means installed already, with an `uninstall` action
* extension name starts with `x` means uninstalled, with an `install` action
* extension name ends with `*` is published by @chemzqm, IMO, is official

##### Usage

* `:CocList marketplace` list all available extensions
* `:CocList marketplace python` to search extension that name contains `python`

![coc-marketplace](https://i.loli.net/2019/06/06/5cf885c18736a85017.png) 

#### [coc-prettier](https://github.com/neoclide/coc-prettier)
 
    you can use `:Prettier` to format current buffer.
    your can `<leader>f` for range format.

    Prettier range format only support languageId including: `javascript`,
`javascriptreact`, `typescript`, `typescriptreact`, `json` and `graphql`.


##### Update your `coc-settings.json` for format on save

Open settings file with:

    :CocConfig

Add:

```
  "coc.preferences.formatOnSaveFiletypes": ["css", "markdown"],
```

to setup the languages which you want to format on save.

#### [coc-snippets](https://github.com/neoclide/coc-snippets)
 
 | Shortcut                  | Action                                                                                      |
 | :----:                      | :----:                                                                                        |
 | `Insert Mode`  `Ctrl` `l` | coc-snippets-expand<br>(trigger snippet expand)                                                 |
 | `Visual Mode`  `Ctrl` `j` | coc-snippets-select<br>(select text for visual placeholder of snippet)                          |
 | `Ctrl` `j`                | coc_snippet_next<br>(jump to next placeholder, it's default of coc.nvim)                        |
 | `Ctrl` `k`                | coc_snippet_prev<br>(jump to previous placeholder, it's default of coc.nvim)                    |
 | `xmap` `<leader>` `x`     | coc-convert-snippet <br>(Use <leader>x for convert visual selected code to snippet)             |
 | `imap` `<C-j>` `<Plug>`   | coc-snippets-expand-jump <br>(Use <C-j> for both expand and jump (make expand higher priority.) |



#### [coc-explorer](https://github.com/weirongxu/coc-explorer)

#### [coc-translator](https://github.com/voldikss/coc-translator)
 

## vim configuration
1. Copy vim and coc Scripts to ~/.vimrc & ~/.vim/coc-settings.json

2. Reopen VIM.

3. Wait Coc Extension installing finished

4. Execute :PlugInstall to Finish VIM Plugin install

5. Configure the rest components
