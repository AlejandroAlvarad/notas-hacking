## Obejtivo
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit5**
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR

## Solución 
```
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ la
maybehere00  maybehere03  maybehere06  maybehere09  maybehere12  maybehere15  maybehere18
maybehere01  maybehere04  maybehere07  maybehere10  maybehere13  maybehere16  maybehere19
maybehere02  maybehere05  maybehere08  maybehere11  maybehere14  maybehere17
bandit5@bandit:~/inhere$ file ./-maybehere0?
./-maybehere0?: cannot open `./-maybehere0?' (No such file or directory)
bandit5@bandit:~/inhere$ file ./maybehere0?
./maybehere00: directory
./maybehere01: directory
./maybehere02: directory
./maybehere03: directory
./maybehere04: directory
./maybehere05: directory
./maybehere06: directory
./maybehere07: directory
./maybehere08: directory
./maybehere09: directory
bandit5@bandit:~/inhere$ file ./*/*
./maybehere00/-file1:       ASCII text, with very long lines (1038)
./maybehere00/-file2:       ASCII text, with very long lines (9387)
bandit5@bandit:~/inhere$ find -readdable -c 1033c -type f
find: unknown predicate `-readdable'
bandit5@bandit:~/inhere$ find -readable -c 1033c -type f
find: unknown predicate `-c'
bandit5@bandit:~/inhere$ find -readable -size 1033c -type f
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
P4L4vucdmLnm8I7Vl7jG1ApGSfjYKqJU
```

## Notas adicionales 
| Comando | Descripción |
|-------|-----|
| find | Busca archivos en el sistema |
| -readable | Que el archivo sea legible (ASCII) |
| -size | Permite especificar el tamaño |
| -type | Permite especificar el tipo de archivo |

man find
h - Muestra la ayuda dentro del manual de ayuda
/ - readable - Busca la palabra readable, estando dentro de la ayuda del manual
N - Busca la siguiente ocurrencia hacia atras
n - Busca la siguiente ocurrencia hacia adelante
q - Salir del manual de ayuda
## Referencia 