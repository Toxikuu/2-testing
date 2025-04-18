NAME="guile"
VERS="3.0.10"
DESC="Portable, embeddable Scheme implementation written in C"
CATG="dev lib"
UPST="https://git.savannah.gnu.org/git/guile.git"
VCMD="git ls-remote --tags --refs $UPST | sed 's@.*/@@' | grep '^v[0-9]' | grep -Ev 'rc|alpha|beta' | sort -V | tail -n1"
DEPS=(
    "gc"
)

SOURCE="https://ftp.gnu.org/gnu/guile/guile-$VERS.tar.xz"
EXTRA=()

2b() {

cfg
mk
mi

mkdir -pv                              "$D"/usr/share/gdb/auto-load/usr/lib
mv -vf "$D"/usr/lib/libguile-*-gdb.scm "$D"/usr/share/gdb/auto-load/usr/lib

}
