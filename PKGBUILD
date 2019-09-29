pkgname=signal-desktop
pkgver=1.27.3
pkgrel=1
pkgdesc='Private messaging from your desktop'
arch=('x86_64')
url='https://github.com/WhisperSystems/Signal-Desktop'
license=('GPL3')
options=(!strip)
depends=('gconf' 'gtk2' 'libnotify' 'libxtst' 'nss' 'xdg-utils' 'libxss')

sha512sums=('21a00820cb218e155020e6a2e24d3235fca77dd714c3c13263fe435d5326caf57caea8461f0b5830fb1762b0f567864496ad26299c3cb326ddcbd64951a21d7c'
            '7db7ee79a07fb86fec471e63c5189d61e8a2ca8fc2e659ea89ef22516e24e0a3c9f32c93f8ee520f56abc187b9b9304355e8aadb427c4920cda4f663ab1489fa')
source=("https://updates.signal.org/desktop/apt/pool/main/s/signal-desktop/signal-desktop_${pkgver}_amd64.deb"
        'signal-desktop')

package() {
  # extract package data
  tar xf data.tar.xz -C "${pkgdir}"

  # install alias in /usr/bin
  mkdir "${pkgdir}/usr/bin"
  install -D -m755 signal-desktop "${pkgdir}/usr/bin/signal-desktop"
}
