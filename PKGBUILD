pkgname=('bootsplash-theme-manjaro-maia')
pkgver=1.2
pkgrel=1
url="https://lists.freedesktop.org/archives/dri-devel/2017-December/160242.html"
arch=('x86_64')
license=('GPL')

depends=()
builddepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-manjaro-maia.sh'
	'bootsplash-manjaro-maia.initcpio_install'
	'spinner.gif'
	'logo.png')

sha256sums=('51559d3ccfb448b03fa6439faf5869dbd0c2fbda1b5d5bf5d4ba70e60937472a'
            'd1607e5a8a4cd478d6139d6dc9b7d0adadf18cd74c6da878a6d1bf04efa5133b'
            'f6568b09ac446239aefa9e8e60d7ed9fdecd83609467d4100688e6f26e51d37c'
            'd133d311d59e2f7bb108a70fc94da8c8514fe749f9d4d1bb231936938f1e8453'
            '1bcf2ac5c091cf8f8c4820bb9bbe0ac53edf128f39926fe5e5bf57b0ad05a128')

build() {
  cd "$srcdir"
  sh ./bootsplash-manjaro-maia.sh
}

package_bootsplash-theme-manjaro-maia() {
  pkgdesc="Bootsplash Theme 'Manjaro Maia'"
  cd "$srcdir"

  install -Dm644 "$srcdir/bootsplash-manjaro-maia" "$pkgdir/usr/lib/firmware/bootsplash-themes/manjaro-maia/bootsplash"
  install -Dm644 "$srcdir/bootsplash-manjaro-maia.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-manjaro-maia"
}
