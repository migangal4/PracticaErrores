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