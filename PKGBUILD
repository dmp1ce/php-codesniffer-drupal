# Maintainer: David Parrish <daveparish@gmail.com>
# Contributer: Joris Steyn <jorissteyn@gmail.com>
pkgname=php-codesniffer-drupal
major=8.x
minor=2.0
candidate=rc1
pkgver=${major}_${minor}_${candidate}
pkgrel=1
pkgdesc='Drupal coding standard for PHP_CodeSniffer'
arch=('any')
url='http://drupal.org/project/coder'
license=('custom')
depends=('php-codesniffer')
provides=('php-codesniffer-drupal')
source=("http://ftp.drupal.org/files/projects/coder-${major}-${minor}-${candidate}.tar.gz")
md5sums=('90729b9135795a1c53312c61f5658dd4')

package() {
  install -D -m644 "${startdir}/LICENSE" "${pkgdir}/usr/share/licenses/${pkgname}/LICENSE" 
  install -d "$pkgdir"/usr/share/pear/PHP/CodeSniffer/Standards/Drupal
  cp -dr --no-preserve=ownership "$srcdir"/coder/coder_sniffer/Drupal/* "$pkgdir"/usr/share/pear/PHP/CodeSniffer/Standards/Drupal/
}
