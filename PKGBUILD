# Maintainer: Jilen <jilen.zhang@gmail.com>
# Upstream URL: https://github.com/atom/atom
#

pkgname=keeweb
pkgver=0.4.6
pkgrel=1
pkgdesc='Keepass web app'
arch=('x86_64')
url='https://github.com/antelle/keeweb'
license=('MIT')
source=("https://github.com/antelle/keeweb/releases/download/v$pkgver/KeeWeb.linux.x64.zip" keeweb.desktop)
sha256sums=("eefad46b82f238b8d7fd936a5af9f561003fefba7108307206bdc8b51f3fa8b6" "1e67ee7d0758110e1935521080266396465a592a5abe8be521736e5e9cf61f75")



package() {
  install -Dm644 keeweb.desktop "$pkgdir"/usr/share/applications/keeweb.desktop
  cp -dr --no-preserve=ownership "$srcdir" "$pkgdir"/usr/share/keeweb
  mkdir -p "$pkgdir"/usr/bin
  ln -s  "$pkgdir"/usr/share/keeweb/KeeWeb "$pkgdir"/usr/bin/KeeWeb
}
