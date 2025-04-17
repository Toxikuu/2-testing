NAME="hyperfine"
VERS="3cedcc38d0c430cbf38b4364b441c43a938d2bf3"
DESC="Benchmarking tool"
CATG="cli utils"
UPST="https://github.com/sharkdp/hyperfine.git"
DEPS=(
    "rust"
)

SOURCE="${UPST%.git}/archive/$VERS.tar.gz"
EXTRA=()

2b() {

with rust
cbr

install -vDm755 "target/release/$NAME" -t "$D/usr/bin"

install -vDm644 "target/release/build/$NAME-"*"/out/$NAME.bash" "$D/usr/share/bash-completion/completions/$NAME"
install -vDm644 "target/release/build/$NAME-"*"/out/$NAME.fish" "$D/usr/share/fish/vendor_completions.d/$NAME.fish"
install -vDm644 "target/release/build/$NAME-"*"/out/$NAME"      "$D/usr/share/zsh/site-functions/_$NAME"

install -vDm644 "doc/$NAME.1" "$D/usr/share/man/man1/$NAME.1"
install -vDm755 scripts/*.py -t "$D/usr/lib/$NAME/scripts" 

}
