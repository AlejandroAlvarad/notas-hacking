## Obejtivo
The password for the next level is stored in the file **data.txt** and is the only line of text that occurs only once

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit8**
TESKZC0XvTetK0S9xNwm25STk5iWrBvP

## Solución 
```
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
EN632PlfYiZbn3PhVK3XOGSlNInNE00t
```

## Notas adicionales 
| Comando | Descripción |
|-------|-----|
| sort | Ordena lineas de texto|
| uniq | Filtra los repetidos, cuenta los y filta los unicos|
| -u | Muestra solo los que no se repitieron |


## Referencia 
