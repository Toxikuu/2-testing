NAME="guile"
VERS="3.0.10"
DESC="Portable, embeddable Scheme implementation written in C"
CATG="dev lib"
UPST="https://git.savannah.gnu.org/git/guile.git"
DEPS=()

SOURCE="https://ftp.gnu.org/gnu/guile/guile-$VERS.tar.xz"
EXTRA=()

2b() {

cfg
mk
mi

mkdir -pv                              "$D"/usr/share/gdb/auto-load/usr/lib
mv -vf "$D"/usr/lib/libguile-*-gdb.scm "$D"/usr/share/gdb/auto-load/usr/lib

}
