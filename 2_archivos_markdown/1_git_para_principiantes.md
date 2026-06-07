# Comandos Básicos (Día a Día)

### **git status**
Sirve para: Ver qué archivos has modificado, añadido o borrado, y que Git todavía no está guardando.

- **Cómo se conecta con otros:** Se enlaza con **`git add`**, porque después de ver qué cambiaste con status, usas add para seleccionar cuáles quieres guardar en el próximo paquete.
- **Cuándo usarlo:** Sirve para casos donde dejaste de trabajar ayer, vuelves hoy y no te acuerdas qué archivos estuviste tocando, así que quieres revisar antes de guardar.

---

### **git add .**
Sirve para: Agarrar todos los archivos que modificaste y meterlos en una caja imaginaria listos para ser guardados.

- **Cómo se conecta con otros:** Se enlaza con **`git commit`**, porque primero los metes en la caja (add) y luego le pones la etiqueta y sellas la caja (commit).
- **Cuándo usarlo:** Sirve para casos donde ya terminaste una pequeña tarea y quieres preparar todos esos cambios para guardarlos de una vez.

---

### **git commit -m "mensaje"**
Sirve para: Tomarle una "foto" o guardar permanentemente los archivos que habías seleccionado, poniéndoles un título corto que explique qué hiciste.

- **Cómo se conecta con otros:** Se enlaza con **`git push`**, porque después de guardar localmente varios "commits" (fotos), usas push para enviarlos todos a internet.
- **Cuándo usarlo:** Sirve para casos donde terminaste de arreglar un error en el código y quieres guardar ese progreso para que no se pierda.

### git commit --amend

sirve exactamente para **editar el último commit** y evitar crear un segundo commit por un olvido.

Modifica el **último commit** que hiciste en tu historial. En lugar de amontonar un nuevo commit que diga "arreglo de error" o "me faltó un archivo", este comando "abre" el último commit, le mete los nuevos cambios y lo vuelve a cerrar. El historial queda limpio, como si nunca te hubieras equivocado.

- **Lo que hace:** Mete los archivos nuevos al último commit y **asume que quieres cambiar o mejorar el mensaje anterior**.
- **El flujo:** Le das Enter y Git **congela la terminal**. Te abre una pantalla negra (un editor de texto) y te obliga a revisar el mensaje. No te dejará continuar trabajando hasta que guardes o cierres ese editor.
### git commit --amend -m "nuevo mensaje"

con este podemos aprovechar a editar el mensaje 

### git commit --amend --no-edit

_Agregar `--no-edit` sirve para que Git reutilice el mismo mensaje que ya tenía el commit anterior, ahorrándote el paso de abrir el editor de texto._
- **Lo que hace:** Mete los archivos nuevos al último commit y **asume que el mensaje actual ya está bien**.
- **El flujo:** Le das Enter, Git hace el cambio en un milisegundo y tú sigues trabajando. Nadie te interrumpe.
---

### **git push**
Sirve para: Enviar todos los cambios que ya guardaste en tu computadora hacia la nube (como GitHub) para que otros puedan verlos.

- **Cómo se conecta con otros:** Se enlaza con **`git pull`**, porque mientras push envía tus cosas, pull es lo opuesto y descarga las cosas que los demás enviaron.
- **Cuándo usarlo:** Sirve para casos donde terminaste tu trabajo del día y quieres subirlo a internet para que tu equipo pueda revisarlo o descargarlo.

---

### **git pull**
Sirve para: Descargar los últimos cambios que hay en internet y mezclarlos automáticamente con tus archivos en tu computadora.

- **Cómo se conecta con otros:** Se enlaza con **`git clone`**, ya que clone descarga todo por primera vez, pero pull solo descarga lo nuevo que haya cambiado desde la última vez que revisaste.
- **Cuándo usarlo:** Sirve para casos donde llegas en la mañana y quieres asegurarte de tener el código más actualizado que tus compañeros programaron la noche anterior.

---

### **git init**
Sirve para: Crear un repositorio nuevo desde cero en tu computadora, convirtiendo una carpeta normal en una carpeta mágica que Git puede vigilar.

- **Cómo se conecta con otros:** Se enlaza con **`git add`**, porque después de inicializar la carpeta (init), empiezas a añadir (add) los archivos que quieres guardar.
- **Cuándo usarlo:** Sirve para casos donde empiezas un proyecto totalmente nuevo en tu computadora y quieres que Git comience a llevar el registro desde el día uno.

### git remote add url

- **`git remote add`**: Le dice a Git que vas a gestionar los servidores remotos (la nube) que están vinculados a tu carpeta local.

- `url` aca no va la palabra url sino el link tener presente que el link puede ser HTTPS o SSH esto cambia  


### git remote set-url origin git@github.com:TheCodeShort/nombre-de-tu-repositorio.git

- si el link que se copio para el repo no es o nos equivocamos se puede cambiar de esa manera tener presente que se puede cambiar a HTTPS o SSH los link o url cambian 

- **`git remote`**: Le dice a Git que vas a gestionar los servidores remotos (la nube) que están vinculados a tu carpeta local.
- **`set-url origin`**: Le ordena a Git: _"Borra la dirección de internet que tenías guardada bajo el nombre 'origin' y reemplázala por una nueva"_. (`origin` es simplemente el nombre estándar que Git le da a tu repositorio principal en la nube).
- **`git@github.com:...`**: Es la nueva dirección, pero ahora con el formato **SSH** que utiliza tus llaves de seguridad en lugar de contraseñas.


### git remote -v
- con esto podemos ver los link que están vinculados al repositorio y ver si es SSH o HTTPS 
---

### **git rm**
Sirve para: Borrar un archivo de tu computadora y avisarle a Git al mismo tiempo que ya no quieres que lo siga vigilando.

- **Cómo se conecta con otros:** Se enlaza con **`git commit`**, porque después de decirle a Git que borre el archivo, necesitas guardar ese cambio (commit) para que sea oficial.
- **Cuándo usarlo:** Sirve para casos donde te das cuenta de que creaste un archivo por error y quieres eliminarlo completamente del proyecto.

---

### **git mv**
Sirve para: Cambiarle el nombre a un archivo o moverlo a otra carpeta, y que Git entienda qué fue lo que pasó en lugar de pensar que lo borraste.

- **Cómo se conecta con otros:** Se enlaza con **`git commit`**, porque mover el archivo es un cambio que debes guardar formalmente.
- **Cuándo usarlo:** Sirve para casos donde escribiste mal el nombre de un archivo (como "indxe.html") y quieres corregirlo ("index.html") sin confundir a Git.

---
# nano .gitignore

- **¿Qué hace?**: `nano` es un editor de texto que viene integrado en la terminal de Linux (como el Bloc de Notas de Windows, pero sin ventanas). `.gitignore` es el nombre del archivo.
- **En la práctica**: Al ejecutarlo, tu terminal se convertirá en una pantalla negra para escribir. Solo debes escribir dentro la ruta `.obsidian/workspace.json`. Esto crea el archivo físicamente en la carpeta que me muestras.

2. Guardar y salir en Nano (`Ctrl + O`, `Enter`, `Ctrl + X`)

- **¿Qué hace?**: Como Nano no tiene botones de "Archivo -> Guardar", usas el teclado.
    - `Ctrl + O` significa "Escribir el archivo" (Guardar).
    - `Enter` confirma que mantienes el nombre `.gitignore`.
    - `Ctrl + X` significa "Salir" para cerrar el editor y volver a tu terminal normal.

# echo ".obsidian/workspace.json" >> .gitignore

- es parecido a nano cambia es la manera en crear el archivo este es mas automático y nano se habré una ventana y toca poner comando para guardar 