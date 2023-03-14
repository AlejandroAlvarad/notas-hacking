## Obejtivo
There is a website running at `https://jupiter.challenges.picoctf.org/problem/53751/` ([link](https://jupiter.challenges.picoctf.org/problem/53751/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:53751

## Hints
- The password is being filtered.

## Solución
```
A comparacion al anterior ya nos empieza a filtrar algunas cosas, no sabemos que nos filtra, pero adivinando suponiendo que hay un usuario "admin" ponemos un ; al final para que ignore la contraseña, entonces quedaría asi:
Usuario: admin';
Contraseña: cualquiera

Entramos y nos muestra
Your flag is: picoCTF{m0R3_SQL_plz_c34df170}
```
## Solucion
picoCTF{m0R3_SQL_plz_c34df170}