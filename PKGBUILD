# Maintainer: Russi <ixaxaar@mailbox.org> <aur@ixaxaar.in>

pkgname=perftest
pkgver=24.04.0.0.41
pkgrel=1
pkgdesc="OpenFabrics Alliance InfiniBand verbs performance testing and benchmarking tools"
arch=('x86_64')
url="https://github.com/linux-rdma/perftest"
license=('GPL2' 'custom:OpenIB.org BSD')
depends=('bash' 'rdma-core')
makedepends=('git' 'autoconf' 'automake' 'libtool')
source=("git+https://github.com/linux-rdma/perftest.git#tag=${pkgver//_/-}")
sha256sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  git describe --tags | sed 's/^v//;s/-/./g;s/-/./'
}

build() {
  cd "$srcdir/$pkgname"
  ./autogen.sh
  ./configure --prefix=/usr
  make
}

package() {
  cd "$srcdir/$pkgname"
  make DESTDIR="$pkgdir" install
  install -Dm644 COPYING "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}
