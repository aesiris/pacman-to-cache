# Maintainer: aesiris
pkgname='pacman-to-cache'
pkgver=0.2.4
pkgrel=1
pkgdesc='A service to automatically download updates into pacman cache'
arch=('any')
license=('GPL')
depends=('')
source=("https://github.com/aesiris/${pkgname}/archive/${pkgver}.tar.gz")
sha256sum=('')
#makedepends=('git')
#source=("git://github.com/aesiris/${pkgname}#tag=${pkgver}")
#sha256sums=('SKIP')

package() {
	cd "$srcdir/$pkgname"
	install -Dm755 "$pkgname" "$pkgdir/usr/bin/$pkgname"
	install -Dm644 "$pkgname.service" "$pkgdir/usr/lib/systemd/system/$pkgname.service"
	install -Dm644 "$pkgname.timer" "$pkgdir/usr/lib/systemd/system/$pkgname.timer"
	#gzip -9 man.manpage
	#install -Dm 0644 man.manpage.gz "$pkgdir/usr/share/man/man1/$pkgname.1.gz"
}
