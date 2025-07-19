# Original Author: ushiboy (https://github.com/ushiboy)
# Maintainer: Aditya Singh (https://github.com/s-adi-dev)

pkgname=python-nmcli
pkgver=1.5.0
pkgrel=1
pkgdesc="Python wrapper around NetworkManager's nmcli command (by ushiboy)"
arch=('any')
url="https://github.com/ushiboy/nmcli"
license=('MIT')
depends=('python')
makedepends=('git' 'python-setuptools' 'python-build' 'python-wheel' 'python-installer')
source=("nmcli-src::git+https://github.com/ushiboy/nmcli.git")
sha256sums=('SKIP')

build() {
    cd "$srcdir/nmcli-src"
    python -m build --wheel --no-isolation
}

package() {
    cd "$srcdir/nmcli-src"
    python -m installer --destdir="$pkgdir" dist/*.whl
}
