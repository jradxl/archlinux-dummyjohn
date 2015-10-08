# Maintainer:  John Radley <jradxl [at] gmail [dot] com>
# An absolutely useless package, DummyJohn, to test the Build, Install and Service features of Arch/Manjaro Linux

pkgname=dummyjohn
pkgver=0.1.3
pkgrel=3
pkgdesc="A dummy package"
arch=('any')
license=('Apache')
url="http://www.jsrsoft.co.uk"
depends=('bash' 'sh')
#optdepends=('')
#conflicts=('' '' '' '')
#replaces=()
#backup=()
install=$pkgname.install

source=(
    "https://github.com/jradxl/dummyjohn/releases/download/v${pkgver}/${pkgname}-${pkgver}.tar.gz"
    'dummyjohn.service'
)

#noextract=("")

# If "ERROR: Integrity checks are missing", then use updpkgsums (previously makepkg -g >> PKGBUILD)
# and the md5 line will be replaced here.
# Each file in source has a md5 value between '' separated by space.
md5sums=('acb6e9626326411c0e2d799492631814'
         '9f9db547f8d05f3502e610c9fbba4f77')

build()
{
echo build
	pwd
    cd "${srcdir}"/${pkgname}-${pkgver}
    #patch -Np1 -i ../some.patch
}

xpackage()
{
echo package1
cd ${pkgname}-${pkgver}
pwd
install -dm700 "${pkgdir}"/opt/dummyjohn/databases
install -dm755 "${pkgdir}"/opt/dummyjohn/bin
cp -r bin/* "${pkgdir}"/opt/dummyjohn/bin/
cp -r databases/* "${pkgdir}"/opt/dummyjohn/databases/
echo package2
}

package()
{
  cd ${pkgname}-${pkgver}

  install -dm755 "${pkgdir}"/opt/dummyjohn
  install -dm705 "${pkgdir}"/opt/dummyjohn/benchmark
  install -dm755 "${pkgdir}"/opt/dummyjohn/bin
  install -dm705 "${pkgdir}"/opt/dummyjohn/config
  install -dm705 "${pkgdir}"/opt/dummyjohn/databases
  install -dm755 "${pkgdir}"/opt/dummyjohn/lib
  install -dm755 "${pkgdir}"/opt/dummyjohn/log
  install -dm755 "${pkgdir}"/opt/dummyjohn/plugins
  install -dm705 "${pkgdir}"/opt/dummyjohn/www

  # Recursively copy files
  cp -r . "${pkgdir}"/opt/dummyjohn

  install -d "${pkgdir}"/usr/bin
  install -d "${pkgdir}"/var/log/dummyjohn
  install -d "${pkgdir}"/usr/lib/systemd/system

  # Create a file, could be a link
  touch "${pkgdir}"/usr/bin/dummy.txt
  touch "${pkgdir}"/var/log/dummyjohn/dummy.txt

  # Example of patching a text file
  sed -i 's|\.\./log|/opt/dummyjohn/log|' config/dummyjohn-server-log.properties
  sed -i 's|YOUR_DUMMYJOHN_INSTALLATION_PATH|/opt/dummyjohn|' bin/dummyjohn.sh
  sed -i 's|USER_YOU_WANT_DUMMYJOHN_RUN_WITH|dummyjohn|' bin/dummyjohn.sh

  # Alternative to recursive copying
  install -m755 bin/console.sh "${pkgdir}"/opt/dummyjohn/bin/
  install -m705 config/* "${pkgdir}"/opt/dummyjohn/config/
  install -m705 bin/shutdown.sh bin/server.sh bin/dummyjohn.sh "${pkgdir}"/opt/dummyjohn/bin/
  install -m644 "${srcdir}"/dummyjohn.service "${pkgdir}"/usr/lib/systemd/system/

  #install -m644 "${srcdir}"/dummyjohn.zip "${pkgdir}"/opt/dummyjohn/plugins
  #install -m755 lib/* "${pkgdir}"/opt/dummyjohn/lib/
  #install -m705 benchmark/* "${pkgdir}"/opt/dummyjohn/benchmark/
  }

