## Obejtivo
The password for the next level is stored in a file called **spaces in this filename** located in the home directory

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit2**
**rRGizSaX8Mk1RTb1CNQoXTcYZWU6lgzi**

## Solución 
```
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat space_in_this_filename
cat: space_in_this_filename: No such file or directory
bandit2@bandit:~$ cat 'spaces in this filename'
aBZ0W5EmUfAf7kHTQeOwd8bauFJ2lAiG
bandit2@bandit:~$
```

## Notas adicionales 

## Referencia 
[Leer archivos con espacios en el nombre](https://linuxhint.com/reference-filename-with-spaces-linux/)