# Maintainer: Muflone http://www.muflone.com/contacts/english/
# Contributor: jose <jose1711 [at] gmail (dot) com>

pkgname=gwakeonlan
pkgver=0.6.2
pkgrel=1
pkgdesc="GTK+ utility to awake machines using the Wake on LAN."
url="http://www.muflone.com/gwakeonlan"
arch=('any')
license=('GPL2')
depends=('gtk3' 'gobject-introspection' 'python2-xdg' 'python2-gobject' 'gtk-update-icon-cache')
source=("${pkgname}-${pkgver}.tar.gz"::"https://github.com/muflone/${pkgname}/archive/${pkgver}.tar.gz")
md5sums=('ccdc29789e9a9233631d4e2d403b5797')
sha1sums=('7f4c7177df7f870149006f46d430fe7bb881292a')
sha256sums=('fa6a88351f5a437ca2171c012352f01a3cab147a09ac6c6b3278980f14eeb862')
install="${pkgname}.install"

build() {
  cd "${pkgname}-${pkgver}"
  python2 setup.py build
}

package() {
  cd "${pkgname}-${pkgver}"
  python2 setup.py install --optimize=1 --root "${pkgdir}"
}

