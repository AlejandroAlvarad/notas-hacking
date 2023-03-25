## Descripcion
Can you crack the password to get the flag?
Download the password checker here and you'll need the encrypted flag in the same directory too.

## Hits
- To view the file in the webshell, do: $ nano level1.py
- To exit nano, press Ctrl and x and follow the on-screen prompts.
- The str_xor function does not need to be reverse engineered for this challenge.

## Solucion

```
th0rtilla-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: asw
That password is incorrect
th0rtilla-picoctf@webshell:~$ nano level1.py
### THIS FUNCTION WILL NOT HELP YOU FIND THE FLAG --LT ########################
def str_xor(secret, key):
    #extend key to secret length
    new_key = key
    i = 0
    while len(new_key) < len(secret):
        new_key = new_key + key[i]
        i = (i + 1) % len(key)        
    return "".join([chr(ord(secret_c) ^ ord(new_key_c)) for (secret_c,new_key_>
###############################################################################


flag_enc = open('level1.flag.txt.enc', 'rb').read()



def level_1_pw_check():
    user_pw = input("Please enter correct password for flag: ")
    if( user_pw == "1e1a"):
        print("Welcome back... your flag, user:")
        decryption = str_xor(flag_enc.decode(), user_pw)
        print(decryption)
        return
    print("That password is incorrect")



level_1_pw_check()
podemos ver que la contraseña es 1e1a
th0rtilla-picoctf@webshell:~$ python3 level1.py
Please enter correct password for flag: 1e1a
Welcome back... your flag, user:
picoCTF{545h_r1ng1ng_fa343060}
th0rtilla-picoctf@webshell:~$ 
```

## Bandera
picoCTF{545h_r1ng1ng_fa343060}
