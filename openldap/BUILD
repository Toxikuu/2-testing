NAME="openldap"
VERS="2.6.9"
DESC="Lightweight Directory Access Protocol implementation"
CATG="lib"
UPST="https://git.$NAME.org/$NAME/$NAME.git"
DEPS=(
    "cyrus-sasl"
)

SOURCE="https://www.openldap.org/software/download/OpenLDAP/openldap-release/openldap-$VERS.tgz"
EXTRA=(
    "https://www.linuxfromscratch.org/patches/blfs/svn/$NAME-$VERS-consolidated-1.patch"
)

2b() {

tpatch "$SRC/$NAME-$VERS-consolidated-1.patch"
autoreconf -fiv

_cfg_opts=(
    --sysconfdir=/etc
    --enable-dynamic
    --disable-debug
    --disable-slapd
)

cfg ${_cfg_opts[@]}
mk depend
mk
mi

}
