## Objetivo
The developer of this website mistakenly left an important artifact in the website source, can you find it?The website is [here](http://saturn.picoctf.net:53295/)

## Hints
How could you mirror the website on your local machine so you could use more powerful tools for searching?

## Solución
Inspeccionamos la pagina y en el apartado CSS nos vamos al style.css y en la linea 328 encontramos la bandera
```
 .navbar-expand-md .navbar-nav .nav-link {
     padding: 15px 48px;
     font-size: 16px;
     color: #000;
     line-height: 18px;
}
/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7} **/
 .carousel-indicators li {
     width: 20px;
     height: 20px;
     border-radius: 11px;
     background-color: #070000;
}
```
## Bandera
picoCTF{1nsp3ti0n_0f_w3bpag3s_8de925a7}