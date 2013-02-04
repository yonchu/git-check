git-check
=======================

Check git status and check if git remote repositories is updated.

![sample01](https://raw.github.com/yonchu/git-check/master/img/sample01.png)

![sample02](https://raw.github.com/yonchu/git-check/master/img/sample02.png)

Usage
-----------------------

```
Usage:
git-check [-s|-r|-w] [-f <Repositories list file>] [Directory ...]

Options:
  -s : Check git status.
  -r : Check if git remote repositories is updated.
  -w N : Indent width.(Default: 4)
  -f [File] : The file in which Wrote the path to repositories.
```

Check git status in current directory:

```console
$ git-check -s
### Check status:
[.] (master)
 M hoge.txt
 D README
A  fuga.txt
?? piyo.txt
```

Check git remote repositories:

```console
$ git-check -r .vim/bundle/*
### Check remote:
(up to date) [.vim/bundle/EasyMotion](master -> master) URL: git://github.com/vim-scripts/EasyMotion.git
(up to date) [.vim/bundle/jedi-vim](master -> master) URL: git://github.com/davidhalter/jedi-vim.git
    (Not on any branch : prehash=89bd32e) [jedi]
(local out of date) [.vim/bundle/neosnippet](master -> master) URL: git://github.com/Shougo/neosnippet.git
(local out of date) [.vim/bundle/syntastic](master -> master) URL: git://github.com/scrooloose/syntastic.git
(local out of date) [.vim/bundle/unite.vim](master -> master) URL: git://github.com/Shougo/unite.vim.git
(up to date) [.vim/bundle/vim-javascript-syntax](master -> master) URL: git://github.com/jelera/vim-javascript-syntax.git
(up to date) [.vim/bundle/vim-smartword](master -> master) URL: git://github.com/kana/vim-smartword.git
    (not init) [mduem]
(up to date) [.vim/bundle/vim-surround](master -> master) URL: git://github.com/tpope/vim-surround.git
...
```

Check both status:

```console
$ git-check dotfiles
```

Check repositories in the specified file:

```console
$ cat repos.txt
~/dotfiles
~/dotfiles.local
~/work/dev/github/*

$ git-check -f repos.txt
```

See also
-----------------------

Japanese reference:


