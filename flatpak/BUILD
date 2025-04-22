NAME="flatpak"
VERS="1.16.0"
DESC="Linux application sandboxing and distribution framework"
CATG="bin utils"
UPST="https://github.com/$NAME/$NAME.git"
DEPS=(
    "appstream"
    "dbus"
    "fuse3"
    "glib"
    "gpgme"
    "json-glib"
    "libsoup3"
    "elogind"
    "ostree"
    "p11-kit"
    "pyparsing"
    
    "appstream-glib"
    "bubblewrap"
    "curl"
    "libarchive"
    "libseccomp"
    "libxau"
    "libxml2"
    "xdg-dbus-proxy"
    "xdg-desktop-portal"
)

SOURCE="${UPST%.git}/releases/download/$VERS/$NAME-$VERS.tar.xz"
EXTRA=()

2b() {

with meson ninja

_cfg_opts=(
    -D systemd=disabled
    -D tests=false
)

ms ${_cfg_opts[@]}
nj
ni

}
