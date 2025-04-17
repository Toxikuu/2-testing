NAME="pinentry"
VERS="1.3.1"
DESC="Collection of simple PIN entry dialogs"
CATG="lib"
UPST="https://github.com/gpg/$NAME.git"
DEPS=(
    "libassuan"
    "libgpg-error"
)

SOURCE="https://www.gnupg.org/ftp/gcrypt/$NAME/$NAME-$VERS.tar.bz2"
EXTRA=()

2b() {

# fltk=1.4.1 consistency
sed -i "/FLTK 1/s/3/4/" configure
sed -i '14462 s/1.3/1.4/' configure

cfg --enable-pinentry-tty
mk
mi

}
