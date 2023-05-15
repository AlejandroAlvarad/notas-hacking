## Objetivo
We have recovered a [binary](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev) and a [text file](https://jupiter.challenges.picoctf.org/static/7aa5f383ec616fe9d72c2ffe1fabd0d9/rev_this). Can you reverse the flag.

## Hints
objdump and Gihdra are some tools that could assist with this

## Solución

```
cifrado = open('rev_this','r').read()

print (cifrado)

flag = ''

for i in range (8, len(cifrado)-1):
        if i &  1 == 0:
                flag += chr( ord(cifrado[i]) - 5 )
        else:
                flag += chr( ord(cifrado[i]) +2 )

print (flag)
r3v3rs36ad73964
```
## Bandera
picoCTF{r3v3rs36ad73964}