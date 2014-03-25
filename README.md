NERD-tree-project
=================
A VIM plugin shows you the project directory in NERD tree.

Author: Janlay Wu <janlay@gmail.com>    
Version: 0.1

## Description
  This plugin works together with [NERD tree](https://github.com/scrooloose/nerdtree).
  It tries to resolve root project directory for current file,
  and calls NERD_tree in that directory.
  If no project found, then calls NERD_tree in current directory.

## Install
### Install manually
First, make sure [NERD tree](https://github.com/scrooloose/nerdtree) is installed properly. Then put NERD_tree_project.vim in `~/.vim/plugin` (*nix) or `$HOME/vimfiles/plugin` (Windows)

### Use pathogen
You may want to install it with [pathogen.vim](https://github.com/tpope/vim-pathogen):

    cd ~/.vim/bundle
    git clone https://github.com/scrooloose/nerdtree.git`

## Usage
Type in normal mode:

    ToggleNERDTree<CR>
or map shortcut in your .vimrc file:

    `map <F8> :ToggleNERDTree<CR>`

## Customize
Make NERD_tree Project to recognize more project, such as scons:

    `let g:NTPNames = add(g:NTPNames, 'SConstruct')`
or add more file types:

    `extend(g:NTPNames, ['*.sln', '*.csproj'])`
You may want to set g:NTPNamesDirs to define directory patterns:

    `let g:NTPNamesDirs = ['.git', '*.xcodeproj', '*.xcworkspace']`

## License
  Check the MIT license