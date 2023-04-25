## Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:63115/) and see what you can discover.

## Hints
Is there more code than what the inspector initially shows?

## Solución

Inspeccionamos la pagina y entramos a styles.css y scrip.jss
En **styles** encontramos:
```
body {
  background-color: lightblue;
}

/*  picoCTF{1nclu51v17y_1of2_  */
```
En **scrip** encontremos:
```
function greetings()
{
  alert("This code is in a separate file!");
}

//  f7w_2of2_6edef411}

```
Armando la bandera quedaria así:
***picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}***

## Bandera
picoCTF{1nclu51v17y_1of2_f7w_2of2_6edef411}