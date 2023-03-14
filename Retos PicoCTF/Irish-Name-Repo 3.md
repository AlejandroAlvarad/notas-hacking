## Obejtivo
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/40742/` ([link](https://jupiter.challenges.picoctf.org/problem/40742/)) or http://jupiter.challenges.picoctf.org:40742. Try to see if you can login as admin!

## Hints
- Seems like the password is encrypted.

## Solución
```
La contraseña esta encriptado de ROT13, entonces usando eso rotamos el ' or 1==1; y la rotacion la metemos en la contraseña que quedaria como ' be 1==1;

Entramos y nos da esto: Your flag is: picoCTF{3v3n_m0r3_SQL_4424e7af}
```
## Solucion
picoCTF{3v3n_m0r3_SQL_4424e7af}