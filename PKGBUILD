pkgname=gource
pkgver=0.43
pkgrel=1
pkgdesc="software version control visualization"
license=(GPL3)
arch=(x86_64)
url=http://code.google.com/p/gource/
depends=('ftgl' 'sdl2' 'sdl2_image' 'pcre' 'glew' 'boost-libs')
makedepends=('boost' 'glm' 'mesa')
source=(https://github.com/acaudwell/Gource/releases/download/gource-${pkgver}/gource-${pkgver}.tar.gz)
md5sums=('d2b601782692301f6d8ecc97dc85d3f7')

build() {
	cd "$srcdir/$pkgname-$pkgver"

	./configure --prefix=/usr
	make
}

package() {
	cd "$srcdir/$pkgname-$pkgver"

	make DESTDIR="$pkgdir" install
}
# vim: ts=2:sw=2 et:
