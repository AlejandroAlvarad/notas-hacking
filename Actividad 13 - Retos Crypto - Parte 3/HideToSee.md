## Objetivo
How about some hide and seek heh?Look at this image [here](https://artifacts.picoctf.net/c/241/atbash.jpg).

## Hints
Download the image and try to extract it

## Solución

```
th0rtilla-picoctf@webshell:~/HideToSee$ steghide extract -sf atbash.jpg
Enter passphrase: 
wrote extracted data to "encrypted.txt".
th0rtilla-picoctf@webshell:~/HideToSee$ cat encrypted.txt
krxlXGU{zgyzhs_xizxp_7142uwv9}
th0rtilla-picoctf@webshell:~/HideToSee$ 
```
## Bandera
picoCTF{atbash_crack_7142fde9}