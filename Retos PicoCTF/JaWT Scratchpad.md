## Obejtivo

Check the admin scratchpad! `https://jupiter.challenges.picoctf.org/problem/58210/` or http://jupiter.challenges.picoctf.org:58210
## Hints
- What is that cookie?
- Have you heard of JWT?

## Solución
```
Con el token que nosotros tenemos lo mostramos con el editcooke y nos vamos a la pagina https://jwt.io/ y de ahí nos vamos a kali usando john, pero debemos  de descomprimir el rockyou y ya de ahi le pasamos el token que se nos genero en mi caso:


kali@kali:~$ john token -w=/usr/share/wordlists/rockyou.txt
Using default input encoding: UTF-8
Loaded 1 password hash (HMAC-SHA256 [password is key, SHA256 256/256 AVX2 8x])
Will run 2 OpenMP threads
Press 'q' or Ctrl-C to abort, almost any other key for status
ilovepico        (?)     
1g 0:00:00:07 DONE (2023-03-14 11:21) 0.1283g/s 949598p/s 949598c/s 949598C/s iloverob4live345..ilovemymother@
Use the "--show" option to display all of the cracked passwords reliably
Session completed. 
kali@kali:~$ 

se observa que que uso ilovepico y nos regresamos a la pagina para poder generarlo cambiando el usuario a admin y el token a ilovepico y nos da:

picoCTF{jawt_was_just_what_you_thought_44c752f5}

```
## Solucion
picoCTF{jawt_was_just_what_you_thought_44c752f5}