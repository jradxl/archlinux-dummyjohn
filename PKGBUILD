# Maintainer:  John Radley <jradxl [at] gmail [dot] com>
# An absolutely useless package, DummyJohn, to test the Build, Install and Service features of Arch/Manjaro Linux

pkgname=dummyjohn
pkgver=0.1.1
pkgrel=1
pkgdesc="DummyJohn dummy package"
arch=('any')
license=('Apache')
url="http://www.jsrsoft.co.uk"
depends=('java-runtime-headless')
#optdepends=('')
#conflicts=('' '' '' '')
#replaces=()
#backup=()
install=$pkgname.install
source=
(
  "https://github.com/jradxl/archlinux-dummyjohn/releases/download/v${pkgver}/${pkgname}-${pkgver}.tar.gz"
)

#noextract=("")
#md5sums=('682e1a20b5651898dc4057650cb25367' '25f15357f72faba7ae7bf48c880ca072' '11ca04909f55bcf5ff7a4a739a6b89af' 'bd8a11d5eabc337862ff9276dd31b80a')

build()
{
    cd "${srcdir}"/${pkgname}-${pkgver}
    #patch -Np1 -i ../some.patch
}

package()
{
  cd ${pkgname}-${pkgver}

  install -dm755 "${pkgdir}"/opt/dummyjohn
  install -dm700 "${pkgdir}"/opt/dummyjohn/config
  install -dm700 "${pkgdir}"/opt/dummyjohn/databases
  install -dm755 "${pkgdir}"/opt/dummyjohn/bin
  install -dm700 "${pkgdir}"/opt/dummyjohn/www
  install -dm755 "${pkgdir}"/opt/dummyjohn/lib
  install -dm755 "${pkgdir}"/opt/dummyjohn/plugins

  #install -d "${pkgdir}"/usr/bin
  #install -d "${pkgdir}"/var/log/dummyjohn
  #install -d "${pkgdir}"/usr/lib/systemd/system

  #sed -i 's|\.\./log|/opt/dummyjohn/log|' config/dummyjohn-server-log.properties
  #sed -i 's|YOUR_DUMMYJOHN_INSTALLATION_PATH|/opt/dummyjohn|' bin/dummyjohn.sh
  #sed -i 's|USER_YOU_WANT_DUMMYJOHN_RUN_WITH|dummyjohn|' bin/dummyjohn.sh

  #install -m755 bin/console.sh "${pkgdir}"/opt/dummyjohn/bin/
  #install -m755 lib/* "${pkgdir}"/opt/dummyjohn/lib/
  #install -m700 config/* "${pkgdir}"/opt/dummyjohn/config/
  #install -m700 bin/shutdown.sh bin/server.sh bin/dummyjohn.sh "${pkgdir}"/opt/dummyjohn/bin/
  #cp -r www/* "${pkgdir}"/opt/dummyjohn/www/

  #install -m644 "${srcdir}"/dummyjohn.service "${pkgdir}"/usr/lib/systemd/system/

  #install -m644 "${srcdir}"/dummyjohn.zip "${pkgdir}"/opt/dummyjohn/plugins
}
