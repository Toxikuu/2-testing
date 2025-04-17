NAME="lmdb"
VERS="0.9.31"
DESC="Fast, compact, key-value embedded data store"
CATG="lib db"
UPST="https://github.com/LMDB/lmdb.git"
DEPS=()

SOURCE="${UPST%.git}/archive/LMDB_$VERS.tar.gz"
EXTRA=()

2b() {

cd libraries/liblmdb

mk
sed -i 's| liblmdb.a||' Makefile
mi prefix=/usr

}
