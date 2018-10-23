# Maintainer: Kewl <xrjy@nygb.rh.bet(rot13)>
# Contributor: Karol "Kenji Takahashi" Woźniak <kenji.sx>

pkgname=copyq
pkgver=3.6.1
pkgrel=1
pkgdesc="Clipboard manager with searchable and editable history"
url="https://github.com/hluk/copyq"
depends=('libxtst' 'qt5-script' 'qt5-svg' 'qt5-x11extras' 'hicolor-icon-theme')
optdepends=('copyq-plugin-itemweb')
makedepends=('cmake' 'qt5-tools')
license=('GPL3')
arch=('x86_64')
source=("${pkgname}-${pkgver}.tar.gz::${url}/archive/v${pkgver}.tar.gz")
sha256sums=('79bb76c0afcfd769932a9d3b6cfa985dadc1b71443be2277ef0367fa6a4a658f')

build() {
    cd "CopyQ-${pkgver}"
    cmake -DCMAKE_BUILD_TYPE=Release -DWITH_WEBKIT=0 -DCMAKE_INSTALL_PREFIX=/usr -DWITH_QT5=TRUE .
    make
}

package() {
    cd "CopyQ-${pkgver}"
    make DESTDIR="${pkgdir}" install
}
