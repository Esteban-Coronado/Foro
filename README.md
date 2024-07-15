# Foro
El objetivo de este proyecto es proporcionar una plataforma donde los usuarios puedan registrar, listar, actualizar y eliminar topics relacionados con diferentes cursos. La aplicación garantiza la seguridad de las operaciones a través de la implementación de Spring Security y el uso de tokens JWT para la autenticación de usuarios.

## Tecnologías Utilizadas
- MySQL
- Java
- Spring Security
- Token JWT

## Funcionalidades de la API

- ### Registro de un Nuevo Topic
Método: POST
Permite registrar nuevos topics enviando datos como título, mensaje, autor y curso en formato JSON. Los datos son validados antes de almacenarse en la base de datos.

- ### Listado de Topics
Método: GET
Devuelve una lista de todos los topics disponibles con detalles como título, mensaje, fecha de creación, estado, autor y curso en formato JSON.

- ### Detalle de Topics
Método: GET
Proporciona los detalles de un topic específico utilizando el ID del topic extraído con @PathVariable.

- ### Actualización de Topic
Método: PUT
Permite actualizar la información de un topic específico. Los datos recibidos son validados y se asegura que el topic exista antes de realizar la actualización.

- ### Eliminación de Topic
Método: DELETE
Permite eliminar un topic específico. Se verifica la existencia del topic antes de proceder con la eliminación.

- ### Implementación de Spring Security
Spring Security se ha implementado para asegurar que solo los usuarios autenticados puedan interactuar con la API. La clase SecurityConfigurations gestiona el acceso a través de solicitudes HTTP.

- ### Autenticación de Usuarios
Un controlador de autenticación maneja las solicitudes de inicio de sesión, utilizando AuthenticationManager para validar las credenciales de los usuarios.

- ### Base de Datos de Usuarios
La base de datos se ha extendido para incluir una tabla de usuarios, donde se almacenan las credenciales de autenticación.

- ### Token JWT
Para aumentar la seguridad, se ha implementado el uso de tokens JWT. La clase TokenService se encarga de generar y validar tokens, con configuraciones definidas en application.properties.