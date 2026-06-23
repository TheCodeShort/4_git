https://www.conventionalcommits.org/pt-br/v1.0.0-beta.4/

La especificación **Conventional Commits** fue creada originalmente por **[![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABEAAAARCAYAAAA7bUf6AAACCElEQVR4AaSSP2hTQRzHP+93d8kLhQptU5FuQVTooNJFsA5qceriUJxdbFHoIGTo0kmhQ1e3gJtjSyCriHuGUiJSNRCRaHCIBTFqzXvn/S4o3d8Pvvzeu/vd535/TpIk8UWlEAKkkMQYQ1FJMArrXxbOuQhTr+UpWPfURyWWcuYou5xMKlhJ/lcgGlgqlajVahwcHNDtdjk6OmJ3dzcGKbQksHkz5e3jEe83ofPwO+fPljFhXc9LMBYXF2m32xFUrVZZWFhgfX2dnZ0dvHE8umZ4cv0b1TPCfPqHizOG9oNfXK4RMhLEWsvKygrq9/b2aLVa1Ot11DY2Nqg4y9NbP8gQ7jdnudqY5tWHE2x+wr1ajoR9caEXa2trccR6eHV1la2tLXq9nnK4cuEcOYZPx4aXPc+X3xXutuYg8dy55LHGEnuiIO89eZ5HWJqmjMfj+F1yBvGEPDxOBO1BnlvUyrmP/6ElEoN10YWs1Ot0VAp2xjBOdBWckXCzQUIJPoc8mUBFyfv7+wwGA6amphgOhzSbTTqdDv1+n8OPx3z+mfJmmILNCAeQtMzXbJrmu9lJJtrQRqPB8vIyo9GIpaUltre3Y3O14ZJl3H4xT/31TMhgOg5g1ibceD7Hs8PKBCIisRyFqfTNqFcRLLEGCRP0poSEB6bxqqSsDT1VjpZURAEq4YbCKgzgLwAAAP//Ei3eCQAAAAZJREFUAwB1lZ4Jh0Ve6wAAAABJRU5ErkJggg==)⁠Benjamin E. Coe](https://blog.marcnuri.com/conventional-commits)** en el año **2017**.

# ¿En qué se inspiró?

Benjamin Coe se basó directamente en las directrices de contribución de **Angular** (el famoso framework de programación creado por **Google**). El equipo de Google ya usaba estos prefijos en sus proyectos internos para organizar sus miles de commits diarios. Lo que hizo Coe fue tomar esa idea de Google, limpiarla y redactarla como un estándar abierto e independiente para que cualquier empresa del mundo pudiera usarlo.

# ¿Quién es Benjamin E. Coe?

No es un programador cualquiera; en ese momento y durante años fue un ingeniero clave y líder de equipo en **npm** (el gestor de paquetes de Node.js, que hoy pertenece a **GitHub / Microsoft**). Al ser una figura importante en el mundo del código abierto, su propuesta ganó confianza inmediata en la comunidad.

# ¿Cuándo y por qué lo empezaron a usar las empresas?

- **El inicio (2017 - 2018):** Se empezó a usar formalmente en **2017** con sus primeras versiones de prueba (de ahí el "beta" que ves en tu link). Al principio lo adoptaron proyectos grandes de código abierto. 

- **La explosión comercial (2019 - 2020):** En **2019** se lanzó la versión estable `1.0.0`. A partir de ese año, las empresas medianas y grandes lo adoptaron masivamente. 

1. `feat:` Feature (Funcionalidad)

- **¿Cuándo se usa?**: Cuando agregas algo nuevo al proyecto que el usuario final puede ver o usar.
- **Ejemplo en terminal**:
    
    
    ```git
    git commit -m "feat: agregar botón de modo oscuro en la barra de navegación"
    ```
    
    

2. `fix:` Bug Fix (Corrección)

- **¿Cuándo se usa?**: Cuando arreglas un error, un fallo o un bug en el código que estaba funcionando mal.
- **Ejemplo en terminal**:
    
    
    ```git
    git commit -m "fix: corregir error que cerraba la aplicación al hacer clic en enviar"
    ```


3. `!` o `BREAKING CHANGE:` **Cambio Rompedor / Destructivo** (Cambio Drástico)

- **¿Cuándo se usa?**: Cuando haces un cambio tan grande que "rompe" el código anterior. Avisa a los demás programadores que deben actualizar todo porque lo viejo ya no funcionará. Se puede poner un signo `!` antes de los dos puntos o la palabra abajo.
- **Ejemplo en terminal (con `!`)**:
    
    
    ```git
    git commit -m "feat!: cambiar base de datos de Mysql a PostgreSQL"
    ```
    
    

---

# 👥 Los 5 más usados de la comunidad

La página oficial dice que puedes usar otros nombres si tu equipo quiere. Estos son los 5 que todo el mundo usa en el trabajo real para que el historial quede perfecto.

4. `docs:` (Documentación)

- **¿Cuándo se usa?**: Cuando solo cambias textos de explicación, manuales de usuario o el archivo `README.md`. No tocas nada de código del programa.
- **Ejemplo en terminal**:
    
    bash
    
    ```git 
    git commit -m "docs: actualizar las instrucciones de instalación en el README"
    ```
    
    Usa el código con precaución.
    

5. `chore:` Tarea hogareña o rutina (Tareas rutinarias / Mantenimiento) ^8dcf15

- **¿Cuándo se usa?**: Para tareas de limpieza que no cambian el código del negocio ni arreglan bugs. Por ejemplo, instalar una librería, configurar herramientas o actualizar dependencias.
- **Ejemplo en terminal**:
    
    bash
    
    ```git 
    git commit -m "chore: instalar la librería axios para peticiones web"
    ```
    
    Usa el código con precaución.
    

6. `test:` **Automated Tests** (Pruebas)

- **¿Cuándo se usa?**: Cuando creas o modificas archivos de pruebas automatizadas (test unitarios) para comprobar que tu código funciona bien.
- **Ejemplo en terminal**:
    
    bash
    
    ```git 
    git commit -m "test: agregar prueba para validar el formulario de registro"
    ```
    
    Usa el código con precaución.
    

7. `refactor:` **Refactoring** (Refactorización)

- **¿Cuándo se usa?**: Cuando mejoras cómo está escrito el código por dentro para que sea más limpio o rápido, pero el programa visualmente sigue haciendo **exactamente lo mismo** para el usuario. No es una función nueva ni un bugfix.
- **Ejemplo en terminal**:
    
    bash
    
    ```git 
    git commit -m "refactor: simplificar la función que calcula los precios del carrito"
    ```
    
    Usa el código con precaución.
    

8. `style:` **Code Style / Formatting** (Estilos y formato)

- **¿Cuándo se usa?**: Cambios que no afectan el significado del código (espacios en blanco, formato, falta de puntos y comas, etc.). _Ojo: No se refiere a hojas de estilo CSS de diseño, sino al estilo visual del texto del código._
- **Ejemplo en terminal**:
    
    bash
    
    ```git 
    git commit -m "style: corregir indentación y eliminar espacios en blanco dobles"
    ```