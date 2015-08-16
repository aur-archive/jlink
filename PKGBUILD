# Maintainer: Se7endAY <87635645@qq.com>

pkgname=jlink
pkgver=4.84f
pkgrel=1
pkgdesc="It gives you the J-LINK USB drivers."
arch=('i686' 'x86_64')
url="http://www.segger.com/jlink-software.html"
license=('custom')
install="jlink.install"
source=(http://dl.cici.link/jlink/$pkgname-$pkgver-$CARCH.tar.gz)
if test "$CARCH" == x86_64; then
	md5sums=('f24ad20b6d66b2edb3a077e412ac7d1a')
else
	md5sums=('d429107f87592ccf8e2c932cf75e6711')
fi

package() {
	cd "$srcdir/$pkgname-$pkgver-$CARCH"
	mkdir -p "${pkgdir}/opt/JLink"
	mkdir -p "${pkgdir}/etc/udev/rules.d/"
	cp 99-jlink.rules "${pkgdir}/etc/udev/rules.d/"
	rm 99-jlink.rules
	cp -r * "${pkgdir}/opt/JLink"
}
