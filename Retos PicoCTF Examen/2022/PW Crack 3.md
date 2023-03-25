## Descripcion
Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag and the hash in the same directory too.
There are 7 potential passwords with 1 being correct. You can find these by examining the password checker script.

## Hits
- To view the level3.hash.bin file in the webshell, do: $ bvi level3.hash.bin
- To exit bvi type :q and press enter.
- The str_xor function does not need to be reverse engineered for this challenge.

## Solucion
```
pos_pw_list = ["f09e", "4dcf", "87ab", "dba8", "752e", "3961", "f159"]
son las posibles contraseñas fui introduciendo las contraseñas, como son solo 7 no hubo problema

Please enter correct password for flag: 87ab
Welcome back... your flag, user:
picoCTF{m45h_fl1ng1ng_cd6ed2eb}
```

## Bandera
picoCTF{m45h_fl1ng1ng_cd6ed2eb}