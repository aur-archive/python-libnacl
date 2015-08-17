# $Id$
# Maintiner: Thomas S Hatch <thatch45@gmail.com>

pkgname=('python-libnacl' 'python2-libnacl')
pkgver=0.9.1
pkgrel=1
pkgdesc='A simple ctypes based python binding to libsodium'
arch=('any')
url='http://libnacl.readthedocs.org'
license=('APACHE')
depends=('libsodium')
source=("https://pypi.python.org/packages/source/l/libnacl/libnacl-$pkgver.tar.gz")
md5sums=('625124dd981c81ac1075b161247547e5')

build() {
  cd $srcdir
  cp -r libnacl-$pkgver python2-libnacl-$pkgver
}

package_python-libnacl() {
  depends=('python')
  cd "$srcdir/libnacl-$pkgver"
  python3 setup.py install --root="$pkgdir" -O1
}

package_python2-libnacl() {
  depends=('python2')
  cd "$srcdir/python2-libnacl-$pkgver"
  python2 setup.py install --root="$pkgdir" -O1
}
