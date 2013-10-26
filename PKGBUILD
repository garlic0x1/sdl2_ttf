# Maintainer: Sven-Hendrik Haase <sh@lutzhaase.com>

pkgname=sdl2_ttf
pkgver=2.0.12
pkgrel=2
pkgdesc="A library that allows you to use TrueType fonts in your SDL applications (Version 2)"
arch=('i686' 'x86_64')
url="http://www.libsdl.org/projects/SDL_ttf"
license=('MIT')
depends=('sdl2' 'freetype2')
makedepends=('cmake')
options=(!libtool)
source=("$url/release/SDL2_ttf-${pkgver}.tar.gz")
md5sums=('79787216b56cb4707f39d538f2225e00')

build() {
  cd "${srcdir}/SDL2_ttf-${pkgver}/"

  ./configure --disable-static --prefix=/usr
  make
}

package() {
  cd "${srcdir}/SDL2_ttf-${pkgver}/"

  make DESTDIR="${pkgdir}/" install
  install -Dm644 COPYING.txt "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
