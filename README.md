# EscuChamos Postman Collection

Este repositorio contiene la colección de Postman para probar y utilizar la API de **EscuChamos**.

## Descripción

El archivo `EscuChamos.postman_collection.json` incluye una serie de peticiones HTTP organizadas por módulos para interactuar con el backend de la aplicación. Los módulos cubiertos incluyen:

- **Auth**: Registro, inicio de sesión, recuperación de cuenta, verificación de correo.
- **Users**: Gestión de perfil, cambio de contraseña, subir/eliminar fotos, administración de usuarios.
- **Notifications**: Notificaciones en vivo, leer/visto, conteo y eliminación.
- **Follows**: Seguir/dejar de seguir usuarios, ver seguidores/seguidos.
- **Countries**: Listado e información de países de la base de datos.
- **Statuses**: Estados disponibles en el sistema.
- **Type posts**: Tipos de publicaciones.
- **Posts**: Creación, actualización, visualización y eliminación de publicaciones.
- **Shares**: Compartir publicaciones.

## Prerrequisitos

- [Postman](https://www.postman.com/downloads/) instalado en tu equipo.

## Instalación

1.  Clona este repositorio o descarga el archivo `EscuChamos.postman_collection.json`.
2.  Abre Postman.
3.  Haz clic en el botón **Import** (arriba a la izquierda).
4.  Selecciona o arrastra el archivo `EscuChamos.postman_collection.json`.
5.  La colección "EscuChamos" aparecerá en tu panel izquierdo de colecciones.

## Configuración de Variables

Para que las peticiones funcionen correctamente, debes configurar las siguientes variables de entorno en Postman. Puedes hacerlo creando un nuevo "Environment" o editando las variables de la colección.

| Variable | Descripción | Ejemplo |
| :--- | :--- | :--- |
| `url` | La URL base de tu API (incluyendo el slash final si es necesario) | `http://localhost:8000/api/` |
| `token` | El token de autenticación (JWT) obtenido tras el login | `Bearer eyJ0eXAiOiJK...` |

### Cómo obtener el token

1.  Ve a la carpeta **Auth** > **login**.
2.  En el **Body**, ingresa un `username` y `password` válidos.
3.  Envía la petición (**Send**).
4.  Copia el token de la respuesta y actualiza la variable `token` en tu entorno de Postman.
    *   *Nota*: Asegúrate de incluir el prefijo `Bearer ` si la API lo requiere, o configuralo directamente en la pestaña **Authorization** de la colección si está automatizado.

## Uso

1.  Selecciona la petición que deseas probar (ej. **Posts** > **index**).
2.  Asegúrate de que el entorno correcto esté seleccionado (donde definiste `url` y `token`).
3.  Revisa los parámetros (`Params`), el cuerpo (`Body`) o los encabezados (`Headers`) si necesitas modificar algún dato.
4.  Haz clic en **Send**.
5.  Verifica la respuesta en el panel inferior.
