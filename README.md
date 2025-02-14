# Ingeniería del software

Manual para una asignatura de **Ingeniería del software** para estudiantes de grado (por ejemplo, grado en Ingeniería Informática).

## Uso

### Construcción del libro

Si deseas desarrollar y/o compilar el libro de Ingeniería del Software, debes:

1. Clonar este repositorio.
2. Ejecutar `pip install -r requirements.txt` (se recomienda hacerlo dentro de un entorno virtual).
3. (Opcional) Editar los archivos fuente del libro ubicados en el directorio `manual_ings/`.
4. Ejecutar `jupyter-book clean manual_ings/` para eliminar cualquier compilación existente.
5. Ejecutar `jupyter-book build manual_ings/`.

Se generará una versión completamente renderizada en HTML del libro en `manual_ings/_build/html/`.

### Publicación del libro

Consulta la [documentación de Jupyter Book](https://jupyterbook.org/publish/web.html) para conocer las opciones de publicación en línea del libro mediante servicios como GitHub, GitLab o Netlify.

Para la publicación específicamente en GitHub y GitLab, el proyecto [cookiecutter-jupyter-book](https://github.com/executablebooks/cookiecutter-jupyter-book) incluye plantillas e información sobre archivos opcionales de flujo de integración continua (CI) que permiten desplegar libros en línea de manera fácil y automática con GitHub o GitLab. Por ejemplo, si elegiste `github` en la opción `include_ci` de cookiecutter, tu plantilla de libro se generó con un archivo de flujo de trabajo de GitHub Actions que, una vez enviado a GitHub, renderiza automáticamente y publica tu libro en la rama `gh-pages` de tu repositorio, alojándolo en GitHub Pages cuando se realiza un push o pull request en la rama principal.

## Contribuidores

Damos la bienvenida y reconocemos todas las contribuciones. Puedes ver la lista de contribuidores actuales en la [pestaña de contribuidores](https://github.com/angellareo/manual_ings/graphs/contributors).

## Créditos

Este proyecto ha sido creado utilizando el excelente proyecto de código abierto [Jupyter Book](https://jupyterbook.org/) y la plantilla [executablebooks/cookiecutter-jupyter-book](https://github.com/executablebooks/cookiecutter-jupyter-book).
