# mineshafter arch linux package, pkgbuild
# https://github.com/dokuro-chan 
pkgname=minecraft
pkgver=latest
pkgrel=24
pkgdesc="Fuck shitcraft, this is a free version of minecraft, thanks to mineshafter-launcher"
arch=(any)
license=('custom')
url="http://mineshafter.info/"
depends=('java-runtime' 'xorg-xrandr' 'ttf-font' 'libxtst')
noextract=('minecraft.jar')
source=(minecraft http://mineshafter.info/s/Mineshafter-launcher.jar minecraft.desktop minecraft.png minecraft.install LICENSE)
md5sums=('016733d9b0ce647d0f6d5435086f0e8e' 'b3bd65de09f2b92808e74e308f48e1df' 'ecb1bd9b6e6305987b6fb5832ab0b468'
         'dfecf76f9db4497399f4b7c171150c89' '6ff71d817ff71cf5e014b9d798745148' '4f9895e9a0df1cebb21613b448f1ab8c')
install='minecraft.install'

package() {
   cd "$srcdir"
   
   install -D -m755 "${srcdir}/minecraft" "${pkgdir}/usr/bin/minecraft"
   install -D -m644 "${srcdir}/Mineshafter-launcher.jar" "${pkgdir}/usr/share/minecraft/minecraft.jar"

   # install desktop launcher, icon, and license
   install -D -m644 "${srcdir}/minecraft.desktop" "${pkgdir}/usr/share/applications/minecraft.desktop"
   install -D -m644 "${srcdir}/minecraft.png" "${pkgdir}/usr/share/pixmaps/minecraft.png"
   install -D -m644 "${srcdir}/LICENSE"                 "${pkgdir}/usr/share/licenses/minecraft/LICENSE"
}

