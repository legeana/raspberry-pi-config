# Maintainer: Lisa White <lisa.rsfp+dev@gmail.com>
pkgname=legeana-raspberry-pi-config
pkgver=0.0.3
pkgrel=1
epoch=
pkgdesc="Raspberry Pi configuration"
arch=('any')
url=""
license=('MIT')
groups=()
depends=(
  'inetutils'
  'man-db'
  'mlocate'
  'wpa_supplicant'
)
makedepends=()
checkdepends=()
optdepends=(
  'argonone: fan control'
  'bindfs: cooperative development'
  'python-gpiozero: gpio library'
  'python-raspberry-gpio: gpio library'
)
provides=()
conflicts=()
replaces=()
backup=(
  'etc/udev/rules.d/gpio.rules'
  'etc/systemd/network/wlan0.network'
  'etc/wpa_supplicant/wpa_supplicant-wlan0.conf'
)
options=()
install=
changelog=
source=(
  gpio.rules
  wlan0.network
  wpa_supplicant-wlan0.conf
)
install=rpi-config.install
noextract=()
sha256sums=('9abcf02cf3bc875d83572b0cb49daa9a9c99fedff510d93ffcc27d5350b0efc7'
            'ac464435e0a978be0b7c5c45cc535d1b3da2d5bffa0cabe5c68b691e3f7a3283'
            '1e3f3187f9128c4a5ef3fd6494a8192497019d77d2bda93156f5785daccb9682')
validpgpkeys=()

package() {
  install -Dm644 "$srcdir/gpio.rules" "$pkgdir/etc/udev/rules.d/gpio.rules"
  install -Dm644 "$srcdir/wlan0.network" "$pkgdir/etc/systemd/network/wlan0.network"
  install -Dm600 "$srcdir/wpa_supplicant-wlan0.conf" "$pkgdir/etc/wpa_supplicant/wpa_supplicant-wlan0.conf"
  ln -sf /usr/share/zoneinfo/Europe/Dublin "$pkgdir/etc/localtime"
}
