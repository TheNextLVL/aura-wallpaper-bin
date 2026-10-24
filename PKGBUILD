# Maintainer: TheNextLVL
pkgname=aura-wallpaper-bin
pkgver=1.7.2
pkgrel=1
pkgdesc="A native Rust live wallpaper manager for COSMIC and GNOME Wayland"
arch=('x86_64')
url="https://github.com/antwny/aura"
license=('GPL-3.0-only')
depends=('mpv' 'ffmpeg' 'wayland' 'libxkbcommon')
provides=('aura')
conflicts=('aura' 'aura-git' 'aura-bin')
source=("https://github.com/antwny/aura/releases/download/v${pkgver}/aura-v${pkgver}-x86_64-linux.tar.gz")
sha256sums=('SKIP')

package() {
    # Entramos a la subcarpeta que genera la extracción del tar.gz
    cd "$srcdir/aura-v${pkgver}-x86_64-linux"

    # 1. Instalación de los ejecutables principales
    install -Dm755 "aura" "$pkgdir/usr/bin/aura"
    install -Dm755 "mpvpaper" "$pkgdir/usr/bin/mpvpaper"

    # 2. Acceso directo de la aplicación (.desktop) para el menú de GNOME
    install -Dm644 "io.github.antwny.aura.desktop" "$pkgdir/usr/share/applications/io.github.antwny.aura.desktop"

    # 3. Metainformación de la aplicación (AppStream / Software Center)
    install -Dm644 "io.github.antwny.aura.metainfo.xml" "$pkgdir/usr/share/metainfo/io.github.antwny.aura.metainfo.xml"

    # 4. Iconos
    install -Dm644 "io.github.antwny.aura.svg" "$pkgdir/usr/share/icons/hicolor/scalable/apps/io.github.antwny.aura.svg"
    install -Dm644 "navbar-closed-symbolic.svg" "$pkgdir/usr/share/icons/hicolor/scalable/status/navbar-closed-symbolic.svg"
    install -Dm644 "navbar-open-symbolic.svg" "$pkgdir/usr/share/icons/hicolor/scalable/status/navbar-open-symbolic.svg"

    # 5. Licencia oficial
    if [ -f "LICENSE" ]; then
        install -Dm644 "LICENSE" "$pkgdir/usr/share/licenses/$pkgname/LICENSE"
    fi
}
