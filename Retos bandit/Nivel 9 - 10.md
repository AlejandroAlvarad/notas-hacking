## Obejtivo
The password for the next level is stored in the file **data.txt** in one of the few human-readable strings, preceded by several ‘=’ characters.

## Datos de acceso
**bandit.labs.overthewire.org**
**bandit9**
EN632PlfYiZbn3PhVK3XOGSlNInNE00t

## Solución 
```
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ string data.txt -n 10
Command 'string' not found, did you mean:
  command 'strings' from deb binutils (2.38-4ubuntu2.1)
  command 'spring' from deb ruby-spring (2.1.1-2)
  command 'spring' from deb spring (105.0.1+dfsg-4)
Try: apt install <deb name>
bandit9@bandit:~$ strings data.txt -n 10
c========== the
h;========== password
========== isT
Q!%     6eSvd]
n.E========== G7w8LIi6J3kTb8A7j9LgrywtEUlyyp6s
e:V&nQutgo
bandit9@bandit:~$
```

## Notas adicionales 
| Comando | Descripción |
|-------|-----|
| strings | Te muestras las cadenas imprimibles |
| -n | Numero minimo de caracteres |

## Referencia 