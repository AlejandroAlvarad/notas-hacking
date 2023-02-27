## Obejtivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit12**
JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
## Solución 
```
bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat
The password is wbWdlBxEir4CaE8LaPhauuOo6pwRmrDw
```
## Notas adicionales 
La contraseña estaba comprimida en varios tipos de compresiones, tuvimos que estar usando el comando "file -" al final para saber como descomprimirlo
## Referencia 