# Generated by gem2arch (https://github.com/anatol/gem2arch)
# Maintainer: Anatol Pomozov <anatol.pomozov@gmail.com>

_gemname=mail
pkgname=ruby-$_gemname-2.5
pkgver=2.5.4
pkgrel=1
pkgdesc='Mail provides a nice Ruby DSL for making, sending and reading emails.'
arch=(any)
url='http://github.com/mikel/mail'
license=(MIT)
depends=(ruby ruby-mime-types-1 ruby-treetop-1.4)
options=(!emptydirs)
source=(https://rubygems.org/downloads/$_gemname-$pkgver.gem)
noextract=($_gemname-$pkgver.gem)
sha1sums=('03b1c19074973f8da94a72cb8579c5d54317934e')

package() {
  local _gemdir="$(ruby -e'puts Gem.default_dir')"
  gem install --ignore-dependencies --no-user-install -i "$pkgdir/$_gemdir" -n "$pkgdir/usr/bin" $_gemname-$pkgver.gem
  rm "$pkgdir/$_gemdir/cache/$_gemname-$pkgver.gem"
  install -D -m644 "$pkgdir/$_gemdir/gems/$_gemname-$pkgver/MIT-LICENSE" "$pkgdir/usr/share/licenses/$pkgname/MIT-LICENSE"
}
