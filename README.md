# emacs-void
Installing emacs-30 from souce on voidlinux

```shell
git clone https://github.com/emacs-mirror/emacs
	
cd emacs

git checkout remotes/origin/emacs-30

sudo xbpx-install autoconf make gcc texinfo gtk+3-devel libXaw-devel libgccjit-devel jansson-devel giflib-devel pkgconf gnutls-devel tree-sitter-devel ncurses-devel

./autogen.sh

./configure CFLAGS='-march=native -mtune=native -O3 -fomit-frame-pointer' --with-tree-sitter --with-xft --with-xml2 --with-x-toolkit=lucid --with-json --with-native-compilation

make bootstrap -j

sudo make install
```
