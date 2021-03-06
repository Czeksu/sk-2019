Struktura adresu IP
-------------------
```192.168.100.192```
```255.255.255.0```

Podział na równą ilość podsieci
-------------------------------
```2^S >= n```
Chcemy 7 -> 2^3 >= 7
Maska -> 255.255.255.11100000 -> 255.255.255.224 -> /27

Wprowadzenie
------------
------------------------------
| dziesiętnie |  binarnie   | 
| --------- |:-------------| 
| ``10``  | 1010 | 
| ``92``  | 0101 1100 | 
| ``37``  | 0010 0101 | 
| ``240`` | 1111 0000 | 
| ``192`` | 1100 0000 | 
| ``255`` | 1111 1111 | 
| ``128`` | 1000 0000 | 
| ``168`` | 1010 1000 | 


------------------------------
| binarnie |  dziesiętnie   | 
| --------- |:-------------| 
| ``00100000``  | 32 | 
| ``11111000``  | 248 | 
| ``10100000``  | 160 | 
| ``00110000`` | 48 | 
| ``10101100`` | 172 | 
| ``01000000`` | 64 | 
| ``11111100`` | 252 | 
| ``01100010`` | 98 | 
 
Notacja CIDR
------------
 
------------------------------
| maska |  /(X) x - liczba bitów   | 
| --------- |:-------------| 
| ``255.255.255.0``   | /24 | 
| ``255.128.0.0``     | /9 | 
| ``255.255.252.0``   | /14 | 
| ``255.255.254.0``   | /15 | 
| ``255.255.255.240`` | /20 | 
| ``255.240.0.0``     | /12 | 

------------------------------
| CIDR |  Maska   | 
| --------- |:-------------| 
| ``/8``    | 255.0.0.0 | 
| ``/20``   | 255.255.240.0 | 
| ``/30``   | 255.255.255.252 | 
| ``/16``   | 255.255.0.0 | 
| ``/27``   | 255.255.255.224 | 
| ``/11``   | 255.224.0.0 | 


Liczba hostów
-------------

------------------------------
| sieć |  liczba   | 
| --------- |:-------------| 
| ``10.0.0.0/8``    | 16777214 | 
| ``172.16.0.0/16``   | 65534 | 
| ``192.168.1.0/24``   | 254 | 
| ``192.168.1.0/27``   | 30 | 
| ``192.168.1.0/29``   | 6 | 
| ``192.168.1.0/31``   | 1 | 

