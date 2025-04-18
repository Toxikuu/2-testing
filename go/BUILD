NAME="go"
VERS="1.24.2"
DESC="The Go programming langueage"
CATG="lang dev"
UPST="https://github.com/golang/go.git"
VCMD="git ls-remote --tags --refs '$UPST' | sed 's@.*/@@' | grep '^go' | grep -Ev 'rc|alpha|beta' | sort -V | tail -n1"
DEPS=()

SOURCE="https://go.dev/dl/go$VERS.linux-amd64.tar.gz"
EXTRA=()
EXTRACT=1

2preinstall() {

    # Upstream recommends removing any previous Go install
    # https://go.dev/doc/install
    rm -rf "/opt/go"

}

2build() {

mkdir -pv "$D/opt"
tar xf "$SRC/go=$VERS.tar.gz" -C "$D/opt"

# cleanup
rm -rvf "$D/opt/"{test,doc,api}
rm -vf "$D/opt/"{VERSION,PATENTS,SECURITY.md,codereview.cfg}

}
