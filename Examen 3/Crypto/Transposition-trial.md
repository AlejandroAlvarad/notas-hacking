## Objetivo
Our data got corrupted on the way here. Luckily, nothing got replaced, but every block of 3 got scrambled around! The first word seems to be three letters long, maybe you can use that to recover the rest of the message.Download the corrupted message [here](https://artifacts.picoctf.net/c/191/message.txt).

## Hints
Split the message up into blocks of 3 and see how the first block is scrambled

## Solución
Usamo el siguiente codigo
```
ctxt = "heTfl g as iicpCTo{7F4NRP051N5_16_35P3X51N3_V6E5926A}4"
ptxt = ""

for i in range(len(ctxt)):
    if i % 3 == 0 and i + 2 < len(ctxt):
        ptxt = ptxt + ctxt[i+2] + ctxt[i]
    elif i % 3 == 2:
        pass
    else:
        ptxt = ptxt + ctxt[i]

print(ptxt)
```
## Bandera
The flag is picoCTF{7R4N5P051N6_15_3XP3N51V3_56E6924A}
