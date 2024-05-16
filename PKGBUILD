# $Id$

pkgname=glacier-alarm-listener 
pkgver=0.2
pkgrel=1
pkgdesc="Nemo alarm events notification popup"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-alarm-listener"
license=('BSD-3-Clause')
depends=('qt6-glacier-app' 'timed' 'glacier-alarmclock>=0.2')
makedepends=('cmake' 'qt6-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('0825323764939cc809e41868f3c5a5cadf85bdabadcf6b10462f597c0891375e')

build() {
    cd $pkgname-$pkgver
    cmake \
        -DCMAKE_INSTALL_PREFIX:PATH='/usr'
    make all
}

package() {
    cd $pkgname-$pkgver
    make DESTDIR="$pkgdir" install
}