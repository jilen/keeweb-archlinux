# Maintainer: Jilen <jilen.zhang@gmail.com>
# Upstream URL: https://github.com/atom/atom
#

pkgname=keeweb
pkgver=1.0.4
pkgrel=1
pkgdesc='Keepass web app'
arch=('x86_64')
url='https://github.com/antelle/keeweb'
license=('MIT')
source=("https://github.com/antelle/keeweb/releases/download/v$pkgver/KeeWeb.linux.x64.zip" keeweb.desktop)
sha256sums=("b0801dd708e3d4e6afe666e2bf0bdb5dde5af88ec45b18ad132cc97dd81f2cea" "1e67ee7d0758110e1935521080266396465a592a5abe8be521736e5e9cf61f75")



package() {
  install -Dm644 keeweb.desktop "$pkgdir"/usr/share/applications/keeweb.desktop
  cp -dr --no-preserve=ownership "$srcdir" "$pkgdir"/usr/share/keeweb
  mkdir -p "$pkgdir"/usr/bin
  ln -s  "$pkgdir"/usr/share/keeweb/KeeWeb "$pkgdir"/usr/bin/KeeWeb
}
