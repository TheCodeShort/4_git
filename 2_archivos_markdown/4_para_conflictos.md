
# git config pull.rebase true

- **¿Qué hace?** Cambia la configuración interna de Git para este proyecto específico. Le dice a Git que, a partir de ahora, cada vez que hagas un `git pull`, use la estrategia de **Rebase** (rebasar) en lugar de crear commits de fusión.
- **Por qué lo usaste:** Lo ejecutaste para responder al mensaje de ayuda amarillo que te daba Git en la primera pantalla, donde te exigía definir una estrategia para reconciliar tus ramas divergentes.

# git rm --cached .obsidian/workspace.json

- **¿Qué hace?**: `git rm` significa remover/borrar para Git. La bandera `--cached` es la clave aquí: le dice a Git que **borre el archivo de su memoria/historial de seguimiento, pero NO de tu computadora**.
- **En la práctica**: Tu archivo seguirá existiendo en tu PC para que Obsidian funcione bien, pero Git dejará de vigilar si cambia o no.


# git checkout --theirs .obsidian/workspace.jso`

- **Qué hace:** Le dice a Git: _"En este archivo que choca, borra lo de esta PC y quédate con lo que viene de mi otra PC"_.

# git add .obsidian/workspace.json

- **Qué hace:** Marca el conflicto de ese archivo como "resuelto" y lo prepara para guardarse.

# git rebase --continue

- **Qué hace:** Le dice a Git: _"Ya arreglé el problema, continúa acomodando el resto de mis commits"_.