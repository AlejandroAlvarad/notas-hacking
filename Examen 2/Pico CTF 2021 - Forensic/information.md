## Objetivo
Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/c28a959c5605d5f67480d5dd3a77f302/cat.jpg)

## Hints
- Look at the details of the file
- Make sure to submit the flag as picoCTF{XXXXX}

## Solución

Descargamos la imagen e intentemos ver la descripcion
```
th0rtilla-picoctf@webshell:~/information$ binwalk cat.jpg

DECIMAL       HEXADECIMAL     DESCRIPTION
--------------------------------------------------------------------------------
0             0x0             JPEG image data, JFIF standard 1.02

th0rtilla-picoctf@webshell:~/information$ strings cat.jpg | grep picoCTF{*
```

Entramos a hexedit para ver que podiamos encontrar y una linea que parece interesante es: **cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9** , parece ser base 64, lo intentamos traducir
```
th0rtilla-picoctf@webshell:~/information$ echo cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9 | base64 -d
picoCTF{the_m3tadata_1s_modified}
th0rtilla-picoctf@webshell:~/information$ 
```
## Bandera
picoCTF{the_m3tadata_1s_modified}