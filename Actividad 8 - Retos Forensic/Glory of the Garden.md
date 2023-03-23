## Descripción 
This [garden](https://jupiter.challenges.picoctf.org/static/d0e1ffb10fc0017c6a82c57900f3ffe3/garden.jpg) contains more than it seems.

## Hits
What is a hex editor?

## Solución
```
th0rtilla-picoctf@webshell:~/picoctf/forence/gloryofthegarfen$ strings garden.jpg -n 15
Copyright (c) 1998 Hewlett-Packard Company
sRGB IEC61966-2.1
sRGB IEC61966-2.1
IEC http://www.iec.ch
IEC http://www.iec.ch
.IEC 61966-2.1 Default RGB colour space - sRGB
.IEC 61966-2.1 Default RGB colour space - sRGB
,Reference Viewing Condition in IEC61966-2.1
,Reference Viewing Condition in IEC61966-2.1
%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz
Here is a flag "picoCTF{more_than_m33ts_the_3y3eBdBd2cc}"
```

## Bandera
picoCTF{more_than_m33ts_the_3y3eBdBd2cc}