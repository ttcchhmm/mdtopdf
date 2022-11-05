_pkgname=mdtopdf
pkgname=$_pkgname-git
pkgver=0 # Placeholder
pkgrel=1
pkgdesc='Small script used to convert Markdown files to PDF using Pandoc (Development version)'
url='https://github.com/ttcchhmm/mdtopdf'
arch=('any')
license=('GPL2')

depends=('bash' 'pandoc' 'texlive-bin' 'noto-fonts' 'ttf-droid')
makedepends=('git')

source=('git+https://github.com/ttcchhmm/mdtopdf.git')

pkgver() {
    cd mdtopdf
    git describe --long | sed 's/-/.r/;s/-/./'
}

package() {
    cd "${srcdir}/${_pkgname}"

    install -D mdtopdf "${pkgdir}/usr/bin/mdtopdf" 
}