## Obejtivo
To get truly 1337, you must understand different data encodings, such as hexadecimal or binary. Can you get the flag from this program to prove you are on the way to becoming 1337? Connect with `nc jupiter.challenges.picoctf.org 15130`.

## Hints
- I hear python can convert things.
- It might help to have multiple windows open.

## Solución
```
th0rtilla-picoctf@webshell:~$ nc jupiter.challenges.picoctf.org 15130
Let us see how data is stored
animation
Please give the 01100001 01101110 01101001 01101101 01100001 01110100 01101001 01101111 01101110 as a word.
...
you have 45 seconds.....

Input:
animation
Please give me the  143 157 155 160 165 164 145 162 as a word.
Input:
computer
Please give me the 736f636b6574 as a word.
Input:
socket
You've beaten the challenge
Flag: picoCTF{learning_about_converting_values_02167de8}
```

## Solucion
Se tuvo que convertir de diferentes bases a texto, primero fue de binario, despues a octal y al final de hexa.
picoCTF{learning_about_converting_values_02167de8}
