# $Id$

pkgname=glacier-alarm-listener 
pkgver=0.2.1
pkgrel=1
pkgdesc="Nemo alarm events notification popup"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-alarm-listener"
license=('BSD-3-Clause')
depends=('qt6-glacier-app' 'timed' 'glacier-alarmclock>=0.2')
makedepends=('cmake' 'qt6-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('5b5355a51a80ce07de32afbc44d6d9f179cfa2b09b6258c75fffed187f2b678d')

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