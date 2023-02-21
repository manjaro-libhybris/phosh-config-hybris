# Maintainer: Bardia Moshiri <fakeshell@bardia.tech>
# Contributor: Erik Inkinen <erik.inkinen@gmail.com>

pkgname=phosh-config-hybris
provides=('phosh-config-hybris')
pkgver=0.2
pkgrel=1
pkgdesc="Phosh configuration for Halium"
arch=('any')
url="https://github.com/manjaro-libhybris/phosh-config-hybris"
license=('GPL2')
depends=('phoc-hybris' 'phosh-hybris' 'halium-wrappers')
makedepends=('git')
source=('phosh-config-hybris::git+https://github.com/manjaro-libhybris/phosh-config-hybris.git')
sha256sums=('SKIP')

package() {
    cd phosh-config-hybris

    install -d ${pkgdir}/etc/systemd/system/phosh.service.d
    install -m 644 phosh.service.d/20-wlroots-hwc-env.conf ${pkgdir}/etc/systemd/system/phosh.service.d/
    install -m 644 phosh.service.d/30-force-user.conf ${pkgdir}/etc/systemd/system/phosh.service.d/
    install -m 644 phosh.service.d/40-droid-wait.conf ${pkgdir}/etc/systemd/system/phosh.service.d/
}
