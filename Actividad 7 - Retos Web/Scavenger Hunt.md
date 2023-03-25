## Obejtivo
There is some interesting information hidden around this site [http://mercury.picoctf.net:27393/](http://mercury.picoctf.net:27393/). Can you find it?

## Hints
- 

## Solución
```
Inspeccionando el codigo encontramos esto
 Here's the first part of the flag: picoCTF{t 

Depues nos movemos al css y encontrmos esto:
/* CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */

Usamos este link http://mercury.picoctf.net:27393/robots.txt y encontramos esto:
User-agent: *
Disallow: /index.html
# Part 3: t_0f_pl4c
# I think this is an apache server... can you Access the next flag?

nos pasamos a 
 Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.

por ultimo
http://mercury.picoctf.net:27393/.DS_Store
Congrats! You completed the scavenger hunt. Part 5: _d375c750}

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_d375c750}
```
## Solucion