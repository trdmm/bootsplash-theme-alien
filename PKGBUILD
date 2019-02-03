pkgname=('bootsplash-theme-manjaro-maia')
pkgver=1.2
pkgrel=1
url="https://github.com/tchavei/bootsplash-manjaro-maia"
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
            '92e7ef05c0bf03f53e5ac081631c3a2852af9342ca84c2347f88113c02412408'
            'cb12145581e1d82db89cde1f79429933fc682baa2b34c26b7f1c9e670ceac588'
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
