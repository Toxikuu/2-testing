NAME="libgcrypt"
VERS="1.11.0"
DESC="General purpose crypto library used by GnuPG"
CATG="lib sec"
UPST="https://github.com/gpg/libgcrypt.git"
VCMD="git ls-remote --tags --refs '$UPST' | sed 's@.*/@@' | grep '$NAME-' | grep -Ev 'base|beta|rc' | sort -V | tail -n1"
DEPS=(
    "libgpg-error"
)

SOURCE="https://www.gnupg.org/ftp/gcrypt/$NAME/$NAME-$VERS.tar.bz2"
EXTRA=()

2b() {

cfg
mk
mi

}
