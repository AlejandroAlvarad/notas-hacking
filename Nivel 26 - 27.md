## Obejtivo
Good job getting a shell! Now hurry and grab the password for bandit27!
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit26**
c7GvcKlw9mC7aUQaPx7nwFstuAIBw1o1
## Solución 
```
bandit26@bandit:~$ ls
bandit27-do  text.txt
bandit26@bandit:~$ ./bandit27-do cat /etc/bandit_pass/bandit27
YnQpBuifNMas1hcUFk70ZmqkhUU2EuaS
bandit26@bandit:~$
```
## Notas adicionales 
Seguimos abusando del **more** una vez entramos al editor usamos los comandos 
**:set shell=/bin/bash**
**:set shell**
una vez ejecutados ya podemos escapar del scrip
para salir del editor ocupamos el comando 
**:qa**
## Referencia