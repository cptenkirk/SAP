## Voreinstellungen in Linux

# SSD oder NVME Zugriffsrechte müssen auch verteilt werden!!!

# Max Map Count erhöhen (Essentiell für HANA):

bash

sudo sysctl -w vm.max_map_count=2147483647

# Gleichzeitige asynchrone E/A-Operationen anheben 

bash

sudo sysctl -w fs.aio-max-nr=18446744073709551615

# System-V-Shared-Memory-Segmente anpassen 

bash

sudo sysctl -w kernel.shmmni=32768

# Damit die Einstellungen auch nach einem Server-Neustart bleiben Öffnen Sie die Systemkonfiguration

bash

sudo nano /etc/sysctl.conf

# Fügen Sie ganz unten am Ende der Datei diese drei Zeilen ein

textvm.max_map_count=2147483647
fs.aio-max-nr=18446744073709551615
kernel.shmmni=32768



Default ABAP User

Client: 001
User: DEVELOPER
Password: ABAPtr2022#00