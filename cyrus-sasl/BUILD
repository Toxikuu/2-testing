NAME="cyrus-sasl"
VERS="2.1.28"
DESC="Simple Authentication and Security Layer implementation"
CATG="lib sec"
UPST="https://github.com/cyrusimap/$NAME.git"
DEPS=(
    "lmdb"
)

SOURCE="${UPST%.git}/releases/download/$NAME-$VERS/$NAME-$VERS.tar.gz"
EXTRA=()

2b() {

# gcc=14 compat
sed '/saslint/a #include <time.h>'       -i lib/saslutil.c
sed '/plugin_common/a #include <time.h>' -i plugins/cram.c

_cfg_opts=(
    --sysconfdir=/etc
    --enable-auth-sasldb
    --with-dblib=lmdb
    --with-dbpath=/var/lib/sasl/sasldb2
    --with-sphinx-build=no
    --with-saslauthd=/var/run/saslauthd
)

cfg ${_cfg_opts[@]}
mk -j1
mi

}
