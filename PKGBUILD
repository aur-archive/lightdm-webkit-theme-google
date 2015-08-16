# Maintainer: Max Glenister <moglenstar@gmail.com>
pkgname=lightdm-webkit-theme-google
pkgver=r11.d83ee55
pkgrel=1
pkgdesc='A ChromeOS-style theme for lightdm-webkit-greeter'
arch=('any')
url='https://github.com/omgmog/lightdm-webkit-google'
license=('custom:WTFPL')
depends=('lightdm-webkit-greeter')
makedepends=('git')
source=("$pkgname::git+https://github.com/omgmog/lightdm-webkit-google.git")
md5sums=('SKIP')

pkgver() {
  cd "$srcdir/$pkgname"
  printf 'r%s.%s' "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$srcdir/$pkgname"
  outdir=$pkgdir/usr/share/lightdm-webkit/themes/lightdm-webkit-google
  mkdir -p "$outdir"
  cp -r assets index.html index.theme "$outdir"
}
