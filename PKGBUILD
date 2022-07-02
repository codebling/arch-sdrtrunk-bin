# Maintainer: GI_Jack <GI_Jack@hackermail.com>
_pkgver=0.5.0-beta3
_pkgvertag=$(echo ${_pkgver} | sed -E 's/-(alpha|beta)([0-9]+)/-\1.\2/')
_filename=sdr-trunk-linux-${CARCH}-v${_pkgver}
pkgname=sdrtrunk-bin
pkgver=${_pkgver/-/.}
pkgrel=1
pkgdesc="A cross-platform java application for decoding, monitoring, recording and streaming trunked mobile and related radio protocols using SDR"
arch=('i686' 'x86_64')
url="https://github.com/DSheirer/sdrtrunk"
license=('GPLv3')
groups=()
depends=('jre-openjdk' 'java-openjfx')
#makedepends=('jdk-openjdk' 'gradle')
checkdepends=()
optdepends=()
provides=()
conflicts=('sdrtrunk')
replaces=()
backup=()
options=()
install=
changelog=
source=("https://github.com/DSheirer/sdrtrunk/releases/download/v${_pkgvertag}/${_filename}.zip"
	"sdrtrunk.desktop" "cat-radio-icon.png")
sha256sums=(SKIP
            'ea344583a65800239959917ef8849c725975ea05b571cbd74133b20b8c71f46d'
            '9cfe31c8bd4043891cf59aa76b33f30ed9b9f4403a386e5bf57f32226f3f2b26')

package() {
  install -Dm644 cat-radio-icon.png "${pkgdir}/usr/share/pixmaps/cat-radio-icon.png"
  install -Dm644 sdrtrunk.desktop   "${pkgdir}/usr/share/applications/sdrtrunk.desktop"
  
  cd "${_filename}"
  mkdir -p "${pkgdir}/opt/sdrtrunk"
  cp -ra * "${pkgdir}/opt/sdrtrunk"
  
}
