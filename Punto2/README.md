# **PXE Server (Preboot eXecution Environment)**

## DCHP (Dynamic Host Configuration Protocol)

The DHCP service is used to assign the IP to a number of hosts automatically, saving the manual work of assigning an IP to each of the computers on a network. This is useful for PXE when assigning the Ip to the client that uses the service. But to achieve this it is necessary to configure the subnet, the mask, the range of usable Ips, the broadcast Ip (last Ip of the network), and the server ip. For the PXE service, the installation file is added to the DHCP configuration file and boot options are activated within it. All this can be seen in the attached configuration file.

## TFTP (Trivial File Transfer Protocol)

The TFTP service is usually used in computer networks and allows file transmission like the FTP service, but in a very simple and basic way, even unlike FTP, TFTP uses port 69 and the UDP transport protocol instead of TCP. To enable it, set the disable option to "no" in the TFTP configuration file.

## KICKSTART

In order for the entire installation to be carried out automatically, it is necessary to configure a quick start file indicating all the initial configurations that the PXE service is going to execute, for example, the time zone, the language, the download packages, etc. In this file, access to the TFTP is configured, indicating the IP of the server and the path that has been configured with an encrypted password that has been obtained during the configuration process of the PXE service.

## PXE MENU FILE

It is the initial configuration menu for starting the service. This menu and its characteristics must be indicated in the file of certain startup configurations.  
