# Práctica del curso de git, gitHub y Sourcetree

## Ejercicio 1

Se deberá crear un repositorio y realizar una serie de operaciones desde la consola de comandos sobre el mismo para posteriormente subir el repositorio a Github.

Se deberá entregar a través del formulario de prácticas indicando la URL del repositorio.  En el repositorio, deberá existir un archivo readme.md con las respuestas a las siguientes preguntas:

* ¿Qué comando utilizaste en el paso 11? ¿Por qué?

`git reset --hard HEAD~1`

Porque necesito que head deje de apuntar al último commit de la rama actual y apunte al commit inmediatamente anterior.  Para ello ejecuto el comando `git reset HEAD~1`.  Con el parametro `--hard` le indico que al deshacer el commit no quiero mantener en el working copy los cambios realizados.

* Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

```
git reflog
git reset --hard 9a4d65b
git log --graph --decorate --pretty=oneline --abbrev-commit
```

1. Dado que al ejecutar `git log` el commit deshecho ya no nos aparece en el grafo de la rama actual, ejecuto `git reflog` para ver los commits por los que ha pasado el puntero `HEAD` y buscar el id del commit a rehacer.

2. Reapunto `HEAD` al identificador del commit deshecho con modo `--hard` para que me modifique el working copy.

3. Miro el estado actual del grafo de la rama styled.


* El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

No, porque la rama styled ya contiene los commits de la rama master, está actualizada.

* El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si hay conflicto, debido a que la rama htmlify contiene también el fichero git-nuestro.md al igual que la rama styled, y ambas ramas tienen contenido diferente en las mismas lineas de codigo.

* El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, porque al incorporar la rama styled en master, `HEAD`deja de apuntar al último commit de master y pasa a apuntar al último commit de la rama styled, absorbiendo asi desde master los commits de styled que no contenía con un merge fast forward.

* ¿Qué comando o comandos utilizaste en el paso 25?

`git log --graph --decorate --pretty=oneline --abbrev-commit`

* El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Si, porque si hiciese un merge fast forward el puntero `HEAD` que antes del merge apunta a master, pasaría a apuntar a title y no habría perdida de commits en dicha incorporación.

* ¿Qué comando o comandos utilizaste en el paso 27?

`git reset HEAD~1`

* ¿Qué comando o comandos utilizaste en el paso 28?

`git checkout -- git-nuestro.md`

* ¿Qué comando o comandos utilizaste en el paso 29?

`git branch -D title`

* ¿Qué comando o comandos utilizaste en el paso 30?

```
git reflog
git reset --hard c4168b0
```

<Commit> is the SHA of the commit where the merge was done.

* ¿Qué comando o comandos usaste en el paso 32?

```
git log --graph --decorate --pretty=oneline --abbrev-commit
git reset --hard 1322c1e 
```

* ¿Qué comando o comandos usaste en el punto 33?

```
git reflog
git reset --hard c4168b0
```