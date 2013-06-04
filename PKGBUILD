# Maintainer: aesiris

_pkgname='pacman-to-cache'
pkgname='pacman-to-cache'
pkgver=0.2.1
pkgrel=1
pkgdesc='Service to automatically download updates into pacman cache'
arch=('any')
license=('GPL')
depends=('')
makedepends=('git')
source=("git://github.com/aesiris/${_pkgname}#tag=${pkgver}")
sha256sums=('SKIP')

package() {
	cd "$srcdir/${_pkgname}"
	install -Dm755 "$pkgname" "$pkgdir/usr/bin/$pkgname"
	install -Dm644 "$pkgname.service" "$pkgdir/usr/lib/systemd/system/$pkgname.service"
	install -Dm644 "$pkgname.timer" "$pkgdir/usr/lib/systemd/system/$pkgname.timer"

	#gzip -9 man.manpage
	#install -Dm 0644 man.manpage.gz "$pkgdir/usr/share/man/man1/$pkgname.1.gz"
}
