# Maintainer: Koragg Knightwolf <31944041+KoraggKnightWolf@users.noreply.github.com>
# Contributor: Dave Brown <d.brown@bigdavedev.com>
# Contributor: theblazehen <com.theblazehen@post - reverse>
pkgname=xinit-xsession
pkgver=2
pkgrel=1
pkgdesc="Allows ~/.xinitrc to be run as a session from your display manager"
url="https://github.com/KoraggKnightWolf/xinit-xsession"
arch=('any')
license=("GPL3")
provides=('xinit-xsession')
depends=('bash')
source=("git+$url.git")
#sha1sums=('0b3ee35032ba0cef758d61154c1bfbb858b8827c'
#          '9665e18bd24aca0afd9d46d3c9200893fd12a391')
md5sums=('SKIP')

prepare() {
    mv $pkgname $pkgname-$pkgver
}


package() {
	cd $pkgname-$pkgver
        install -Dm755 xinitrcsession-helper "${pkgdir}/usr/bin/xinitrcsession-helper"
        install -Dm644 xinitrc.desktop "${pkgdir}/usr/share/xsessions/xinitrc.desktop"
	install -Dm644 LICENSE $pkgdir/usr/share/licenses/$pkgname/LICENSE
	install -Dm644 README.md $pkgdir/usr/share/doc/$pkgname/README.md
        install -Dm644 CHANGELOG.md $pkgdir/usr/share/doc/$pkgname/CHANGELOG.md

}
