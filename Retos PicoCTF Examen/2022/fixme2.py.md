## Descripcion
Fix the syntax error in the Python script to print the flag.
Download Python script

## Hits
- Are equality and assignment the same symbol?
- To view the file in the webshell, do: $ nano fixme2.py
- To exit nano, press Ctrl and x and follow the on-screen prompts.
- The str_xor function does not need to be reverse engineered for this challenge.

## Solucion
```
th0rtilla-picoctf@webshell:~$ python3 fixme2.py
  File "/home/th0rtilla-picoctf/fixme2.py", line 22
    if flag = "":
       ^^^^^^^^^
SyntaxError: invalid syntax. Maybe you meant '==' or ':=' instead of '='?
th0rtilla-picoctf@webshell:~$ nano fixme2.py
th0rtilla-picoctf@webshell:~$ python3 fixme2.py
That is correct! Here's your flag: picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}
```
Fue un error de programación donde se intentaba hacer una coparación pero con un solo = y no con ==

## Bandera
picoCTF{3qu4l1ty_n0t_4551gnm3nt_4863e11b}