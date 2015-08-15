# Contributor: Jaroslaw Swierczynski <swiergot@aur.archlinux.org>

pkgname=gg2
pkgver=2.3.0
pkgrel=3
pkgdesc="GTK+ Gadu-Gadu client with Tlen.pl and Jabber support"
arch=('i686' 'x86_64')
url="http://sourceforge.net/projects/ggadu/"
license=('GPL')
depends=(loudmouth gtkspell xosd libxss libtlen)
makedepends=(esound)
options=('!libtool')
source=(http://downloads.sourceforge.net/sourceforge/ggadu/$pkgname-$pkgver.tar.gz)
md5sums=('46f93bec0bf3418f0c9122f4b1c1c225')

build() {
  cd $startdir/src/$pkgname-$pkgver
  ./configure --prefix=/usr --without-arts
  make || return 1
  make DESTDIR=$startdir/pkg install
  install -D -m 644 $pkgname.desktop $startdir/pkg/usr/share/applications/$pkgname.desktop
}
