## Objetivo
In RSA, a small `e` value can be problematic, but what about `N`? Can you decrypt this? [values](https://mercury.picoctf.net/static/12d820e355a7775a2c9129b2622a7eb6/values)

## Hints
Bits are expensive, I used only a little bit over 100 to save money

## Solución

```
Decrypt my super sick RSA:
c: 843044897663847841476319711639772861390329326681532977209935413827620909782846667
n: 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
e: 65537
th0rtilla-picoctf@webshell:~/MindPsQs$ 

En Python
>>> c = 843044897663847841476319711639772861390329326681532977209935413827620909782846667
>>> n = 1422450808944701344261903748621562998784243662042303391362692043823716783771691667
>>> e = 65537

Para sacar P y Q usaremos la pagina de http://factordb.com/ para poder sacarlos

>>> from Crypto.Util.number import inverse, long_to_bytes
>>> p = 2159947535959146091116171018558446546179
>>> q = 658558036833541874645521278345168572231473
>>> phi = (p - 1)*(q - 1)
>>> d = inverse(e, phi)
>>> m = pow(c,d,n)
>>> print(long_to_bytes(m))
b'picoCTF{sma11_N_n0_g0od_00264570}'
```
## Bandera
picoCTF{sma11_N_n0_g0od_00264570}