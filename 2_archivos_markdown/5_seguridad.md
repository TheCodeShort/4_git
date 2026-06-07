# para tener el correo pribado GitHub

- Ve a la esquina superior derecha, haz clic en tu foto de perfil y selecciona **Settings** (Configuración) pero no del repo.
- En la barra lateral izquierda, haz clic en **Emails**.
- Busca la sección llamada **Keep my email addresses private** (Mantener mis direcciones de correo privadas).
- Ahí verás un correo con el formato `ID+username@://github.com`. Copia esa dirección.


# **`git config --global user.email "..."`**
 Le dice a Git qué correo electrónico debe estampar en cada cambio que hagas . Al usar el correo anónimo de GitHub, proteges tu cuenta real de spammers que recolectan correos de repositorios públicos.
# **`git config --global user.name "..."`**
Define el nombre visible que aparecerá junto a tus cambios.

# `git config --list` 

Esto te mostrará una lista con tu nombre, correo y otras preferencias activas.


# `ssh-keygen -t ed25519 -C "165424154+TheCodeShort@://github.com"`

- con esto creamos nuestra llave criptografica esto nos ayuda a tener seguridad y se usa cuando se creo un repo y el link es en SSH 

- recordar que el correo es el que hayamos registrado en este ejemplo este correo se lo da GitHub para evitar poner el original o propio 

- esto se guarda en el computador es como registrar o darle permiso a los computadores para que puedan hacer un push o hacer cambios 

- Cuando se crea nos mostrara la ruta y después nos deja ponerle contraseña a ese archivo pero se puede dejar sin contraseña

## Para guardar la llave creada en GitHub

- esta llave se guarda en github esto nos sirve para evitar poner siempre la clave automáticamente el lo hace va al PC y busca la llave 

- nos dirigimos a la ruta que nos creo en el paso anterior que en linux es /hom/name_user/ssh y buscamos la carpeta ssh y hay una llamada asi id_ed25519.pub  puede variar un poco pero es el mismo formato aca se encuentra la llave que empieza con  ssh


# `ssh -T git@github.com`

- con esto podemos probar la conexion a git hub, preguntara si queremos hacer la conexion se escribe que yes despues ENTER y saldra  `Hi TheCodeShort! You've successfully authenticated, but GitHub does not provide shell access.
`