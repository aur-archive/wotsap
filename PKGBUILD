# This is an example PKGBUILD file. Use this as a start to creating your own,
# and remove these comments. For more information, see 'man PKGBUILD'.
# NOTE: Please fill out the license field for your package! If it is unknown,
# then please put 'unknown'.

# Maintainer: Your Name <youremail@domain.com>
pkgname=wotsap
pkgver=0.6
pkgrel=2
pkgdesc="A tool to find paths in the OpenPGP Web of Trust"
arch=('any')
url="http://www.lysator.liu.se/~jc/wotsap/"
license=('GPL')
depends=('python2' 'python-imaging')
changelog=
source=(http://www.lysator.liu.se/~jc/wotsap/download/$pkgname-$pkgver.tgz)
md5sums=('347755ecab208977e880cfc3182ead03')

build() {
  cd "$srcdir/$pkgname-$pkgver"
  sed -i "s/python$/python2/" wotsap
  sed -i "s/python$/python2/" pks2wot
}

package() {
  cd "$srcdir/$pkgname-$pkgver"
  install -D wotsap "$pkgdir/usr/bin/wotsap"
  install -D pks2wot "$pkgdir/usr/bin/pks2wot"
  install -D wotfileformat.txt "$pkgdir/usr/share/doc/wotsap/wotfileformat.txt"
}

# vim:set ts=2 sw=2 et:
