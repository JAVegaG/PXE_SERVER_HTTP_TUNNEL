# Tunel del servicio HTTP

## PORT FORWARDING

Permite la conexión entre los puertos de la maquina virtual (servidor) y el host (maquina real) lo que hace posible acceder al servidor HTTP usando localhost e indicando el puerto de acceso (que a su vez está conectado al puerto de HTTP del servidor), para esto se configura el vagrantfile de la maquina y se indica que puerto se desea conectar entre host y maquina virtual por ejemplo el puerto 80 del servidor y el 8080 del host (esto se puede ver en el Vagrantgile anexado).

## TUNEL PARA ACCESO WEB REMOTO

Permite el acceso al servicio HTTP desde cualquier lugar de la web a través de una URL temporal usando el vagrant share que comparte el puerto del servidor (en la practica se usaba el puerto que en el item anterior correspondia al host (8080)) y el driver ngrok que crea el tunel y su correspondiente URL, la sintaxis del codigo fue:

vagrant share servidor --http 8080 --driver ngrok

