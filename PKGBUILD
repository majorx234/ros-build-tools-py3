# Maintainer: Oskar Roesler <oskar@oskar-roesler.de>

pkgdesc='Utilities for building Arch packages for ROS stacks.'
url="https://github.com/ros-melodic-arch/ros-build-tools-py3"

pkgname='ros-build-tools-py3'
pkgver='0.3.1'
arch=('any')
pkgrel=3
license=('BSD')
makedepends=()
optdepends=('python3' 'python-argparse' 'python-yaml' 'python-termcolor' 'python-certifi')
depends=('bash')
provides=('ros-build-tools')
conflicts=('ros-build-tools')

pkg_destination_dir="/usr/share/ros-build-tools"

source=('fix-python-scripts.sh'
        'clear-ros-env.sh'
        'create_pkgbuild.py')

sha256sums=('5528486d640d91136276edda2075aefc06f360e6297e556051bae57b9479aeda'
	    '9626b8e5f3865f5640660f4a7f6a00afc4db8448b95329b4d5a64bd691677a88'
	    '66ed7e8fbbbd9b000960fdd38b949ee796c8ca22c30997156abc4ced5f4e6be7')
build() {
  return 0
}

package() {
  mkdir -p ${pkgdir}${pkg_destination_dir}
  for file in "${source[@]}"; do
    cp $file ${pkgdir}${pkg_destination_dir}/$file
  done
}

