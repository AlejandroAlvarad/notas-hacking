## Descripcion
Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag in the same directory too.

## Hits
- Does that encoding look familiar?
- The str_xor function does not need to be reverse engineered for this challenge.

## Solucion
```
th0rtilla-picoctf@webshell:~$ nano level2.py
th0rtilla-picoctf@webshell:~$ python3
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> print(chr(0x64) + chr(0x65) + chr(0x37) + chr(0x36))
de76
>>> 

pasamos el contraseña a python para saber cual es saber la contraseña

th0rtilla-picoctf@webshell:~$ python3 level2.py
Please enter correct password for flag: de76
Welcome back... your flag, user:
picoCTF{tr45h_51ng1ng_489dea9a}
th0rtilla-picoctf@webshell:~$ 
Intoducimos la contraseña y nos da la bandera
```

## Bandera
picoCTF{tr45h_51ng1ng_489dea9a}