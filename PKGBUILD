# Maintainer: Mike Mogenson <michael.mogenson@gmail.com>

_pkgname=pureline
pkgname=bash-pureline-git
pkgver=r119.19ef111
pkgrel=1
pkgdesc="A simple but powerful Powerline style prompt for the Bash shell written in Bash script"
url="https://github.com/chris-marsh/pureline"
arch=('any')
license=('MIT')
depends=('sh')
provides=('bash-pureline')
install=bash-pureline-git.install
makedepends=('git')
source=(git://github.com/chris-marsh/pureline)
md5sums=('SKIP')

pkgver() {
  cd "$_pkgname"
  printf "r%s.%s" "$(git rev-list --count HEAD)" "$(git rev-parse --short HEAD)"
}

package() {
  cd "$_pkgname"
  install -D -m644 -t "$pkgdir/usr/share/$_pkgname/"            pureline
  install -D -m644 -t "$pkgdir/usr/share/$_pkgname/configs/"    configs/*.conf
  install -D -m644 -t "$pkgdir/usr/share/licenses/$_pkgname/"   LICENSE.md
}
