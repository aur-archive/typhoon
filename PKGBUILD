pkgname=typhoon
pkgver=0.8.94
pkgrel=1
pkgdesc="A weather application based on Stormcloud"
arch=('any')
url="https://www.launchpad.net/typhoon"
license=('GPL3')
depends=('dconf' 'python2' 'python2-gobject' 'webkitgtk3')
makedepends=('python2-distutils-extra')
install=typhoon.install
source=("https://launchpad.net/$pkgname/trunk/$pkgver/+download/${pkgname}_$pkgver.tar.gz")
md5sums=('659f85cb08b4c0bdffe943d507c83362')

package() {
  cd $pkgname

  python2 setup.py install --root="$pkgdir/" --optimize=1

  find "$pkgdir/" -type f -not -name typhoon -exec chmod 644 '{}' \;
}
