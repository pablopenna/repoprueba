Ej1.
* Instalar git y registrarse: hecho
* Crear repo: hecho
* Conectalo con repo en local:
    
    Para descargar el repo que has creado en local
    ```
    git clone <URL del repo>
    ```
    ejemplo:
    ```
    git clone https://github.com/pablopenna/repoprueba
    ```
    Este comando crea una carpeta con el contenido del repo.

* Crea una rama y escribe texto random en el README. Commitea los cambios y subelos a github de nuevo en una rama.

    Para hacer esta tarea, primero crearemos la rama en local, haremos los cambios y despúes mandaremos los cambios junto con la nueva rama a nuestro repo.

    Los repos cuando son creados empiezan con una sola rama, que es la principal. Esta, por defecto, se llama `master`

    1. Crear rama en local: Con el comando `git branch <nombre_rama>` crearemos una nueva rama. Por ejemplo:
    ```
    git branch ramaB
    ```

    Para comprobar las ramas de las que disponemos y en la que estamos usamos `git branch` a secas. La rama actual se marca con un asterisco (`*`).

    Para cambiar a la nueva rama:
    ```
    git checkout ramaB
    ```

    Con esto ya estamos en la nueva rama, los cambios que hagamos ahora se harán en esta y no en la princiapl.

    A continuación, cambiar el texto en el README. Yo simplemente he borrado todo y he escrito "random".

    Añadimos el README con git add para commitear sus cambios

    ```
    git add README.md
    ```

    Creamos el commit de nuestra rama B 

    ```
    git commit -m "Commit de la rama B"
    ```

    Y aquí la parte clave, en lugar de enviar el commit a nuestra rama principal con 

    ```
    git push origin master
    ```

    lo enviamos a la nueva rama 

    ```
    git push -u origin ramaB
    ```

    Para comprobar los commits de nuetro repo y sus diferentes ramas:

    * Rama master: https://github.com/pablopenna/repoprueba/commits/master

    * Rama ramaB: https://github.com/pablopenna/repoprueba/commits/ramaB

* Mergea la rama en master.

Mergear ramas no se puede hacer directamente en el repo. Para ello, tendremos que hacer primer un merge en nuestro repo local (en nuestro PC) y después enviar el resultado de la operación al repo.

En nuestro caso, si queremos incorporar los cambios de nuestra ramaB en nuestra rama principal "master".

* Posicionarnos en la rama master
```
git checkout master
```
* Mergear la ramaB en master
```
git merge ramaB
```
Esto lo que hace es incorporar el/los commits extra de la ramaB en master.

* Enviar cambios al repo

```
git push origin master
```

Con esto, si comprobamos los commits de nuestro repo, el commit que hicimos en la ramaB debería figurar ahora también en nuestra rama master.




    Fuentes:
    * [Ramas en git](https://www.toolsqa.com/git/git-create-branch/)
    * [Hacer merge de dos ramas](https://stackoverflow.com/questions/23336221/how-to-merge-one-remote-branch-into-another-remote-branch)

