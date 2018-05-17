---
title: Instalando Unlaunch
layout: single
sidebar:
  nav: "side"
---

Si tu consola NO es de región USA, tienes que tener instalado un DSiWare previamente exploiteado para continuar.
{: .notice--info}

Unlaunch actualmente están beta. Por favor, procede con precaución.
{: .notice--info}

Unlaunch es un exploit bootcode de DSi que permite instalar HiyaCFW, un custom firmware de DSi a tu consola.

## Descargas
- La última versión de [Unlaunch](http://problemkaputt.de/unlaunch.zip)
- La última versión de [HBMenu](https://github.com/devkitPro/nds-hb-menu/releases/){:target="_blank"}
- La última versión de [ugopwn](/assets/files/ugopwn.zip)
  - Sólo para consolas de USA
- La última versión de [twlnf](https://github.com/Jimmy-Z/twlnf/releases){:target="_blank"}
- La última versión de [Python 3](https://www.python.org/downloads/){:target="_blank"}
- La última versión de [DSi SRL Extractor](/assets/files/dsi_srl_extract.zip)

## Preparando la tarjeta SD

1. Instala Python 3 en tu ordenador
2. Abre la aplicación de ajustes de sistema
3. Selecciona **Gestión de datos > Memoria del sistema > Flipnote Studio > Copiar > Sí**
	- Si no aparece gestión de datos, abre la tienda DSi, ciérrala, y vuelve a intentarlo
4. Cuando acabe apaga la consola
5. Saca la tarjeta SD de tu consola e insértala en el ordenador
6. Copia el contenido del archivo `.zip` de ugopwn a la raíz de tu SD
  - Sólo para consolas de USA
7. Copia el contenido del archivo `.7z` de twlnf a la raíz de tu SD, y renombra `twlnf.nds` a `boot.nds`
8. Copia el contenido del archivo `.zip` del DSi SRL Extractor a una carpeta en tu escritorio
9. Abre la raíz de tu tarjeta SD
10. Ve a /Private/DS/Title/
11. Copia el archivo`.bin` a tu carpeta del DSi SRL Extractor
12. Ejecuta el archivo console_id `.py` de dentro de la carpeta
  - Este script requiere [WINE](https://www.winehq.org/){:target="_blank"} en sistemas Mac/Linux/*nix
13. Cuando se abra, pulsa Enter
14. Copia el archivo console_id `.txt` a la raíz de tu tarjeta SD
15. Saca la tarjeta SD de tu ordenador y vuélvela a introducir en tu DSi

## Creando una copia de la NAND

1. Abre Flipnote Studio
  - Asegúrate de que *Iniciar en modo calendario* está desactivado en los ajustes de Flipnote Studio
  - If you already have another DSiWare exploit installed, open that and skip to Step 14
2. Select **View Flipnote > SD Card > Select Folder > User > ugopwn**
3. Click on the note with the red bottom half
4. Select "Edit"
5. Click on the Flipnote frog icon in the bottom left
6. Click on the film roll icon
7. Select **Copy > Back > Exit**
8. Click the second note.
9. Click on the Flipnote frog icon in the bottom left
10. Click on the film roll icon.
11. Click on the single right arrow (the next to last arrow icon) two times
  - You will see a new frame be created
12. Click on the paste button exactly 122 times.
13. Select "Erase" and then "Paste"
  - This should launch twlnf
14. When prompted, press **A** to create a nand backup
  - This will take a few minutes
  - Store this NAND backup in a safe location, it is a critical backup and we will need it later to install HiyaCFW
15. Press **B** to quit twlnf
  - Your console will power off

## Installation

1. Insert your system's SD card into your computer
2. Copy `BOOT.NDS` from the `hbmenu` folder in the HBMenu `.tar.bz2` file to the root of your SD card
  - twlnf is currently your `boot.nds`; for now, rename it to `boot.bak` or `twlnf.nds`
3. Copy `UNLAUNCH.DSI` from the Unlaunch `.zip` file to the root of your SD card
4. Rename `UNLAUNCH.DSI` to `unlaunch.nds`
5. Unplug your SD card, and insert it in your DSi
6. Power on your DSi, and repeat steps 1 through 13 in **Creating a NAND backup**
  - HBMenu should appear
7. Navigate to `unlaunch.nds`, and press **A**
  - Unlaunch's installer should appear
8. Navigate to `INSTALL NOW` and press **A**
  - If Unlaunch freezes at `LOADING FAT`, please read our [FAQ](/help/faq)
9. When done, navigate to `POWER DOWN` and press **A**
  - Your system will power off
10. Turn your system on, to verify Unlaunch installed properly
  - You should briefly see the Unlaunch screen, and boot into a version of the DSi Menu with no sound

With Unlaunch installed, your system now has primitive brick protection, unless the launcher's TMD file is destroyed. Unlaunch has protections that should prevent this from happening, and HiyaCFW uses your SD card as the DSi's NAND, making your system theoretically unbrickable.

[Installing HiyaCFW](/guide/installing-hiyacfw){: .btn .btn--light-outline}
{: style="text-align: center;"}
