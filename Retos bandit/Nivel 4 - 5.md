## Obejtivo
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit4**
2EW7BBsr6aMMoJ2HjW067dm8EgX26xNe

## Solución 
```
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file01  -file02  -file03  -file04  -file05  -file06  -file07  -file08  -file09
bandit4@bandit:~/inhere$ cat ./-file00
T߼B#6Kt36Xt��)bandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ cat ./-file01
g       ضb~]CgnSkIbandit4@bandit:~/inhere$ cat ./-file02
E\>b+6ћOg-/~7ZDXbandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ cat ./-file03
ZП`l7
 w]bandit4@bandit:~/inhere$ cat ./-file04
,%)��ё;He.1;        bandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ cat ./-file05
zh@aӿmx ԒuiߚN86bandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ cat ./-file06
evNȕ"=lҙ#      /+].?bandit4@bandit:~/inhere$
bandit4@bandit:~/inhere$ cat ./-file07
lrIWWI6bB37kxfiCQZqUdOIYfr6eEeqR
bandit4@bandit:~/inhere$
```

## Notas adicionales 
Se pueden usar el comando file ./* para saber que tipo de archivos de archivos era, y solo ver el que fuera ASCII (este comando se debe ejecutar dentro de la carpeta inhere)

## Referencia 
