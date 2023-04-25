## Objetivo
The flag is somewhere on this web application not necessarily on the website. Find it.Check [this](http://saturn.picoctf.net:55771/) out.

## Hints


## Solución
No encontramos nada en los archivos entonces modificamos la url y añadimos **/robots.txt** el cual sale lo siguiente
```
User-agent *
Disallow: /cgi-bin/
Think you have seen your flag or want to keep looking.

ZmxhZzEudHh0;anMvbXlmaW
anMvbXlmaWxlLnR4dA==
svssshjweuiwl;oiho.bsvdaslejg
Disallow: /wp-admin/
```

Nos damos cuenta que **anMvbXlmaWxlLnR4dA** esta en base 64, nos vamos a cyber chef y nos da **js/myfile.txt** , entonces lo modificamos el url y ponemos lo que nos dio y nos sale la bandera

## Bandera
picoCTF{Who_D03sN7_L1k5_90B0T5_22ce1f22}