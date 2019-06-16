Ustawianie parametrów sieci
---------------------------
1. na 1 z komputerów zainstaluj oprogramowanie ``http-chat`` dostępne pod adresem ``https://github.com/jkanclerz/http-chat``

Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcjonalny) |
| ------------- |:-------------:| -----:|
| PC 1 | lubuntu 17.04 |
| IP - address  | 10.0.2.15 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  | lubuntu 17.04 | |
| IP - address  | 10.0.2.4 | |
| MASKA  | 255.255.255.0 | |


Statyczna konfiguracja parametrów połączenia
Wejściowe parametry sieci
-------------------------
| Parametr | wartość | komentarz(opcjonalny) |
| ------------- |:-------------:| -----:|
|   PC 1 |  
| IP - address  | 192.168.10.10 | |
| MASKA  | 255.255.255.0 | |
|   |  | |
| PC 2  |  | |
| IP - address  | 172.16.100.100 | |
| MASKA  | 255.255.0.0 | |

Warto wiedzieć
-------------------------
| Parametr | wartość | komentarz(opcjonalny) |
| ------------- |:-------------:| -----:|
| Lokalizacja pliku z konfiguracją sieci| /etc/network/interfaces | |
| UP -> Wyłączenie interfejsu sieciowego| ifup | |
| DOWN -> Włączenie interfejsu sieciowego| ifdown | |
| Sprawdzenie obecnych parametrów | nmcli | |
| lista wszystkich interfejsów | ip a | |
| Które interfejsy jakie porty słuchają | netstat --listen | |
| wyswietlenie pliku konfiguracyjnego DNS | cat /etc/resolv.conf | |
| symulacja przegladarki | curl -X |
