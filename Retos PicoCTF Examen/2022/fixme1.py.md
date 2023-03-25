## Descripcion
Fix the syntax error in this Python script to print the flag.
Download Python script

## Hits
- Indentation is very meaningful in Python
- To view the file in the webshell, do: $ nano fixme1.py
- To exit nano, press Ctrl and x and follow the on-screen prompts.
- The str_xor function does not need to be reverse engineered for this challenge.

## Solucion
```
th0rtilla-picoctf@webshell:~$ python3 fixme1.py
  File "/home/th0rtilla-picoctf/fixme1.py", line 20
    print('That is correct! Heres your flag: ' + flag)
IndentationError: unexpected indent
th0rtilla-picoctf@webshell:~$ nano fixme1.py
th0rtilla-picoctf@webshell:~$ python3 fixme1.py 
That is correct! Heres your flag: picoCTF{1nd3nt1ty_cr1515_09ee727a}
```
El error estaba en que la ultima linea de codigo tenia una sangria y tuvimos que borrarla para que funcionara
## Bandera
picoCTF{1nd3nt1ty_cr1515_09ee727a}