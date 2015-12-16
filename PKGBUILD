# Maintainer: Jilen <jilen.zhang@gmail.com>
# Upstream URL: https://github.com/atom/atom
#

pkgname=keeweb
pkgver=0.5.1
pkgrel=1
pkgdesc='Keepass web app'
arch=('x86_64')
url='https://github.com/antelle/keeweb'
license=('MIT')
source=("https://github.com/antelle/keeweb/releases/download/v$pkgver/KeeWeb.linux.x64.zip" keeweb.desktop)
sha256sums=("4bed2321519ffbf9a35d1abe98cc7e3b4ea4c477fbb8a6ae2f2d4d8ccc040d46" "1e67ee7d0758110e1935521080266396465a592a5abe8be521736e5e9cf61f75")



package() {
  install -Dm644 keeweb.desktop "$pkgdir"/usr/share/applications/keeweb.desktop
  cp -dr --no-preserve=ownership "$srcdir" "$pkgdir"/usr/share/keeweb
  mkdir -p "$pkgdir"/usr/bin
  ln -s  "$pkgdir"/usr/share/keeweb/KeeWeb "$pkgdir"/usr/bin/KeeWeb
}
