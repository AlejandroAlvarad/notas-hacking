## Descripcion
Run the Python script and convert the given number from decimal to binary to get the flag.
Download Python script

## Hits
- Look up a decimal to binary number conversion app on the web or use your computer's calculator!
- The str_xor function does not need to be reverse engineered for this challenge.
- If you have Python on your computer, you can download the script normally and run it. Otherwise, use the wget command in the webshell.
- To use wget in the webshell, first right click on the download link and select 'Copy Link' or 'Copy Link Address'
- Type everything after the dollar sign in the webshell: $ wget , then paste the link after the space after wget and press enter. This will download the script for you in the webshell so you can run it!
- Finally, to run the script, type everything after the dollar sign and then press enter: $ python3 convertme.py 


## Solucion
```
th0rtilla-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/24/convertme.py
--2023-03-21 00:50:02--  https://artifacts.picoctf.net/c/24/convertme.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.42, 108.156.172.120, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1189 (1.2K) [application/octet-stream]
Saving to: 'convertme.py'

convertme.py        100%[==================>]   1.16K  --.-KB/s    in 0s      

2023-03-21 00:50:02 (61.1 MB/s) - 'convertme.py' saved [1189/1189]

th0rtilla-picoctf@webshell:~$ python3 convertme.py
If 12 is in decimal base, what is it in binary base?
Answer: 1100
That is correct! Here's your flag: picoCTF{4ll_y0ur_b4535_722f6b39}
th0rtilla-picoctf@webshell:~$ 
```

## Bandera
picoCTF{4ll_y0ur_b4535_722f6b39}