pkgname=ltsa
pkgver=3.0.0
pkgrel=1
pkgdesc="Labelled Transition System Analyser V3.0"
arch=('i686' 'x86_64')
url="http://www.doc.ic.ac.uk/~jnm/book/ltsa/LTSA_applet.html"
license=('unknown')
groups=()
depends=('jre8-openjdk')
makedepends=()
optdepends=()
provides=()
conflicts=()
replaces=()
backup=()
options=()
install=
source=("http://www.doc.ic.ac.uk/~jnm/book/ltsa/ltsa.jar")
noextract=('ltsa.jar')
md5sums=('0f5228d6d94f4c035aa239d0e2e104c3')


_gen_script() {
    local _ltsa_script="$pkgdir/usr/local/bin/ltsa"
    mkdir -p $(dirname $_ltsa_script)
    cat << EOF > $_ltsa_script
#!/bin/sh
exec /usr/bin/java -jar '/usr/share/java/ltsa/ltsa.jar' "$@"
EOF
    chmod 755 $_ltsa_script
}


build() {
    echo pass
}

package() {
    install -D $srcdir/ltsa.jar $pkgdir/usr/share/java/ltsa/ltsa.jar
    _gen_script
}
# vim:syntax=sh
