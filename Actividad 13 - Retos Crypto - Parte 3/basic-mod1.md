## Objetivo
We found this weird message being passed around on the servers, we think we have a working decryption scheme.Download the message [here](https://artifacts.picoctf.net/c/128/message.txt).Take each number mod 37 and map it to the following character set: 0-25 is the alphabet (uppercase), 26-35 are the decimal digits, and 36 is an underscore.Wrap your decrypted message in the picoCTF flag format (i.e. `picoCTF{decrypted_message}`)

## Hints
- Do you know what `mod 37` means?
- `mod 37` means modulo 37. It gives the remainder of a number after being divided by 37.

## Solución
Ocupamos la pagina [decode](https://www.dcode.fr/modulo-cipher) en modulo N en 37 y usamos la decodificación con mas sentido

## Bandera
picoCTF{R0UND_N_R0UND_B6B25531}