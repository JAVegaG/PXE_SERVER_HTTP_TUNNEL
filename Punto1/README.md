# **HTTP service tunnel**

## PORT FORWARDING

It allows the connection between the ports of the virtual machine (server) and the host (real machine) which makes it possible to access the HTTP server using localhost and to indicate the access port (which in turn is connected to the HTTP port of the server) For this, the vagrantfile of the machine is configured. Also, the port to be connected between the host and virtual machine is designated, for instance, port 80 of the server and 8080 of the host (this can be seen in the attached Vagrantgile).

## TUNNEL FOR REMOTE WEB ACCESS

It allows access to the HTTP service from anywhere on the web through a temporary URL using the vagrant share that shares the server port (in practice the port that in the previous item corresponds to the host (8080) was used) and the ngrok driver that creates the tunnel and its corresponding URL, the code syntax was:

>vagabond share server --http 8080 --driver ngrok

