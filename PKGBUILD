# Maintainer: Sven-Hendrik Haase <sh@lutzhaase.com>

pkgname=sdl2_ttf
pkgver=2.0.13
pkgrel=1
pkgdesc="A library that allows you to use TrueType fonts in your SDL applications (Version 2)"
arch=('i686' 'x86_64')
url="http://www.libsdl.org/projects/SDL_ttf"
license=('MIT')
depends=('sdl2' 'freetype2')
makedepends=('cmake')
source=("$url/release/SDL2_ttf-${pkgver}.tar.gz")
md5sums=('f57b13b2e51f1f8772cc1a79cdcdb14e')

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
