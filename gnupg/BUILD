NAME="gnupg"
VERS="2.4.7"
DESC="GNU's implementation of Pretty Good Privacy"
CATG="sec utils"
UPST="https://github.com/gpg/gnupg.git"
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
