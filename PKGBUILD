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
validpgpkeys=('E0A3EB202F8E57528E13E72FD7574483BB57B18D'  # Jonathan Esk-Riddell <jr@jriddell.org>
              '0AAC775BB6437A8D9AF7A3ACFE0784117FBCE11D'  # Bhushan Shah <bshah@kde.org>
              'D07BD8662C56CB291B316EB2F5675605C74E02CF'  # David Edmundson <davidedmundson@kde.org>
              '1FA881591C26B276D7A5518EEAAF29B42A678C20') # Marco Martin <notmart@gmail.com>

build(){
  cmake -B build -S breeze-gtk-flatbuttons
  cmake --build build
}

package() {
  DESTDIR="$pkgdir" cmake --install build
}
