
# Sistema de Base de Datos para Biblioteca (3FN)

Repositorio que contiene el diseño relacional, el script de creación y la documentación de una base de datos normalizada hasta la **Tercera Forma Normal (3FN)** para la gestión de una biblioteca.

## Estructura del Proyecto

El proyecto está compuesto por tres entidades principales diseñadas para eliminar redundancias y dependencias transitivas:

1. **`Autores`**: Almacena la información de los escritores.
   - `ID_Autor` (PK)
   - `Nombre_Autor`
2. **`Editores`**: Almacena la información de las editoriales.
   - `ID_Editor` (PK)
   - `Nombre_Editor`
3. **`Libros`**: Tabla central que registra los títulos y los vincula con su respectivo autor y editorial.
   - `ID_Libro` (PK)
   - `Titulo_Libro`
   - `ID_Autor` (FK)
   - `ID_Editor` (FK)

## Diagrama Entidad-Relación (EER)

El modelo relacional muestra la relación de uno a muchos ($1:N$) entre las entidades maestras (`Autores` y `Editores`) y la tabla transaccional (`Libros`):
