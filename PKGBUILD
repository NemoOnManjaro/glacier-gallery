# $Id$
# Contributor: TheKit <nekit1000 at gmail.com>
# Contributor: Bart Ribbers <bribbers@disroot.org>
# Contributor: Alexey Andreyev <aa13q@ya.ru>
# Maintainer: James Kittsmiller (AJSlye) <james@nulogicsystems.com>

pkgname=glacier-gallery
pkgver=0.4
pkgrel=2
pkgdesc="The Glacier image gallery"
arch=('x86_64' 'aarch64')
url="https://github.com/nemomobile-ux/glacier-gallery"
license=('BSD-3-Clause')
depends=('qt6-glacier-app'
	'nemo-qml-plugin-settings'
	'nemo-qml-plugin-thumbnailer'
	'libresourceqt>=1.32.0'
	'qtdocgallery')
makedepends=('qt6-tools' 'clang' 'cmake')
source=("${url}/archive/refs/tags/$pkgver.tar.gz")
sha256sums=('fe3403e0684fa7144df30c856b61e55b90aa38845977ae173c094419eeca24a6')

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
