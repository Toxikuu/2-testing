NAME="bat"
VERS="98c9a5d948d6d26af52c51b6fb845ee5f5e6f7ea"
DESC="Cat clone with syntax highlighting and git integration"
CATG="utils tui"
UPST="https://github.com/sharkdp/bat.git"
DEPS=(
    "rust"
)

SOURCE="${UPST%.git}/archive/$VERS.tar.gz"
EXTRA=()

2b() {

with rust

cbr

install -vDm755 "target/release/bat" -t "$D/usr/bin/"

# Find and package the man page
find . -name bat.1 -type f -exec install -vDm644 {} \
    "$D/usr/share/man/man1/bat.1" \;
# Find and package the bash completion file
find . -name bat.bash -type f -exec install -vDm644 {} \
    "$D/usr/share/bash-completion/completions/bat" \;
# Find and package the zsh completion file
find . -name bat.zsh -type f -exec install -vDm644 {} \
    "$D/usr/share/zsh/site-functions/_bat" \;
# Find and package the fish completion file
find . -name bat.fish -type f -exec install -vDm644 {} \
    "$D/usr/share/fish/vendor_completions.d/bat.fish" \;

}
