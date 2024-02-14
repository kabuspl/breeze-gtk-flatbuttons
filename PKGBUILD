pkgname=breeze-gtk-flatbuttons-git
pkgver=5.27.10
_dirver=$(echo $pkgver | cut -d. -f1-3)
pkgrel=1
pkgdesc='Breeze widget theme for GTK 2 and 3 with flat buttons matching QT theme'
arch=(any)
url='https://kde.org/plasma-desktop/'
license=(LGPL)
depends=()
makedepends=(extra-cmake-modules sassc python-cairo breeze)
conflicts=('breeze-gtk')
provides=('breeze-gtk')
source=(git+https://github.com/kabuspl/breeze-gtk-flatbuttons.git#branch=Plasma/5.27)
sha256sums=('SKIP')

build(){
  cmake -B build -S breeze-gtk-flatbuttons
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
