# $Id$

pkgname=glacier-alarm-listener 
pkgver=0.1
pkgrel=1
pkgdesc="Nemo alarm events notification popup"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-alarm-listener"
license=('BSD-3-Clause')
depends=('qt5-glacier-app' 'timed' 'glacier-alarmclock')
makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('271185cada6d9733ba90200e684a1c7e8f1432270a4299bc7478785e6328eb5b')

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