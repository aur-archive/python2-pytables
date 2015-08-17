# $Id: PKGBUILD 76100 2012-09-11 10:11:13Z aginiewicz $
# Maintainer: Andrzej Giniewicz <gginiu@gmail.com>
# Contributor: Sebastien Binet <binet@cern.ch>

pkgname=python2-pytables
pkgver=2.4.0
pkgrel=1
arch=("i686" "x86_64")
pkgdesc="PyTables is a package for managing hierarchical datasets and designed to efficiently and easily cope with extremely large amounts of data"
url="http://www.pytables.org"
license=("BSD")
depends=('lzo2' 'hdf5' 'python2-numexpr' 'cython2')
provides=('python-pytables') # temporary due to package rename
source=("http://pypi.python.org/packages/source/t/tables/tables-$pkgver.tar.gz")
md5sums=('527ad046f92c9197ca96626b725f71f8')

build() {
  cd "$srcdir"/tables-${pkgver}
  python2 setup.py build
}

package() {
  cd "$srcdir"/tables-${pkgver}
  python2 setup.py install --prefix=/usr --root="$pkgdir" --optimize=1

  install -Dm644 LICENSE.txt "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
}

