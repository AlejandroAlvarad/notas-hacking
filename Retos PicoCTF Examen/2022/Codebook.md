## Descripcion
Run the Python script code.py in the same directory as codebook.txt.
Download code.py
Download codebook.txt

## Hits
- On the webshell, use ls to see if both files are in the directory you are in
- The str_xor function does not need to be reverse engineered for this challenge.

## Solucion
```
th0rtilla-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/code.py
--2023-03-21 00:56:21--  https://artifacts.picoctf.net/c/1/code.py
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 18.160.41.121, 18.160.41.85, 18.160.41.113, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|18.160.41.121|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1278 (1.2K) [application/octet-stream]
Saving to: 'code.py'

code.py             100%[==================>]   1.25K  --.-KB/s    in 0s      

2023-03-21 00:56:21 (743 MB/s) - 'code.py' saved [1278/1278]

th0rtilla-picoctf@webshell:~$ wget https://artifacts.picoctf.net/c/1/codebook.txt
--2023-03-21 00:56:37--  https://artifacts.picoctf.net/c/1/codebook.txt
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 108.156.172.74, 108.156.172.6, 108.156.172.42, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|108.156.172.74|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 27 [application/octet-stream]
Saving to: 'codebook.txt'

codebook.txt        100%[==================>]      27  --.-KB/s    in 0s      

2023-03-21 00:56:37 (1.50 MB/s) - 'codebook.txt' saved [27/27]

th0rtilla-picoctf@webshell:~$ ls
README.txt  code.py  codebook.txt  convertme.py  flag  pico  picoCTF  runme.py
th0rtilla-picoctf@webshell:~$ python3 code.py
picoCTF{c0d3b00k_455157_d9aa2df2}
```

## Bandera
picoCTF{c0d3b00k_455157_d9aa2df2}