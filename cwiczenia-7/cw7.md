
Zadanie
------------

![zadanie 7](nat-2.svg)

2. 
    * Przygotuj konfigurację sieci zgodnie z powyższym diagramem
    * Wykonaj konfigurację translacji adresów tak aby udostępnic komunikację z siecią internet dla ``PC-2`` oraz ``PC-3``
    
3. 
    * Rozszerz architekturę o automatyczną konfigurację hostów w podsieciach ``192.168.64.192/27`` oraz ``172.16.95.216/29`` z wyykorzystaniem usługi ``DHCP``
    * Rozpocznij od zapoznania się z dokumentacją oraz instalacji programu ``isc-dhcp-server`` dla ``PC1``

 ## Rozwiązanie:
 
 
 ## Tworzymy 2 sieci NAT
192.168.64.192/27<br>
172.16.95.216/29<br>


## PC1
enp0s8 - 192.168.64.193/27<br>
enp0s3 - NAT<br>
enp0s9 - 172.16.95.217/29<br>

## PC2
enp0s3 - 192.168.64.194/27<br>

## PC3
enp0s3 - 172.16.95.218/29<br>

## PC1 - ustawiamy forwarding:
echo 1 > /proc/sys/net/ipv4/ip_forward<br>

## PC1 - udostępniamy internet:
iptables -t nat -A POSTROUTING -o enp0s3 -j MASQUERADE<br>

## PC2 - ustawiamy routing:

ip route add default via 192.168.64.193 dev enp0s3<br>

## PC3 - ustawiamy routing:

ip route add default via 172.16.95.217 dev enp0s3<br>
