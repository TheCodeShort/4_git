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
