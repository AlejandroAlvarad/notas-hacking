## Objetivo
Can you get the flag?Here's the [website](http://saturn.picoctf.net:52021/).We know that the website files live in `/usr/share/nginx/html/` and the flag is at `/flag.txt` but the website is filtering absolute file paths. Can you get past the filter to read the flag?

## Hints

## Solución
Este sitio web tiene la característica útil de leer cualquier archivo que queramos también, dada su ruta. Con las rutas de archivo, un ./ anterior significa el directorio actual y ../ significa el directorio adjunto. Como sabemos que estamos en /usr/share/nginx/html/ y queremos acceder a /flag.txt, podemos usar la ruta ../../../../flag.txt para leer el bandera

## Bandera
picoCTF{7h3_p47h_70_5ucc355_e5fe3d4d}