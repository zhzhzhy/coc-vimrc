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
			* [Basic usage:](#basic-usage)
			* [Documentation](#documentation)
			* [Wiki](#wiki)
		* [undotree](#undotree)
			* [Usage](#usage)
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
			* [Usage](#usage-1)
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

| Shortcut     | Action                                             |
| :------------: | :--------------------------------------------------: |
| `Ctrl`+`n`   | **Select next key (multiple cursors)**             |
| `q`          | **Deselect the current keys (multiple cursors)**   |
| `N`          | Select the previous key                            |
| `n`          | Select the next key                                |
| `Esc`        | Quit mutiple cursors                               |

To minimize chances for conflicts, a leader that is specific to VM is defined. The default is `\\` (two backslashes), but you can change it by setting:

```
let g:VM_leader = {your VM leader}
```

##### Basic usage:

- select words with <kbd>Ctrl-N</kbd> (like `Ctrl-d` in Sublime Text/VS Code)
- create cursors vertically with <kbd>Ctrl-Down</kbd>/<kbd>Ctrl-Up</kbd>
- select one character at a time with <kbd>Shift-Arrows</kbd>
- press <kbd>n</kbd>/<kbd>N</kbd> to get next/previous occurrence
- press <kbd>[</kbd>/<kbd>]</kbd> to select next/previous cursor
- press <kbd>q</kbd> to skip current and get next occurrence
- press <kbd>Q</kbd> to remove current cursor/selection
- start insert mode with <kbd>i</kbd>,<kbd>a</kbd>,<kbd>I</kbd>,<kbd>A</kbd>

Two main modes:

- in _cursor mode_ commands work as they would in normal mode
- in _extend mode_ commands work as they would in visual mode
- press <kbd>Tab</kbd> to switch between «cursor» and «extend» mode

Most vim commands work as expected (motions, <kbd>r</kbd> to replace characters, <kbd>~</kbd> to change case, etc). Additionally you can:

- run macros/ex/normal commands at cursors
- align cursors
- transpose selections
- add patterns with regex, or from visual mode

And more... of course, you can enter insert mode and autocomplete will work.


##### Documentation

    :help visual-multi

For some specific topic it's often:

    :help vm-some-topic

##### [Wiki](https://github.com/mg979/vim-visual-multi/wiki)

The wiki was the first documentation for the plugin, but many pictures are
outdated and contain wrong mappings. Still, you can take a look.

You could read at least the [Quick Start](https://github.com/mg979/vim-visual-multi/wiki/Quick-start).
 
 Quick refer the [Key mapping](https://github.com/mg979/vim-visual-multi/wiki/Mappings)

Insert mode with autocomplete, alignment (mappings in pic have changed, don't trust them)

![Imgur](https://i.imgur.com/u5pPY5W.gif)

-------
Undo/Redo edits and selections

![Imgur](https://i.imgur.com/gwFfUxq.gif)

-------
Alternate cursor/extend mode, motions (even %), reverse direction (as in visual mode) and extend from the back. At any time you can switch from extend to cursor mode and viceversa.

![Imgur](https://i.imgur.com/ggQr1Ve.gif)

-------
Select inside/around brackets/quotes/etc:

![Imgur](https://i.imgur.com/GAXQLao.gif)

-------
Select operator, here shown with 'wellle/targets.vim' plugin: sib, sia, saa + selection shift

![Imgur](https://i.imgur.com/yM3Fele.gif)

-------
Synched column transposition

![Imgur](https://i.imgur.com/9JDaLBi.gif)

-------
Unsynched transposition (cycle all regions, also in different lines)

![Imgur](https://i.imgur.com/UQOCxyf.gif)

-------
Shift regions left and right (M-S-\<\>)

![Imgur](https://i.imgur.com/Q7EF8YI.gif)

------
Find words under cursor, add new words (patterns stack), navigate regions, skip them, add regions with regex.

![Imgur](https://i.imgur.com/zWtelNO.gif)

#### [undotree](https://github.com/mbbill/undotree)

![](https://sites.google.com/site/mbbill/undotree_new.png)

##### Usage

| Shortcut                  | Action                       |
| :----:                    | :----:                       |
| `:UndotreeToggle` OR `F5` | toggle the undo-tree panel.  |
| `:redo` OR `<ctrl-r>`     | restore                      |
| `[ number ]`              | marks the most recent change |

 1. Use `:UndotreeToggle` to toggle the undo-tree panel. You may want to map this command to whatever hotkey by adding the following line to your vimrc, take `F5` for example.
```
nnoremap <F5> :UndotreeToggle<CR>
```
 1. Markers
    * Every change has a sequence number and it is displayed before timestamps.
    * The current state is marked as `> number <`.
    * The next state which will be restored by ``:redo`:redo` or ``<ctrl-r>`<ctrl-r>` is marked as `{ number }`.
    * The `[ number ]` marks the most recent change.
    * The undo history is sorted by timestamps.
    * Saved changes are marked as `s` and the big `S` indicates the most recent saved change.
 1. Press `?` in undotree window for quick help.
 1. Persistent undo
    * Usually I would like to store the undo files in a seperate place like below.

```
if has("persistent_undo")
   let target_path = expand('~/.undodir')

    " create the directory and any parent directories
    " if the location does not exist.
    if !isdirectory(target_path)
        call mkdir(target_path, "p", 0700)
    endif

    let &undodir=target_path
    set undofile
endif
```

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

Make `<tab>` used for trigger completion, completion confirm, snippet expand and jump like VSCode.


#### [coc-explorer](https://github.com/weirongxu/coc-explorer)

#### [coc-translator](https://github.com/voldikss/coc-translator)
 

## vim configuration
1. Copy vim and coc Scripts to ~/.vimrc & ~/.vim/coc-settings.json

2. Reopen VIM.

3. Wait Coc Extension installing finished

4. Execute :PlugInstall to Finish VIM Plugin install

5. Configure the rest components
