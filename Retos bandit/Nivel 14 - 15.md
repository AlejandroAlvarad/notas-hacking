## Obejtivo
The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit14**
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
## Solución 
```
bandit14@bandit:~$ nc localhost 30000
fGrHPx402xGC7U7rXKDaxiWFTOiF0ENq
Correct!
jN2kgmIXJ6fShzhT2avhotn4Zcka6tnt
```
## Notas adicionales 
Entramos desde el localhost al puerto 30000 y ponemos la contraseña del nivel 14 para que nos de la siguiente contraseña
## Referencia 