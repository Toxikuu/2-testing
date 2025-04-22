NAME="xdg-desktop-portal-gtk"
VERS="1.15.3"
DESC="GTK-based xdg-desktop-portal backend"
CATG="lib"
UPST="https://github.com/flatpak/$NAME.git"
DEPS=(
    "gtk3"
    "xdg-desktop-portal"
)

SOURCE="${UPST%.git}/releases/download/$VERS/$NAME-$VERS.tar.xz"
EXTRA=()

2b() {

with meson ninja

ms
nj
ni

rm -rvf /usr/lib/systemd

}
