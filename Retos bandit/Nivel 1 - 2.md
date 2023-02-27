## Obejtivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit1**
**NH2SXQwcBdpmTEzi3bvBHMM9H66vVXjL**

## Solución 
```
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ whoami
bandit1
bandit1@bandit:~$ pwd
/home/bandit1
bandit1@bandit:~$ cat -
^C
bandit1@bandit:~$ cat ./-
rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi
bandit1@bandit:~$
```

## Notas adicionales 
Cuando se inteta leer un archivo llamado "-" se hace bola y no abre

## Referencia 
[Archivos con guiones](https://stackoverflow.com/questions/42187323/how-to-open-a-dashed-filename-using-terminal)
