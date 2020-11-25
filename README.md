Clonamos el repositorio en ambas carpetas.

Hacemos un cambio en casa y otro en instituto.

Subimos le cambio en casa.

Sin hacer pull subimos el cambio en instituto y nos da este error:

To https://github.com/migangal4/PracticaErrores.git
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'https://github.com/migangal4/PracticaErrores
.git'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

Solucionamos esto haciendo "pull" antes de subir lo de instituto

Nos da un error:

error: Pulling is not possible because you have unmerged files.
hint: Fix them up in the work tree, and then use 'git add/rm <file>'
hint: as appropriate to mark resolution and make a commit.
fatal: Exiting because of an unresolved conflict.

Que solucionamos entrando en el archivo y seleccionando la version que queremos

<<<<<<< HEAD
		system.out.println("hola");

=======
		system.out.println("adios");
>>>>>>> 8f4c717c4e62e33130f18305fdfb43246da81ab0

Luego hacemos add y commit antes de hacer pull

Volvemos a hacer cambios y volvemos a subirlos de la misma manera, dandonos el mismo error. Lo solucionamos haciendo el mismo proceso de nuevo de nuevo

Una vez mas hacemos los cambios que nos pide el enunciado y una vez mas nos da un error por no haber hecho "pull" antes de subir los cambios

Volvemos a solucionarlo haciendo el mismo proceso antes de aplicar y subir los cambios para que la carpeta este en la ultima version al subir el cambio realizado

Esta vez nos da un error al hacer pull que solucionamos eliminando el fichero java de CarpetaInstituto y volvemos a hacer add, commit y pull


PRACTICA 4

Tras clonar de nuevo el repositorio 

Creamos una ligth tag haciendo

git tag v0.1 "direccionDelPrimerCommit"

Mandamos esa tag a git hub haciendo

git push origin v0.1 (aunque podriamos haber usado --tag tambien)

Despues vamos a el primer commit usando la tag  haciendo

git checkout v0.1

Ahi realizamos un cambio en el archivo Main de java

Hacemos add y commit y lo unico que nos sale es


$ git commit -m "commit añadiendo una frase"
[detached HEAD 4375517] commit añadiendo una frase
 1 file changed, 1 insertion(+)


Pero al volver al ultimo commit haciendo 

git checkout master

Nos avisa git de:

Warning: you are leaving 1 commit behind, not connected to
any of your branches:

  4375517 commit añadiendo una frase

If you want to keep it by creating a new branch, this may be a good time
to do so with:

 git branch <new-branch-name> 4375517

Switched to branch 'master'
Your branch is up to date with 'origin/master'.

Basicamente nos dice que si queremos mantener ese commit lo que tenemos que hacer es hacer una rama nueva, ya que no puedes hacer un commit en una version pasada que afecte a la actual.

Despues en la carpeta instituto hacemos un 

git pull 

Para obtener las tags y hacemos 

git checkout v0.1

Para ir a la primera version en esa carpeta




PRACTICA 5

Hacemos una nueva rama con 

git branch NuevaRama

Cambiamos a esa rama haciendo 

git checkout NuevaRama

Hacemos cambios en esta rama

Hacemos add, commit  y push

Siendo el push 

git push origin NuevaRama

Volvemos a la rama anterior haciendo 

git checkout master

Hacemos cambios alli y hacemos de nuevo add, commit y push.

Vamos ahora a la carpeta instituto

Hacemos pull

Ahora nos saldra que solo tenemos la rama master

(aqui intento hacer git pull NuevaRama haciendo que se me intenten unir ambas ramas, elimino la parte de la rama NuevaRama quedandome con la parte de la rama master para resolver el conflicto, pero esto hara que posteriormente  las considere como unidas ya ambas ramas)

Realmente tenemos las otras ramas tambien solo tenemos que hacer

git checkout NuevaRama

Para que se nos active la rama NuevaRama

Ahora despues de comprobar los cambios en las ramas, volvemos a la rama master

Hacemos

git merge NuevaRama

Pero al haberlo hecho ya antes nos dice que ya lo hemos hecho por lo que no hacemos nada nuevo.