# Maintainer: tramm <tramm@topplayer.win>

pkgname=('bootsplash-theme-alien')
pkgver=0.1
pkgrel=1
url="https://github.com/trdmm/bootsplash-theme-alien"
arch=('x86_64')
pkgdesc="Simple Manjaro Bootsplash with Alien"
license=('GPL')
depends=()
builddepends=('imagemagick')
options=('!libtool' '!emptydirs')

source=('bootsplash-packer'
	'bootsplash-alien.sh'
	'bootsplash-alien.initcpio_install'
	'spinner.gif'
	'logo.png')

sha256sums=('51559d3ccfb448b03fa6439faf5869dbd0c2fbda1b5d5bf5d4ba70e60937472a'
            '521eccd161147e071bcb5f89639c2bdb62d14a3eba87bdaf6bb644dfb94f542d'
            'e39c06ac03c2e5c9fef28f48f3ee028217e96f377c0249d359bed528b77399b8'
            'd133d311d59e2f7bb108a70fc94da8c8514fe749f9d4d1bb231936938f1e8453'
            '61324b8b9a164b4c581ede31c7b006ab75296decd2c609d447ba42d15a00eddc')

build() {
  cd "$srcdir"
  sh ./bootsplash-alien.sh
}

package_bootsplash-theme-alien() {
  pkgdesc="Bootsplash Theme 'Alien'"
  cd "$srcdir"

  install -Dm644 "$srcdir/bootsplash-alien" "$pkgdir/usr/lib/firmware/bootsplash-themes/alien/bootsplash"
  install -Dm644 "$srcdir/bootsplash-alien.initcpio_install" "$pkgdir/usr/lib/initcpio/install/bootsplash-alien"
}
