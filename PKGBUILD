# Maintainer: slwyts <slwyts@users.noreply.github.com>
pkgname=bakaxl-bin
pkgver=4.0.0+bunny
_rev=a03f125
pkgrel=1
pkgdesc="BakaXL Minecraft Launcher (official pre-built .deb repackaged for Arch)"
arch=('x86_64')
url="https://www.bakaxl.com"
license=('custom')
depends=()
makedepends=('dpkg')
provides=('bakaxl')
conflicts=('bakaxl')

source=(
  "https://github.com/BakaXL-Launcher/BakaXL/releases/download/${pkgver}-${_rev}/bakaxl-${pkgver}-${_rev}-linux-x86_64.deb"
  "LICENSE"
)
sha256sums=(
  '8ed0f18fd1c00e2cf61f822412ef6b83b4b867883860672fee84e0fee1f337af'
  'SKIP'
)

package() {
  dpkg-deb -x "${srcdir}/bakaxl-${pkgver}-${_rev}-linux-x86_64.deb" "${pkgdir}"
  install -Dm644 "${srcdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE"
}
