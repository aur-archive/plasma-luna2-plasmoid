# Maintainer: t3ddy  <t3ddy1988 "at" gmail {dot} com>
# Contributor: Bram Schoenmakers <me@bramschoenmakers.nl>

pkgname=plasma-luna2-plasmoid
pkgver=1.3.1
pkgrel=1
pkgdesc="A plasma applet that displays the moon phases."
arch=('i686' 'x86_64')
url="http://www.kde-look.org/content/show.php?content=100337"
license=('GPL')
depends=('kdebase-workspace')
makedepends=('gcc' 'cmake' 'automoc4')
install=luna2.install
source=("http://www.kde-look.org/CONTENT/content-files/100337-plasma-applet-luna2-$pkgver.tar.bz2")
md5sums=('196abe701af16b662176ed46e278ebb0')

build() {
  cd "$srcdir/plasma-applet-luna2"

  mkdir build && cd build

  cmake -DCMAKE_INSTALL_PREFIX=`kde4-config --prefix` ..

  make
}

package() {
  cd "$srcdir/plasma-applet-luna2/build"

  make DESTDIR="$pkgdir/" install
}
# vim:syntax=sh
