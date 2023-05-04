## Objetivo
What does asm3(0xd73346ed,0xd48672ae,0xd3c8b139) return? Submit the flag as a hexadecimal value (starting with '0x'). NOTE: Your submission for this question will NOT be in the normal flag format. [Source](https://jupiter.challenges.picoctf.org/static/17c5620fcffa388fe518d31cb4dd99a0/test.S)

## Hints
more(?) [registers](https://wiki.skullsecurity.org/index.php?title=Registers)

## Solución

```
        <+0>:   push   ebp
        <+1>:   mov    ebp,esp
        <+3>:   xor    eax,eax
        <+5>:   mov    ah,BYTE PTR [ebp+0xa]
        <+8>:   shl    ax,0x10
        <+12>:  sub    al,BYTE PTR [ebp+0xc]
        <+15>:  add    ah,BYTE PTR [ebp+0xd]
        <+18>:  xor    ax,WORD PTR [ebp+0x10]
        <+22>:  nop
        <+23>:  pop    ebp
        <+24>:  ret  

Usamos un Emulador para poder hacerlo (https://carlosrafaelgn.com.br/Asm86/)
viendo el registro EAX al final da: 0x0000C36B
```
## Bandera
0xC36B