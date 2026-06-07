# Comandos de Uso Frecuente (Nivel Intermedio)

### **git branch nombre-de-tu-rama**
Sirve para: Crear un camino o línea de tiempo alterna (como un universo paralelo) en tu código para probar cosas sin dañar el proyecto original.

- **Cómo se conecta con otros:** Se enlaza con **`git checkout`** o **`git switch`**, porque primero creas ese camino alterno con branch, y luego usas checkout para ir a trabajar en él.
- **Cuándo usarlo:** Sirve para casos donde quieres probar un nuevo diseño de botones en la página web, pero no quieres romper la página principal por si algo sale mal.

---

### **git switch (o git checkout)**
Sirve para: Moverte entre los diferentes caminos o líneas de tiempo (ramas) que has creado en tu proyecto.

- **Cómo se conecta con otros:** Se enlaza con **`git merge`**, ya que te mueves a la rama principal (switch) para luego fusionarla con el trabajo de la otra rama (merge).
- **Cuándo usarlo:** Sirve para casos donde estabas trabajando en el diseño de un botón, pero tu jefe te pide arreglar urgente un texto en la página principal, entonces te "cambias" a la versión principal un momento.


### git switch -c nombre-de-tu-rama

- Crear la rama y saltar a ella de una vez (Recomendado)
- Nota: Si usas una versión de Git un poco más antigua, el comando equivalente que hace exactamente lo mismo es `git checkout -b nombre-de-tu-rama`



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


### **Fork** (que significa "tenedor" o "bifurcación")

-  es un botón en GitHub que sirve para **sacar una copia exacta del repositorio de otra persona y guardarla dentro de tu propia cuenta de GitHub**.

- haces el **Fork**, luego un `git clone` a tu PC, modificas el código, y haces `git commit` y `git push`. En ese punto, los cambios ya están guardados con éxito en **tu repositorio clonado**.

- Para que esos cambios lleguen al repositorio original de los dueños, se usa una herramienta llamada **Pull Request (PR)**. El flujo completo funciona así:

```
[Repo Original] ──(Fork)──> [Tu Repo en GitHub] ──(Clone)──> [Tu PC]
       ▲                                                       │
       │                                                   (Cambios)
       └──────────(Pull Request)◄─────────(Push)───────────────┘
```

El paso a paso en la vida real:

1. **Haces el Push:** Subes los cambios desde tu PC a tu repositorio de GitHub (tu Fork).
2. **Abres GitHub:** Entras a la página de **tu Fork** en el navegador.
3. **El botón mágico:** GitHub detectará automáticamente que tu repositorio tiene cambios nuevos que el original no tiene, y te mostrará un botón verde brillante que dice **"Compare & pull request"** (o "New pull request").
4. **Creas el Pull Request:** Al hacer clic, le estás enviando una propuesta formal a los dueños originales. Es como tocarles la puerta y decirles: _"Hola, miren, corregí este error en el código, ¿les gustaría revisar mi propuesta e incluirla en su proyecto?"_.
5. **Ellos deciden (El Merge):** Los dueños originales recibirán una notificación. Ellos revisarán tu código en una pantalla de GitHub donde se ve exactamente qué líneas borraste y cuáles agregaste:
    - Si les gusta tu cambio, presionarán un botón llamado **Merge**. En ese instante, tu código se fusionará con el de ellos y ¡listo!, habrás contribuido oficialmente a un proyecto Open Source.
    - Si encuentran algo mal, te dejarán comentarios en el mismo Pull Request para que lo corrijas antes de aceptarlo.

---

### **git log**
Sirve para: Ver el historial o el diario de todos los guardados (commits) que se han hecho en el proyecto, mostrando quién hizo qué y cuándo.

- **Cómo se conecta con otros:** Se enlaza con **`git status`**, porque status te dice el presente (qué estás haciendo ahora), mientras que log te muestra el pasado (qué se ha hecho antes).
- **Cuándo usarlo:** Sirve para casos donde alguien borró una imagen por error la semana pasada, y quieres mirar el historial para saber exactamente quién y qué día lo hizo.


### git revert <ID_DEL_COMMIT>

nos sirve para revertir cambios  o borrarlo no olvidar que con git log -- oneline podemos obtener el ID de ese commit 

### **git log --oneline**

- Es para que salga el código de cada commit, git no entiende por nombres guardados sino por código saldrá algo así `a1b2c3d nombre del commit`

### git switch --detach numero del commit => (a1b2c3d)

- Viaja al pasado con `git switch` esto nos sirve para saltar entre commits osea es para devolverme a codigos anteriores y demas 

- Cuando haces esto, Git entra en un estado llamado _Detached HEAD_. Significa que estás mirando el pasado pero **no debes ponerte a programar ni a hacer nuevos commits ahí**, porque se podrían perder en el espacio. Usa este modo solo para:

	- Revisar cómo funcionaba el botón antes.
	- Copiar un trozo de código antiguo que borraste sin querer.
	- Asegurarte de que todo compilaba bien en esa fecha.


### git switch nombre-de-tu-rama


Cuando hayas terminado de revisar el pasado y quieras volver a la rama que te asignó tu jefe con todo tu trabajo actual intacto, solo debes escribir:

# por investigar
- Escribes: `git stash` (Guarda tus cambios actuales en una caja fuerte temporal y limpia tu espacio de trabajo).
- Viajas al pasado, revisas lo que necesitas y regresas al presente con `git switch nombre-de-tu-rama`.
- Escribes: `git stash pop` (Saca tus cambios de la caja fuerte y los vuelve a poner en tus archivos exactamente como los dejaste).
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

