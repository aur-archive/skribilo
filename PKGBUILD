# Maintainer: Sindre Devik <sindre.devik@gmail.com>
pkgname=skribilo
pkgver=0.9.2
pkgrel=2
pkgdesc="A complete document programming framework for the Scheme programming language"
url="http://www.nongnu.org/skribilo"
arch=('i686' 'x86_64')
license=('GPL')
depends=('guile-reader' 'lout')
optdepends=( 'texlive-bin: for latex output'
'ploticus: for pie charts'
'guile-lib: to be able to use the RSS-2 reader')
makedepends=('imagemagick')
source=(http://download.savannah.gnu.org/releases/$pkgname/$pkgname-$pkgver.tar.gz)
md5sums=('63e46fc1ec7697acffc93b3ef6e0000f')
build() {
cd $srcdir/$pkgname-$pkgver
./configure --prefix=/usr
make
}
package() {
cd "$srcdir/$pkgname-$pkgver"
make DESTDIR="$pkgdir/" install
}
