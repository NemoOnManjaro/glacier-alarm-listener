# $Id$

pkgname=glacier-alarm-listener 
pkgver=0.1.1
pkgrel=1
pkgdesc="Nemo alarm events notification popup"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-alarm-listener"
license=('BSD-3-Clause')
depends=('qt5-glacier-app>=0.9'
	'timed'
	'glacier-alarmclock')

makedepends=('cmake' 'qt5-tools')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('13dd8358d58e32a47cebd3ccab9644d43417550c35494f95c72c5fde96dc1787')

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