# Maintainer: DrZaius <lou[at]fakeoutdoorsman[dot]com>

pkgname=opusfile
pkgver=0.2
pkgrel=2
pkgdesc="Library for opening, seeking, and decoding .opus files"
arch=('i686' 'x86_64')
url="http://www.opus-codec.org/"
license=('custom')
depends=('libogg' 'openssl' 'opus')
options=('!libtool')
source=("http://downloads.xiph.org/releases/opus/${pkgname}-${pkgver}.tar.gz")
md5sums=('454375f51fb2f84bef9bf2fbf9535bb1')

build() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  ./configure --prefix=/usr
  make
}

package() {
  cd "${srcdir}/${pkgname}-${pkgver}"
  make DESTDIR="${pkgdir}" install
  install -m755 -d "${pkgdir}/usr/share/licenses/opusfile"
  install -m644 COPYING "${pkgdir}/usr/share/licenses/opusfile/"
}
