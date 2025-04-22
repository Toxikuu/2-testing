NAME="xdg-desktop-portal-gtk"
VERS="1.15.3"
DESC="GTK-based xdg-desktop-portal backend"
CATG="lib"
UPST="https://github.com/flatpak/$NAME.git"
VCMD="git ls-remote --tags --refs $UPST | sed 's@.*/@@' | grep -v 'v' | sort -V | tail -n1"
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
