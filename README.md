# openvpn-auto-script

This script can be used in order to install and configure openvpn server and clients

```
STEP 1 : Create Ubuntu 18 machine ( in this case in Azure ) and open the ports UDP/1194 TCP/943
STEP 2 : First time you run the script on the server it will install and configure the Openvpn , the other times you can create new client certs or change openvpn config ...
       
       bash openvpn-install.sh
    
STEP 3 : Copy the client.ovpn file ( should be in Ubuntu /root ) to your client machine and connect running :

	$ sudo apt update
	
	$ sudo apt install openvpn
        
	$ sudo apt install epel-release
        
	$ sudo apt install openvpn
        
	$ ls /etc/openvpn           
	// expected output update-resolv-conf
        
	$ nano client.ovpn
	add:
	up /etc/openvpn/update-resolv-conf
        down /etc/openvpn/update-resolv-conf
	
	$ sudo openvpn --config client.ovpn 
        
       
                 
        
        ```


