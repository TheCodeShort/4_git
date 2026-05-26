# Comandos de Uso Frecuente (Nivel Intermedio)

### **git branch**
Sirve para: Crear un camino o línea de tiempo alterna (como un universo paralelo) en tu código para probar cosas sin dañar el proyecto original.

- **Cómo se conecta con otros:** Se enlaza con **`git checkout`** o **`git switch`**, porque primero creas ese camino alterno con branch, y luego usas checkout para ir a trabajar en él.
- **Cuándo usarlo:** Sirve para casos donde quieres probar un nuevo diseño de botones en la página web, pero no quieres romper la página principal por si algo sale mal.

---

### **git switch (o git checkout)**
Sirve para: Moverte entre los diferentes caminos o líneas de tiempo (ramas) que has creado en tu proyecto.

- **Cómo se conecta con otros:** Se enlaza con **`git merge`**, ya que te mueves a la rama principal (switch) para luego fusionarla con el trabajo de la otra rama (merge).
- **Cuándo usarlo:** Sirve para casos donde estabas trabajando en el diseño de un botón, pero tu jefe te pide arreglar urgente un texto en la página principal, entonces te "cambias" a la versión principal un momento.

---

### **git merge**
Sirve para: Combinar el trabajo que hiciste en una línea de tiempo alterna con la línea de tiempo principal, uniendo todo en un solo lugar.

- **Cómo se conecta con otros:** Se enlaza con **`git branch`**, porque es el final del ciclo: abriste una rama, trabajaste, y ahora la fusionas (merge) para terminarla.
- **Cuándo usarlo:** Sirve para casos donde ya terminaste de probar el diseño del botón nuevo, funciona perfecto, y ahora quieres que sea parte oficial de la página principal.

---

### **git clone**
Sirve para: Descargar a tu computadora un proyecto completo que ya existe en internet (como descargar una carpeta completa con toda su historia).

- **Cómo se conecta con otros:** Se enlaza con **`git pull`**, porque usas clone la primera vez que vas a trabajar en el proyecto, y luego usas pull todos los demás días para actualizar.
- **Cuándo usarlo:** Sirve para casos donde entras a un nuevo trabajo, te dan la dirección del código del proyecto y necesitas bajarlo a tu computadora para empezar a trabajar.

---

### **git log**
Sirve para: Ver el historial o el diario de todos los guardados (commits) que se han hecho en el proyecto, mostrando quién hizo qué y cuándo.

- **Cómo se conecta con otros:** Se enlaza con **`git status`**, porque status te dice el presente (qué estás haciendo ahora), mientras que log te muestra el pasado (qué se ha hecho antes).
- **Cuándo usarlo:** Sirve para casos donde alguien borró una imagen por error la semana pasada, y quieres mirar el historial para saber exactamente quién y qué día lo hizo.

---

### **git diff**
Sirve para: Mostrarte línea por línea exactamente qué palabras o códigos cambiaste dentro de un archivo antes de guardarlo.

- **Cómo se conecta con otros:** Se enlaza con **`git status`**, porque status te dice *qué* archivo cambió, pero diff te muestra *exactamente qué parte* del archivo cambió.
- **Cuándo usarlo:** Sirve para casos donde borraste algo por accidente en tu código, el programa dejó de funcionar, y quieres ver qué cambiaste en los últimos minutos.

---

### **git restore**
Sirve para: Descartar los cambios que no has guardado todavía en un archivo, devolviéndolo a como estaba la última vez que le tomaste foto.

- **Cómo se conecta con otros:** Se enlaza con **`git diff`**, porque miras qué cambiaste con diff, y si no te gusta, usas restore para deshacerlo y volver a la normalidad.
- **Cuándo usarlo:** Sirve para casos donde empezaste a borrar código para "mejorarlo", lo arruinaste todo y quieres que el archivo vuelva a como estaba ayer.

---

### **git remote**
Sirve para: Administrar las conexiones de tu proyecto con el internet, como decirle a Git a qué dirección de GitHub debe enviar las cosas.

- **Cómo se conecta con otros:** Se enlaza con **`git push`**, porque primero configuras la dirección de internet con remote, y luego envías tus archivos allí usando push.
- **Cuándo usarlo:** Sirve para casos donde creas un proyecto en tu computadora, luego creas una carpeta vacía en GitHub y necesitas conectarlos para poder subir tu código.
