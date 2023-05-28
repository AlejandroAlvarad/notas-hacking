## Objetivo
Can you solve this?What two positive numbers can make this possible: `n1 > n1 + n2 OR n2 > n1 + n2`Enter them here `nc saturn.picoctf.net 59859`. [Source](https://artifacts.picoctf.net/c/455/flag.c)

## Hints
- Integer overflow
- Not necessarily a math problem

## Solución

```
th0rtilla-picoctf@webshell:~$ nc saturn.picoctf.net 59859
n1 > n1 + n2 OR n2 > n1 + n2 
What two positive numbers can make this possible: 
1
2147483647
You entered 1 and 2147483647
You have an integer overflow
YOUR FLAG IS: picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_fe14e9e9}

```
## Bandera
picoCTF{Tw0_Sum_Integer_Bu773R_0v3rfl0w_fe14e9e9}