# Maintainer: Jove Yu <yushijun110[AT]gmail.com>

pkgname=deepin-gsettings
pkgver=git20131206094009~a64de3ac19
pkgrel=1
pkgdesc='deepin gsettings python bindings'
arch=('i686' 'x86_64')
depends=('python2' 'python2-distribute')
url="http://www.linuxdeepin.com/"
license=('GPL-3')
source=("http://packages.linuxdeepin.com/deepin/pool/main/d/deepin-gsettings/deepin-gsettings_0.1+${pkgver}.tar.gz")
md5sums=('b0400cafb677048e4401641c10efdc5d')

build(){
	cd "$srcdir"/${pkgname}-0.1+${pkgver}
	python2 setup.py build
}
package() {
	cd "$srcdir"/${pkgname}-0.1+${pkgver}
	python2 setup.py install --root="$pkgdir/" --optimize=1
	
	#cd ${pkgdir}/usr/lib/python2.7/site-packages/deepin_utils/
    #sed -i 's_#! /usr/bin/env python$_#! /usr/bin/env python2_' *.py   
}


