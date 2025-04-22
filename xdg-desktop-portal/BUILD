NAME="xdg-desktop-portal"
VERS="1.20.0"
DESC="Desktop integration portals for sandboxed apps"
CATG="lib"
UPST="https://github.com/flatpak/$NAME.git"
DEPS=(
    "fuse3"
    "gdk-pixbuf"
    "json-glib"
    "pipewire"
    "dbus"

    # recommended
    "bubblewrap"

    # one of several, used because this is the lightest
    "r^xdg-desktop-portal-gtk"
)

SOURCE="${UPST%.git}/releases/download/$VERS/$NAME-$VERS.tar.xz"
EXTRA=()

2b() {

with meson ninja

ms -D tests=disabled
nj
ni

rm -rvf "$D"/usr/lib/systemd

}