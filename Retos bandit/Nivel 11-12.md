## Obejtivo
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions
## Datos de acceso
**bandit.labs.overthewire.org**
**bandit11**
6zPeziLdR2RKNdNYFNb6nVCKzphlXHBM
## Solución 
```
bandit11@bandit:~$ ls
data.txt
bandit11@bandit:~$ cat data.txt | tr "a-zA-Z" "n-za-mN-ZA-M"
The password is JVNBBFSmZwKKOP0XbFXOoW8chDz5yVRv
bandit11@bandit:~$
```
## Notas adicionales 

## Referencia 