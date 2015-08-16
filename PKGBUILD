# Maintainer: Dominik Heidler <dheidler@gmail.com>

pkgname=multibit
pkgver=0.5.18
pkgrel=1
pkgdesc="A lightweight Bitcoin desktop client powered by the BitCoinJ library."
arch=(any)
license=('GPL')
url="https://multibit.org/"
depends=('java-runtime')
noextract=("multibit-exe-${pkgver}.jar")
source=("multibit-exe-${pkgver}.jar::https://multibit.org/releases/multibit-$pkgver/multibit-exe.jar"
		multibit multibit.desktop multibit.png)
md5sums=('a9f2276def31a373a4a6383fb347b9ce'
         '87dc04c25002ebcaa5a8e8456cbd821f'
         '30e725c591e2709c9638b42ca763ecf7'
         '41b492c2898448f0199129fcb1178aac')

package() {
	cd "$srcdir"

	install -D -m755 "multibit"         "${pkgdir}/usr/bin/multibit"
	install -D -m644 "multibit-exe-${pkgver}.jar" "${pkgdir}/usr/share/java/multibit/multibit-exe.jar"

	# Desktop launcher with icon
	install -D -m644 "multibit.desktop" "${pkgdir}/usr/share/applications/multibit.desktop"
	install -D -m644 "multibit.png"     "${pkgdir}/usr/share/pixmaps/multibit.png"
}
