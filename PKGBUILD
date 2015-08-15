# Maintainer: nosada <nosada271@gmail.com>

pkgname=calligra-l10n-ja
pkgver=2.4.2
pkgrel=1
pkgdesc="Japanese Localization for Calligra"
arch=('any')
url='http://www.calligra-suite.org/'
license=('LGPL')
makedepends=('cmake' 'automoc4' 'kdelibs')
options=('docs')

# Japanese localization isn't supported officially, so this PKGBUILD uses unofficial localization file.
# (http://running-dog.net/2012/06/post_329.html)
#source=("http://download.kde.org/stable/calligra-${pkgver}/${pkgbase}/${pkgbase}-ja-${pkgver}.tar.xz")
source=("http://icmpv6.org/Prog/ja.po/calligra-l10n-ja-2.4.2.tar.bz2")
md5sums=('59a0c21a6e2c3e98584b342e58a50a71')

build() {
    cd ${srcdir}/${pkgname}-${pkgver}
    cmake -DCMAKE_BUILD_TYPE=Release -DCMAKE_INSTALL_PREFIX=/usr
    make
}

package() {
  replaces=('koffice-l10n-ja')
  cd ${srcdir}
  make DESTDIR="${pkgdir}" install
}
