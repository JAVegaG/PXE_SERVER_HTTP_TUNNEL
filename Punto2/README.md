# Servicio PXE (Preboot eXecution Environment)

## DCHP (Dynamic Host Configuration Protocol)

El servicio DHCP sirve para asignar la ip a un número de hosts de forma automática ahorrando el trabajo manual de asignar una ip a cada uno de los computadores en una red. Esto resulta útil para el PXE a la hora de asignar la ip al cliente que use el servicio. Pero para conseguirlo es necesaro configurar la subred, la mascara, el rango de ips utilizables, la ip de boradcast (ultima ip de la red) y la ip del servidor. Para el servicio de PXE se agrega el archivo de instalación dentro del archivo de configuración de DHCP y se activan opciones de boot dentro del mismo. Todo esto se puede ver en el archivo de configuración anexo.

## TFTP (Trivial File Transfer Protocol)

El servicio TFTP suele usarse en redes de computadores y permite una transmisión de archivos como lo es el servicio FTP, pero de forma muy sencilla y básica, incluso a diferencia del FTP, TFTP usa el puerto 69 y el protocolo de transporte UDP en lugar de TCP. Para activarlo se configura la opción de disable a "no" en el archivo de configuración de TFTP.

## KICKSTART

Para que toda la instalación se realice automáticamente es necesario configurar un archivo de inicio rápido indicando todas las configuraciones iniciales que va a ejecutar el servicio de PXE, por ejemplo: la zona horaria, el idioma, los paquetes de descarga, etc. En este archivo se configura el acceso al TFTP indicando la ip del servidor y la ruta de acceso que se ha configurado con una contraseña encriptada que se ha obtenido durante el proceso de configuración del servicio PXE.

## PXE MENU FILE

Es el menu de configuración inicial para el boot del servicio. Este menu y sus caracteristicas se deben indicar en el archivo de configuración determinado de inicio.
  
