# generated by the gambas3 ide
# Maintainer : Luca D'Isanto <lukadisanto@gmail.com>

pkgname=remoteaccess
_realname=remoteaccess
pkgdesc="Programma per la gestione delle connessioni rdp, vnc e teamviewer, sia dirette che tramite tunnel ssh"
pkgver=0.1.4
pkgrel=1
arch=('any')
url="http://sourceforge.net/projects/remoteaccess-qt/"
changelog=ChangeLog
license=('custom')
depends=('gambas3-gb-image>=3.5' 'gambas3-gb-image<=3.99.0' 'gambas3-gb-qt4>=3.5' 'gambas3-gb-qt4<=3.99.0' 'gambas3-gb-form>=3.5' 'gambas3-gb-form<=3.99.0' 'gambas3-gb-desktop>=3.5' 'gambas3-gb-desktop<=3.99.0' 'gambas3-gb-settings>=3.5' 'gambas3-gb-settings<=3.99.0' 'gambas3-gb-qt4-ext>=3.5' 'gambas3-gb-qt4-ext<=3.99.0' 'nmap' 'teamviewer' 'rdesktop' 'freerdp' 'gambas3-ide' 'gambas3-runtime' 'realvnc-viewer')
makedepend=('gambas3-devel')
source=(${_realname}-$pkgver.tar.bz2 license.txt\
        'remoteaccess.desktop' 'remoteaccess.png')
md5sums=('b7d696c0280837bc0d710f3804e76c49'
         '35403466a659acad9657584fb79a6020'
         'a2ab2665048a342599622f7c21ff4c67'
         '66b0447856758f7fe9051321a384da09')

build() {
  cd ${srcdir}/${_realname}

  /usr/bin/gbc3 -e -a -g -p -m -x  && gba3
}

package() {
  cd ${srcdir}/${_realname}

  install -d ${pkgdir}/usr/bin
  install -m755 remoteaccess.gambas ${pkgdir}/usr/bin/remoteaccess
  install -D ../remoteaccess.png \
    ${pkgdir}/usr/share/pixmaps/remoteaccess.png
  install -D ../remoteaccess.desktop \
    ${pkgdir}/usr/share/applications/remoteaccess.desktop
  install -Dm644 ${srcdir}/license.txt ${pkgdir}/usr/share/licenses/remoteaccess/license.txt
}
