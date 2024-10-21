# Repositorio Ejercicio-git-Libro

## Paso 1

Crear repositorio y clonarlo en el repositorio local

```code
bae2@jpexposito-VirtualBox:~/Documentos$ git clone https://github.com/GabrielHerreraGanzo/ejercicio-git-libro.git
Clonando en 'ejercicio-git-libro'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Total 3 (delta 0), reused 0 (delta 0), pack-reused 0 (from 0)
Recibiendo objetos: 100% (3/3), listo.
bae2@jpexposito-VirtualBox:~/Documentos$ cd ejercicio-git-libro/
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ ls la
ls: no se puede acceder a 'la': No existe el archivo o el directorio
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ ls -la
total 16
drwxrwxr-x 3 bae2 bae2 4096 oct 18 15:53 .
drwxr-xr-x 7 bae2 bae2 4096 oct 18 15:53 ..
drwxrwxr-x 8 bae2 bae2 4096 oct 18 15:53 .git
-rw-rw-r-- 1 bae2 bae2   21 oct 18 15:53 README.md
```

## Paso 2

Muestro el historial de cambios del repositorio.

```code
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git log
commit ead363ae20d7ebb84c238a63e8ce02204c110e74 (HEAD -> main, origin/main, origin/HEAD)
Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
Date:   Fri Oct 18 15:57:54 2024 +0100

    Creación y clonación del repositorio

commit 3238bae1ba6c36b4ff205e91da61614075998ba0
Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
Date:   Thu Oct 10 18:02:53 2024 +0100

    Initial commit
```

Creo la carpeta capitulos: ```mkdir capitulos``` y creo el fichero capitulo1.txt y ecribo dentro de este un mensaje utilizando ```cat > capitulos/capitulo1.txt```

Por último, añado los cambios a la zona de intercambio temporal(git add), hago un commit de los cambios con el mensaje "Añadido capítulo 1" y vuelvo a mostrar el historial de cambios del repositorio(git log con las opciones).

```code
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro/capitulos$ git add .
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro/capitulos$ git commit -m "Añadido capítulo 1."
[main 8b0899f] Añadido capítulo 1.
 1 file changed, 5 insertions(+)
 create mode 100644 capitulos/capitulo1.txt
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro/capitulos$ git log
commit 8b0899fd4a3d06df2203fe2d308393a4c7522282 (HEAD -> main)
Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
Date:   Mon Oct 21 15:00:33 2024 +0100

    Añadido capítulo 1.

commit ead363ae20d7ebb84c238a63e8ce02204c110e74 (origin/main, origin/HEAD)
Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
Date:   Fri Oct 18 15:57:54 2024 +0100

    Creación y clonación del repositorio

commit 3238bae1ba6c36b4ff205e91da61614075998ba0
Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
Date:   Thu Oct 10 18:02:53 2024 +0100

    Initial commit
```

## Paso 3

Creo el fichero capitulo2.txt con el comando: ```cat > capitulos/capitulo2.txt``` y añado un texto.

Añado los cambios a la zona de intercambio temporal(git add), hago un commit de los cambios con el mensaje "Añadido capítulo 2" y muestro las diferencias entre la última versión y dos versiones anteriores.

```code
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git add .
git commit -m "Añadido capítulo 2."
[main e4cd974] Añadido capítulo 2.
 1 file changed, 4 insertions(+)
 create mode 100644 capitulos/capitulo2.txt
bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git diff HEAD~2..HEAD              
diff --git a/README.md b/README.md
index 6fb2fe6..6ddf7fd 100644
--- a/README.md
+++ b/README.md
@@ -24,3 +24,51 @@ drwxrwxr-x 8 bae2 bae2 4096 oct 18 15:53 .git
 
 # Paso 2
 
+Muestro el historial de cambios del repositorio.
+
+```code
+bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro$ git log
+commit ead363ae20d7ebb84c238a63e8ce02204c110e74 (HEAD -> main, origin/main, origin/HEAD)
+Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
+Date:   Fri Oct 18 15:57:54 2024 +0100
+
+    Creación y clonación del repositorio
+
+commit 3238bae1ba6c36b4ff205e91da61614075998ba0
+Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
+Date:   Thu Oct 10 18:02:53 2024 +0100
+
+    Initial commit
+```
+
+Creo la carpeta capitulos: ```mkdir capitulos``` y creo el fichero capitulo1.txt y ecribo dentro de este un mensaje utilizando ```cat > capitulos/capitulo1.txt```
+
+Por último, añado los cambios a la zona de intercambio temporal(git add), hago un commit de los cambios con el mensaje "Añadido capítulo 1" y vuelvo a mostrar el historial de cambios del repositorio(git log con las opciones).
+
+```code
+bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro/capitulos$ git add .
+bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro/capitulos$ git commit -m "Añadido capítulo 1."
+[main 8b0899f] Añadido capítulo 1.
+ 1 file changed, 5 insertions(+)
+ create mode 100644 capitulos/capitulo1.txt
+bae2@jpexposito-VirtualBox:~/Documentos/ejercicio-git-libro/capitulos$ git log
+commit 8b0899fd4a3d06df2203fe2d308393a4c7522282 (HEAD -> main)
+Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
+Date:   Mon Oct 21 15:00:33 2024 +0100
+
+    Añadido capítulo 1.
+
+commit ead363ae20d7ebb84c238a63e8ce02204c110e74 (origin/main, origin/HEAD)
+Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
+Date:   Fri Oct 18 15:57:54 2024 +0100
+
+    Creación y clonación del repositorio
+
+commit 3238bae1ba6c36b4ff205e91da61614075998ba0
+Author: GabrielHerreraGanzo <gabrielingo112006@gmail.com>
+Date:   Thu Oct 10 18:02:53 2024 +0100
+
+    Initial commit
+```
+
+
diff --git a/capitulos/capitulo2.txt b/capitulos/capitulo2.txt
new file mode 100644
index 0000000..7968eb0
--- /dev/null
+++ b/capitulos/capitulo2.txt
@@ -0,0 +1,4 @@
+ El flujo de trabajo básico con Git consiste en:
+  1- Hacer cambios en el repositorio.
+  2- Añadir los cambios a la zona de intercambio temporal.
+  3- Hacer un commit de los cambios.
\ No newline at end of file
```

## Paso 4

Creo el fichero capitulo3.txt en la carpeta capítulos y le añado un texto.

Añado los cambios a la zona de intercambio temporal(git add), hago un commit de los cambios con el mensaje "Añadido capítulo 3" y muestro las diferencias entre la primera versión y la última version.

```code

```

