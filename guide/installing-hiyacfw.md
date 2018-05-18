---
title: Instalando HiyaCFW
layout: single
sidebar:
  nav: "side"
---

Si tu consola NO es de región USA, tienes que tener instalado un DSiWare previamente exploiteado para continuar.
{: .notice--info}

Necesitarás [Unlaunch](/guide/installing-unlaunch/) instalado antes de proceder.
{: .notice--info}

No actualices el sistema despues de instalar HiyaCFW. Esto borrará los parches de HiyaCFW en tu SD.
{: .notice--danger}

HiyaCFW es un custom firmware para el Nintendo DSi que, una vez instalado, permitirá:
- Ejecutar el sistema desde una tarjeta SD
- Instalar aplicaciones homebrew en el menú de inicio
- Ejecutar flashcards bloqueadas en versiones superiores

## Requisitos
- La última versión de [Python 3](https://www.python.org/downloads/){:target="_blank"}
  - Tú tendrías que tener esto de una sección anterior
- Una tarjeta SD de 2GB o menor, o una tarjeta SD mayor particionada a 2GB or menor
- La última versión de [twlnf](https://github.com/Jimmy-Z/twlnf/releases){:target="_blank"}
- La última versión de [HiyaCFW](https://github.com/Robz8/hiyaCFW/releases){:target="_blank"}
- La última versión de [ugopwn](/assets/files/ugopwn.zip)
- [NUSDownloader](/assets/files/NUSDownloader.zip)
- Una copia de la NAND tomada de tu dispositivo, con el footer de NO$GBA
  - twlnf crea este footer automáticamente cuando hace una copia
  - Tú tendrías que tener esta copia de una sección anterior
- [Scripts de ayuda para la instalación de HiyaCFW](/assets/files/hiyacfw_helper.zip)

## Preparation
1. Inserta tu tarjeta SD de 2GB o menor en tu ordenador
2. Copia *el contenido* del archivo `.zip` de NUSDownloader a una carpeta en tu ordenador
3. Copia *el contenido* del archivo `.7z` de HiyaCFW a una carpeta en tu ordenador
4. Copia *el contenido* del archivo `.7z` de HiyaCFW helper a la carpeta `for PC` dentro de tu carpeta de HiyaCFW
5. Copia *el contenido* del archivo `.zip` de ugopwn a la raíz de tu SD de 2GB o menor
5. Copia *el contenido* del archivo `.7z` de twlnf a la raíz de tu SD de 2GB o menor, y renombra `twlnf.nds` a `boot.nds`
6. Copia `console_id.txt` de la raíz de tu tarjeta SD normal a la raíz de tu SD de 2GB o menor
  - Esto sólo aplica si tu SD de 2GB o menor no es tu tarjeta SD normal
7. Copia `nand.bin` y `nand.bin.sha` de la raíz de tu tarjeta SD normal a la raíz de tu SD de 2GB o menor
8. Abre NUSDownloader en tu computadora
  - Esto puede ser hecho mediante [Mono](http://www.mono-project.com/) en sistemas Mac/Linux/*nix
9. Marca la casilla "Create Decrypted Contents (*.app)", y desmarca "Keep Enc. Contents"
10. Selecciona **Database > System (DSi) > System Menu (Launcher) > [Your Region] > v512 > Start NUS Download!**
11. Sal de NUS Downloader
12. Navega a **titles > 00030017484e41XX > 512** en tu carpeta de NUS Downloader
13. Copia `00000002.app` de la carpeta `512` a la carpeta `for PC` de HiyaCFW
14. Copia tu copia válida de NAND (`nand.bin`) a la carpeta `for PC` de HiyaCFW

## Instrucciones
1. Inserta tu SD de 2GB o menor en tu consola
2. Enciende tu DSi
3. Abre Flipnote Studio
  - Asegúrate que el modo de *Calendario al inicio* esté deshabilitado en la configuración de Flipnote Studio
  - Si tienes otro DSiWare exploiteado instalado, ábrelo y salta hasta el paso 16
4. Selecciona **Ver nota > Tarjeta SD > Elegir carpeta > Usuario > ugopwn**
5. Haz click en la nota con la mitad inferior roja
6. Selecciona "Modificar"
7. Haz click en el icono de la rana de Flipnote de la esquina inferior izquierda
8. Haz click en el icono de rollo de película
9. Selecciona **Copiar > Atrás > Salir**
10. Haz click en la segunda nota.
11. Haz click en el icono de la rana de Flipnote de la esquina inferior izquierda
12. Haz click en el icono de rollo de película.
13. Haz click en la singular flecha derecha (la siguiente al último icono de flecha) dos veces
  - Verás un nuevo cuadro crearse
14. Haz click en el botón pegar exactamente 122 veces.
15. Selecciona "Borrar" y luego "Pegar"
  - Esto debería ejecutar twlnf
16. Presiona **X** para mountar la NAND directamente
17. Presiona **START** para abrir el menú de twlnf
18. Presiona **R** para copiar el contenido de la NAND a tu tarjeta SD
  - Esto tomará varios minutos
  - Mantén tu consola cargándose durante este proceso, para evitar una pérdida repentina de energía
  - Cuando `walk returned 0` aparezca, el proceso se ha completado
19. Una vez terminado, presiona **Select** para salir de twlnf
20. Presiona **A** para confirmar
  - Tu consola se apagará
21. Inserta tu tarjeta SD de 2GB o menor en tu ordenador
22. Mueve todos los archivos de la carpeta `dump` a la raíz de tu tarjeta SD
  - Esto prepara la "SD NAND", de la cual HiyaCFW se ejecutará
23. Navega a la carpeta `for PC` de HiyaCFW
24. Ejecuta `hiyacfw_helper.py` para preparar las modificaciones
  - Este script requiere [WINE](https://www.winehq.org/){:target="_blank"} en sistemas Mac/Linux/*nix
25. Abre la nueva carpeta `Modified Files`
26. Copia `bootloader.nds` a la raíz de tu SD de 2GB o menor
27. Copia 00000002.app a la carpeta **title > 00030017 > 484e41XX > content** en tu SD de 2GB o menor
28. Copia *el contenido de* la carpeta `for 2GB (or lower) SD card (SDNAND)` de HiyaCFW a la raíz de tu SD de 2GB o menor
29. Saca la tarjeta SD de 2GB o menor, e insértala en tu DSi
30. Enciende tu consola
  - La pantalla de bienvenida de HiyaCFW debería aparecer

Tu sistema ahora debería arrancar desde la tarjeta SD en vez de la NAND interna.

[Finalizar Instalación](/guide/finalizing-setup){: .btn .btn--light-outline}
{: style="text-align: center;"}
