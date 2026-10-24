# PKGBUILD para Aura Wallpaper (`aura-wallpaper-bin`)

Este repositorio contiene el script de empaquetado `PKGBUILD` para instalar **Aura** en **Arch Linux** y distribuciones derivadas utilizando el binario oficial precompilado.

---

## 📋 Descripción

**[Aura](https://github.com/antwny/aura)** es un gestor de fondos de pantalla animados en tiempo real (*live wallpaper manager*) escrito en Rust y optimizado para entornos de escritorio **COSMIC** y **GNOME** bajo **Wayland**.

Este paquete (`aura-wallpaper-bin`) descarga el lanzamiento oficial precompilado (`.tar.gz`), instala los binarios, archivos `.desktop`, iconos y metainformación directamente mediante `pacman`. De este modo:
* **No necesitas instalar Rust ni herramientas de compilación** (`cargo`, `rustc`, etc.).
* **Mantienes tu sistema limpio**: cada archivo queda registrado y controlado por el gestor de paquetes de Arch.

---

## 💳 Créditos y Agradecimientos

Este repositorio es únicamente un empaquetador para Arch Linux. El desarrollo, mantenimiento y autoría del software pertenecen íntegramente a su creador original:

* **Proyecto original:** [antwny/aura](https://github.com/antwny/aura)
* **Autor:** [@antwny](https://github.com/antwny)
* **Licencia original:** GNU General Public License v3.0 (GPL-3.0)

*(Si te gusta el proyecto, considera darle una estrella al repositorio oficial de Aura).*

---

## 🛠️ Requisitos Previos

Aura necesita de las siguientes dependencias multimedia en tu sistema (las cuales se verificarán durante la instalación):

* `mpv`
* `ffmpeg`
* `wayland`
* `libxkbcommon`

---

## 🚀 Instalación

### Opción A: Usando `git` y `makepkg` (Recomendado)

1. Clona este repositorio:
   ```bash
   git clone https://github.com/TheNextLVL/aura-wallpaper-bin.git
   cd aura-wallpaper-bin
   ```

2. Compila e instala el paquete con `makepkg`:
   ```bash
   makepkg -si
   ```

### Opción B: Usando un AUR Helper

Si utilizas un helper como `paru` o `yay` en un repositorio local:
```bash
paru -U
# o
yay -U
```

---

## 🗑️ Desinstalación

Para eliminar completamente la aplicación, sus accesos directos, iconos y dependencias no utilizadas, ejecuta:

```bash
sudo pacman -Rns aura-wallpaper-bin
```

---

## 🤖 Nota de Transparencia

> Este paquete `PKGBUILD` y la documentación de este repositorio han sido generados y estructurados con la asistencia de **Inteligencia Artificial**, adaptados específicamente para las directrices de empaquetado de Arch Linux y optimizados para el uso de binarios oficiales precompilados.

---

## 📄 Licencia

El script `PKGBUILD` contenido en este repositorio se distribuye bajo la misma licencia que el proyecto original (**GPL-3.0**). Todos los derechos de los binarios e iconos instalados por este paquete corresponden a [antwny](https://github.com/antwny).
