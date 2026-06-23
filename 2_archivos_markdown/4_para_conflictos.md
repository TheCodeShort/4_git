
# git config pull.rebase true

- **¿Qué hace?** Cambia la configuración interna de Git para este proyecto específico. Le dice a Git que, a partir de ahora, cada vez que hagas un `git pull`, use la estrategia de **Rebase** (rebasar) en lugar de crear commits de fusión.
- **Por qué lo usaste:** Lo ejecutaste para responder al mensaje de ayuda amarillo que te daba Git en la primera pantalla, donde te exigía definir una estrategia para reconciliar tus ramas divergentes.
- **¿Qué hace exactamente?** Activa el método **Rebase** exclusivamente para este proyecto. Le dice a Git: _"Cuando traiga cosas de la nube en esta carpeta, aparta mis commits locales un momento, descarga lo del servidor y luego pon mis cambios arriba de forma limpia"_.

# git rm --cached .obsidian/workspace.json

- **¿Qué hace?**: `git rm` significa remover/borrar para Git. La bandera `--cached` es la clave aquí: le dice a Git que **borre el archivo de su memoria/historial de seguimiento, pero NO de tu computadora** sino de GitHub.

- **En la práctica**: Tu archivo seguirá existiendo en tu PC para que Obsidian funcione bien, pero Git dejará de vigilar si cambia o no.

- Despues de dejar o borrar de GitHub la carpeta que no se necesita hay que guardar los cambios con un commit y no olvidar [[7_guia_commits#^8dcf15]]


# git checkout --theirs .obsidian/workspace.jso`

- **Qué hace:** Le dice a Git: _"En este archivo que choca, borra lo de esta PC y quédate con lo que viene de mi otra PC"_.

# git add .obsidian/workspace.json

- **Qué hace:** Marca el conflicto de ese archivo como "resuelto" y lo prepara para guardarse.

# git rebase --continue

- **Qué hace:** Le dice a Git: _"Ya arreglé el problema, continúa acomodando el resto de mis commits"_.