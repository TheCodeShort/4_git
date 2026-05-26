# Comandos Menos Usados (Avanzados)

### **git stash**
Sirve para: Guardar rápidamente en un "bolsillo temporal" lo que estás haciendo, sin crear un guardado oficial (commit), para que puedas dejar tu área de trabajo limpia por un momento.

- **Cómo se conecta con otros:** Se enlaza con **`git switch`**, porque guardas tus cosas en el bolsillo (stash), te cambias de rama (switch) para hacer algo urgente, y luego regresas y sacas tus cosas del bolsillo.
- **Cuándo usarlo:** Sirve para casos donde estás a mitad de arreglar algo complejo, no has terminado, pero necesitas revisar la rama principal por un momento y no quieres perder tu progreso ni crear un guardado a medias.

---

### **git rebase**
Sirve para: Tomar los cambios que hiciste en tu camino (rama) y reescribir la historia para que parezca que los hiciste hoy mismo sobre la versión más nueva de la rama principal.

- **Cómo se conecta con otros:** Se enlaza con **`git merge`**, ya que ambos combinan ramas, pero rebase deja el historial más limpio y recto, como si todo se hubiera hecho en orden.
- **Cuándo usarlo:** Sirve para casos donde tu rama quedó muy desactualizada comparada con la principal, y quieres que tu trabajo se ordene como si apenas lo acabaras de empezar con la última versión.

---

### **git reset**
Sirve para: Echar el tiempo hacia atrás, borrando o deshaciendo guardados (commits) que ya habías hecho, regresando el proyecto a como estaba en el pasado.

- **Cómo se conecta con otros:** Se enlaza con **`git log`**, porque primero miras el historial (log) para encontrar el código de la "foto" exacta a la que quieres regresar, y luego usas reset para viajar hasta allí.
- **Cuándo usarlo:** Sirve para casos donde te das cuenta de que el último guardado que hiciste rompió toda la aplicación, y prefieres borrarlo por completo y regresar a la versión anterior que sí funcionaba.

---

### **git fetch**
Sirve para: Ir a internet (GitHub) y preguntar "Oigan, ¿hay cambios nuevos?", descargando la información pero sin tocar ni mezclar tus archivos actuales.

- **Cómo se conecta con otros:** Se enlaza con **`git pull`**, porque pull hace un fetch (descarga) y un merge (mezcla) al mismo tiempo, mientras que fetch solo descarga pero no altera tu trabajo.
- **Cuándo usarlo:** Sirve para casos donde sabes que tus compañeros subieron cambios, quieres ver qué subieron, pero no quieres que eso interfiera con el archivo que estás escribiendo en este momento.

---

### **git cherry-pick**
Sirve para: Seleccionar "con pinzas" un solo guardado (commit) específico de otra rama y copiarlo exactamente en la rama donde estás ahora.

- **Cómo se conecta con otros:** Se enlaza con **`git log`**, porque necesitas mirar el historial de la otra rama para encontrar el código exacto de la "cereza" (el commit) que quieres agarrar.
- **Cuándo usarlo:** Sirve para casos donde un compañero arregló un error muy molesto en su rama y guardó ese arreglo, y tú quieres llevar solo ese arreglo específico a tu rama sin traerte todo el resto de su trabajo.

---

### **git tag**
Sirve para: Ponerle una etiqueta especial e inamovible a un guardado (commit) importante, como decir "Esta es la Versión 1.0 oficial".

- **Cómo se conecta con otros:** Se enlaza con **`git log`**, porque miras el historial para elegir el momento perfecto y le pones una etiqueta (tag) para no olvidarlo nunca.
- **Cuándo usarlo:** Sirve para casos donde tu aplicación por fin está lista para salir al público y quieres marcar ese momento exacto en la historia para encontrarlo fácil después.

---

### **git revert**
Sirve para: Crear un guardado (commit) nuevo que hace exactamente lo contrario de un guardado anterior, "deshaciendo" un error pero dejando el historial intacto.

- **Cómo se conecta con otros:** Se enlaza con **`git reset`**, pero mientras reset "borra" la historia para volver atrás, revert crea nueva historia deshaciendo el error de forma segura.
- **Cuándo usarlo:** Sirve para casos donde subiste un error a internet, tus compañeros ya descargaron el código, y necesitas arreglarlo sin arruinarles la historia a ellos.

---

### **git bisect**
Sirve para: Ayudarte a encontrar automáticamente en qué momento exacto de la historia se metió un error (bug) usando una búsqueda rápida.

- **Cómo se conecta con otros:** Se enlaza con **`git log`**, porque en vez de leer cientos de mensajes de historial buscando el error manualmente, bisect te ayuda a encontrarlo como un detective.
- **Cuándo usarlo:** Sirve para casos donde tu juego funcionaba bien hace una semana, hoy ya no funciona, y tienes 50 cambios intermedios y no sabes cuál de ellos rompió el juego.
