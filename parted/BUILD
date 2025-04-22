NAME="parted"
VERS="3.6"
DESC="Disk patitioning tool"
CATG="utils cli"
UPST="https://git.savannah.gnu.org/git/parted.git"
DEPS=(
    # "o^lvm"
    "o^dosfstools"
)

SOURCE="https://ftp.gnu.org/gnu/parted/parted-$VERS.tar.xz"
EXTRA=()

2b() {

cfg --disable-device-mapper # requires lvm
mk
mi

}
