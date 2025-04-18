NAME="gnupg"
VERS="2.4.7"
DESC="GNU's implementation of Pretty Good Privacy"
CATG="sec utils"
UPST="https://github.com/gpg/gnupg.git"
VCMD="git ls-remote --tags --refs '$UPST' | sed 's@.*/@@' | grep 'gnupg-[0-9]' | grep -Ev 'rc|base|alpha|beta' | sort -V | tail -n1 | cut -d- -f2"
DEPS=(
    "libassuan"
    "libgcrypt"
    "libksba"
    "npth"
    "openldap"
    "gnutls"
    "pinentry"
)

SOURCE="https://www.gnupg.org/ftp/gcrypt/gnupg/gnupg-$VERS.tar.bz2"
EXTRA=()

2b() {

mkdir -v build
cd       build

_cfg_opts=(
    --localstatedir=/var
    --sysconfdir=/etc
)

CP=.. cfg ${_cfg_opts[@]}
mk
mi

}
