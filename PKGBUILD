# Maintainer: Kwimy
pkgname=kwimy-splash
pkgver=0.0.1
pkgrel=1
pkgdesc="Kwimy Plymouth splash theme"
arch=('any')
url="https://github.com/KwimyOS"
license=('custom')
source=()
sha256sums=()

prepare() {
  rm -rf "$srcdir/kwimy-splash"
  mkdir -p "$srcdir/kwimy-splash"

  # Copy all files from startdir to srcdir/kwimy-splash, including hidden ones,
  # but excluding pkg, src, and the PKGBUILD itself to avoid recursion.
  find "$startdir" -maxdepth 1 \
    -not -path "$startdir" \
    -not -name "src" \
    -not -name "pkg" \
    -not -name "PKGBUILD" \
    -not -name "*.pkg.tar.*" \
    -not -name ".SRCINFO" \
    -exec cp -r {} "$srcdir/kwimy-splash/" \;
}

package() {
  install -d "$pkgdir/usr/share/plymouth/themes/kwimy-splash"
  cp -a "$srcdir/kwimy-splash/." \
    "$pkgdir/usr/share/plymouth/themes/kwimy-splash/"
}
