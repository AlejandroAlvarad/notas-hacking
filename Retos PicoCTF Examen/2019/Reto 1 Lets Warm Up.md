## Obejtivo
If I told you a word started with 0x70 in hexadecimal, what would it start with in ASCII?

## Hints
Submit your answer in our flag format. For example, if your answer was 'hello', you would submit 'picoCTF{hello}' as the flag.

## Solución
```
th0rtilla-picoctf@webshell:~$ python
Python 3.10.6 (main, Aug 10 2022, 11:40:04) [GCC 11.3.0] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> int (0x70)
112
>>> chr(112)
```
## Solucion
picoCTF{p}