Using ESLint with Your Editor
=============================

Linting works best when automated; below are instructions for integrating ESLint with your editor/IDE of choice. If yours isn't listed, please make a PR to add it! You can also check out ESLint's guide to editor integration [here](http://eslint.org/docs/user-guide/integrations.html).

## Contents
* [Atom](#atom)
* [Emacs](#emacs)
* [Sublime](#sublime)
* [Vim](#vim)

## Atom
[linter-eslint](https://atom.io/packages/linter-eslint) can be installed via `$ npm install linter-eslint`.

[⬆ back to top](#contents)

## Emacs
[Flycheck](https://github.com/flycheck/flycheck) is probably your best bet. [This tutorial](http://codewinds.com/blog/2015-04-02-emacs-flycheck-eslint-jsx.html) walks you through installation and configuration for ESLint, including great information on Babel.io and React/JSX integration.

[⬆ back to top](#contents)

## SublimeText
[SublimeLinter-eslint](https://github.com/roadhump/SublimeLinter-eslint) is maintained and seems to work well (requires [SublimeLinter 3](http://sublimelinter.readthedocs.org/en/latest/)).

[⬆ back to top](#contents)

## Vim
[Syntastic](https://github.com/scrooloose/syntastic) is your best bet. Install it via [Pathogen](https://github.com/tpope/vim-pathogen) and ensure the following are in your `.vimrc`:

```vimscript
" Use Pathogen
execute pathogen#infect()

" Settings for Syntastic (https://github.com/scrooloose/syntastic)
set statusline+=%#warningmsg#
set statusline+=%{SyntasticStatuslineFlag()}
set statusline+=%*

let g:syntastic_always_populate_loc_list = 1
let g:syntastic_auto_loc_list = 1
let g:syntastic_check_on_open = 1
let g:syntastic_check_on_wq = 0
let g:syntastic_javascript_checkers = ['eslint']
```

[⬆ back to top](#contents)
