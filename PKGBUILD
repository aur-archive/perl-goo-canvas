# Maintainer: Shanto <shanto@hotmail.com>
# Contributor: TDY <tdy@gmx.com>

pkgname=perl-goo-canvas
pkgver=0.06
pkgrel=3
pkgdesc="Perl bindings for GooCanvas"
arch=(i686 x86_64)
url="http://search.cpan.org/dist/Goo-Canvas/"
license=('GPL' 'PerlArtistic')
depends=('cairo-perl' 'glib-perl' 'goocanvas1' 'gtk2-perl')
makedepends=('perl-extutils-depends' 'perl-extutils-pkgconfig')
options=('!emptydirs')
source=(http://search.cpan.org/CPAN/authors/id/Y/YE/YEWENBIN/Goo-Canvas-$pkgver.tar.gz)
md5sums=('7dfe0be8c17bfd641d18384d4fd8fb23')

build() {
  cd "$srcdir/Goo-Canvas-$pkgver"
  PERL_MM_USE_DEFAULT=1 perl Makefile.PL INSTALLDIRS=vendor
  make
}

package() {
  cd "$srcdir/Goo-Canvas-$pkgver"
  make install DESTDIR="$pkgdir"
}
