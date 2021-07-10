EL PROBLEMA
------------------
Las tarjetas gráficas (GPUs) se calientan mucho al minar criptomonedas ya que funcionan al 100% de forma continuada y en verano es prácticamente imposible tener el RIG encendido
sin poner el aire acondicionado o un ventilador al lado ya que se sobrecalientan en exceso incluso haciendo undervolting.

He tratado de buscar algún software como CoreTemp (https://www.alcpu.com/CoreTemp/) que vigila las temperaturas de los núcleos de la CPU y si estas aumentan en exceso, pone el sistema a hibernar. Pero no he encontrado nada parecido para las GPUs, así que he decidido programarlo yo mismo.


¿QUÉ ES MINERBOOT?
------------------
MinerBoot es un software que he programado en Visual Basic.NET para tener controladas las temperaturas de todas las GPUs de mi RIG de minado de criptomonedas y una especie de sistema de seguridad anti sobrecalentamiento.

En principio tenía que ser una aplicación solo para mi pero la he ido mejorando y creo que a alguien más le podría ser de uilidad.


¿CÓMO FUNCIONA?
---------------
La idea es simple, MinerBoot crea una lista de todas las GPUs instaladas en el sistema y controla sus temperaturas. A diferencia de CoreTemp, MinerBoot no pone el sistema a hibernar. Si alguna GPU supera la temperatura límite que hemos marcado previamente, este software se encargará de finalizar el proceso del minero, luego hará una pausa de X minutos para que las GPUs se enfíen y luego volverá a lanzar el proceso del minero.

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
MinerBoot funciona con cualquier software de minería por GPU como T-REX, PhoenixMiner, etc...


¿CON QUE SISTEMAS OPERATIVOS ES COMPATIBLE?
------------------------------------------
MinerBoot es una aplicación para sistemas operativos Windows (7, 8 y 10) y necesita permisos de administrador para poder leer las temperaturas de las GPUs correctamente.


CAPTURAS DEL PROGRAMA
---------------------
https://i.postimg.cc/rsbRb9j2/minerboot1.png

https://i.postimg.cc/N049YtD4/minerboot2.png


Si se te ocurre alguna mejora o te gustaría agregar alguna funcionalidad, ponte en contacto conmigo y lo hablamos.
