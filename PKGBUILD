# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-gallery
pkgver=0.3.1
pkgrel=1
pkgdesc="The Glacier image gallery"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-gallery"
license=('BSD-3-Clause')
depends=('qt5-glacier-app'
	'nemo-qml-plugin-settings' 
	'nemo-qml-plugin-thumbnailer' 
	'libresourceqt' 
	'qtdocgallery')
makedepends=('qt5-tools' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('12af5bebafc2e1cea366f746f6909e91f138a0a28bdca0228bd53ab3b33c0310')

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
