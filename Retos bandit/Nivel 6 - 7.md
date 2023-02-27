## Obejtivo
The password for the next level is stored **somewhere on the server** and has all of the following properties:

-   owned by user bandit7
-   owned by group bandit6
-   33 bytes in size

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit6**
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU

## Solución 
```
bandit6@bandit:~$ ls
bandit6@bandit:~$ pwd
/home/bandit6
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>7dev/null
-bash: 7dev/null: No such file or directory
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c 2>/dev/null
/var/lib/dpkg/info/bandit7.password
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
z7WtoNQU2XfjmMtWA8u5rN4vzqu4v99S
bandit6@bandit:~$
```

## Notas adicionales 
| Comando | Descripción |
|-------|-----|
| find | Busca archivos en el sistema |
| / | Indica a find inicar la busqueda desde la raíz / del sistema de archivo |
| -user | Indica al find el usuario al que pertenece el archivo |
| -group | Indica al find el grupo al que pertenece el archivo |
| 2>/dev/null | Envia los errores de la ejecución del comando al dispositivo null (no aparece en la pantalla) |

## Referencia 