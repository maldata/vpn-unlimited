# Maintainer: Mark Locascio <dr.mark.locascio@gmail.com>
pkgname=vpn-unlimited
pkgver=4.1
pkgrel=1
pkgdesc="VPN Unlimited client application"
arch=('x86_64')
url="https://www.vpnunlimitedapp.com"
license=('GPL')
#groups=()

#Depends: libc6 (>= 2.9), libqt5network5 (>= 5.2.1), libqt5script5 (>= 5.2.1), libqt5widgets5 (>= 5.2.1), libqt5core5a (>= 5.2.1), libqt5gui5 (>= 5.2.1), libqt5concurrent5 (>= 5.2.1), libqt5webkit5 (>= 5.1.1), libstdc++6 (>= 4.4.15), zlib1g (>=1.2.0), libcurl3 (>=7.22.0), libc-ares2(>=1.10.0), openvpn, resolvconf, liblzo2-2, libssl1.0.0 (>= 1.0.0), iproute, net-tools

#depends=()
#makedepends=()
#checkdepends=()
#optdepends=()
#provides=()
#conflicts=()
#replaces=()
#backup=()
#options=()
#install=
#changelog=
pkgfile=${pkgname}_${pkgver}_amd64.deb
source=("http://apt.keepsolid.com/debian/pool/main/v/vpn-unlimited/${pkgfile}")
#noextract=()
md5sums=("SKIP")
#validpgpkeys=()

prepare() {
    msg "Extracting from the .deb file..."
    cd ${srcdir}
    tar -xJf data.tar.xz
}

build() {
    msg "Nothing to build..."
}

check() {
    msg "Nothing to check..."
}

package() {
    msg "Moving the files into place..."
    
    install -d ${pkgdir}/usr
#    install -d ${pkgdir}/usr/local/${apprepo}/bin
#    install -d ${pkgdir}/usr/local/${apprepo}/etc
#    install -d ${pkgdir}/usr/local/${apprepo}/var
#    chmod 777 ${pkgdir}/usr/local/${apprepo}/var
    
    cp -r ${srcdir}/usr/* ${pkgdir}/usr
#    cp -r ${srcdir}/${cfgrepo}/* ${pkgdir}/usr/local/${apprepo}/etc/
#    chmod 755 ${pkgdir}/usr/local/${apprepo}/bin/runExpressLocker
    # Here we create a symlink in pkgdir pointing at the location
    # /usr/local/bin/runExpressLocker... even though it doesn't exist
    # on the build machine when the package is being built!
#    ln -s /usr/local/ExpressLocker/bin/runExpressLocker ${pkgdir}/usr/local/bin/runExpressLocker
    
    # make a symlink for the CLI tool
#    ln -s /usr/local/ExpressLocker/bin/runExpressLockerCli ${pkgdir}/usr/local/bin/expresslockercli   
}
