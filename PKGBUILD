pkgname=larch
pkgver=8
pkgrel=4
pkgdesc="a live CD/DVD/USB-stick construction kit"
arch=(any)
url="http://larch.berlios.de/"
license=('custom')
source=(ftp://ftp.berlios.de/pub/$pkgname/$pkgname$pkgver/i686/larch-setup)
md5sums=('e63a0940e93019a106f7cd4946a97c76')
depends=('python2-pyqt' 'python2' 'python2-pexpect' )

package() {
  cd "$srcdir"/

  chmod +x ./larch-setup
  ./larch-setup

	mkdir "$pkgdir"/opt
	mkdir "$pkgdir"/opt/larch
	mkdir "$pkgdir"/opt/liblarch

	cp -r larch0/* "$pkgdir"/opt/larch/
	cp -r liblarch/* "$pkgdir"/opt/liblarch/
}
