# Maintainer: Balló György <ballogyor+arch at gmail dot com>
# Contributor: Jelle van der Waa <jelle at vdwaa dot nl>
# Contributor: Borromini <gotleenucks at g-male dot com>

pkgname=evolution-rss
pkgver=0.3.93
pkgrel=1
pkgdesc="Plugin for Evolution Mail that enables reading of RSS/RDF/ATOM feeds"
arch=('i686' 'x86_64')
url="http://gnome.eu.org/index.php/Evolution_RSS_Reader_Plugin"
license=('GPL')
depends=('evolution')
makedepends=('intltool' 'gconf')
install=$pkgname.install
options=('!libtool')
source=(http://gnome.eu.org/$pkgname-$pkgver.tar.xz)
md5sums=('05f4845482c2d74a5df06da03bdafff8')

build() {
  cd "$srcdir/$pkgname-$pkgver"

  ./configure --prefix=/usr --sysconfdir=/etc --localstatedir=/var \
              --disable-static --disable-schemas-compile
  make
}

package() {
  cd "$srcdir/$pkgname-$pkgver"

  make DESTDIR="$pkgdir/" install
}
