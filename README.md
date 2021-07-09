¿QUÉ ES MINERBOOT?
------------------

MinerBoot es un software que he programado en Visual Basic .NET para tener controladas las temperaturas de todas las GPUs de mi RIG de minado de criptomonedas.
En principio tenía que ser una aplicación solo para mi pero la he ido mejorando y creo que a alguien más le podría ser de uilidad.

Las tarjetas gráficas se calientan mucho al minar ya que funcionan al 100% de forma continua y en verano es prácticamente imposible tener el RIG encendido
sin el aire acondicionado ya que se sobrecalientan en exceso incluso haciendo undervolting.

¿CÓMO FUNCIONA?
---------------

La idea es simple, MinerBoot es un programa que hace una lista de todas las GPUs instaladas en el sistema y controla sus temperaturas, si alguna se pasa de la temperatura límite
que hemos marcado, MinerBoot se encargará de matar el proceso del minero, de hacer una pausa para que las GPUs se enfíen y luego volverá a lanzar el proceso de minero.

En la configuración de la aplicación podemos ajustar la temperatura límite para las GPUs, el ejecutable (.exe) del minero, la linea de comandos para lanzar el minero
y la forma de finalizar el proceso del minero (forzado o no):

Normal  -> Process.CloseMainWindow(): Es cómo si apretas el botón X para cerrar la ventana del minero.

Forzado -> Process.Kill(): Es cómo apretar Ctrl+Alt+Supr y finalizar la tarea en el task manager.


CÓDIGO DE TRECEROS
------------------
MinerBoot utiliza las librerías de Libre Hardware Monitor para leer las temperaturas y los nombres de las tarjetas gráficas.
https://github.com/LibreHardwareMonitor/LibreHardwareMonitor/releases


¿CON QUE SOFTWARE DE MINADO ES COMPATIBLE?
------------------------------------------
MinerBoot funciona con cualquier software de minería por GPU como T-REX, PhoenixMiner, XMRig, etc...
MinerBoot es una aplicación para sistemas operativos Windows y necesita permisos de administrador para ejecutarse correctamente.



Si se te ocurre alguna mejora o te gustaría agregar alguna funcionalidad, ponte en contacto conmigo.

CAPTURAS DEL PROGRAMA
---------------------
https://i.postimg.cc/rsbRb9j2/minerboot1.png

https://i.postimg.cc/N049YtD4/minerboot2.png
