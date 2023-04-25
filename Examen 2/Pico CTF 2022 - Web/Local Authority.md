## Objetivo
Can you get the flag?Go to this [website](http://saturn.picoctf.net:64710/) and see what you can discover.

## Hints
How is the password checked on this website?

## Solución
Entramos a la pagina y nos pide un usuario y una contraseña y pones cualquier cosa, nos manda a un apagina con el mensaje de **Log in Fail**
Inspeccionamos esa pagina y encontramos un archivo **secure.js** y encontramos esto
```
function checkPassword(username, password)
{
  if( username === 'admin' && password === 'strongPassword098765' )
  {
    return true;
  }
  else
  {
    return false;
  }
}
```

Dandonos cuenta que  el **Usuario: admin** y **Password:strongPassword098765** regresamos y ahora ponemos este usuario y contraseña.
Entramos y nos da la bandera
## Bandera
