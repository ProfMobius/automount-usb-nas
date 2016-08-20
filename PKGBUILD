pkgname=automount-usb
pkgver=1.0.0
pkgrel=1
pkgdesc="Automount USB on boot and try to start mariadb after each mount"
arch=('any')
url="http://mobiusstrip.eu"
license=(GPL)
depends=()
source=(
	"98-usb-mount.rules"
	"99-mariadb-delay.rules"
	"usb-mount.sh"
	"usb-mount@.service"
)
sha256sums=(
	'e53b62639240cb0f8221963b31ab4a4ba2037cd3c476b7a3a2f73b24fe1b6b7e'
	'1033c426caa9691a9a08a7076aaf29491760d2d5b9063f2d8f32ea730f8bde50'
	'0759acba8557f04c7525570705c07f78c4970bbf6e05a6aa3e037e338aa9ffd5'
	'2a6b16e27c469ccb29ce8f1ea484b59910149ab4228ed75354fa05028c767c04'
	)

build() {
	echo ""
}

package() {
  install -Dm0644 $srcdir/usb-mount.sh $pkgdir/usr/local/bin/usb-mount.sh
  install -Dm0644 $srcdir/usb-mount\@.service $pkgdir/usr/lib/systemd/system/usb-mount\@.service
  install -Dm0644 $srcdir/98-usb-mount.rules $pkgdir/etc/udev/rules.d/98-usb-mount.rules
  install -Dm0644 $srcdir/99-mariadb-delay.rules $pkgdir/etc/udev/rules.d/99-mariadb-delay.rules

}

