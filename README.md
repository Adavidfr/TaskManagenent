# Task-Management

Task-Management es un sistema de administración de tareas desarrollado utilizando una arquitectura de microservicios. Este proyecto permite gestionar tareas, usuarios, y la presentación de tareas de manera eficiente. Está compuesto por varios servicios que se comunican entre sí y están desplegados utilizando Spring Boot y MySQL.

## Estructura del Proyecto

Este proyecto consta de los siguientes microservicios:

### 1. **Eureka-server**
- **Descripción**: Este servicio actúa como el servidor de descubrimiento de servicios utilizando Eureka, permitiendo que los servicios se registren y encuentren entre sí.
- **Puertos**: 8083

### 2. **Gateway**
- **Descripción**: El Gateway es responsable de enrutar todas las peticiones entre los diferentes servicios. Funciona como un punto único de entrada para todas las solicitudes, facilitando el enrutamiento hacia los servicios adecuados.
- **Puertos**: 5000

### 3. **Task-service**
- **Descripción**: Este servicio maneja todas las funcionalidades relacionadas con las tareas, como crear, editar, buscar y asignar tareas.
- **Funciones principales**:
    - Crear tareas
    - Editar tareas
    - Buscar tareas
    - Asignar tareas
- **Puertos**: 8081

### 4. **Task-submission-service**
- **Descripción**: Este servicio maneja las funcionalidades relacionadas con las presentaciones de tareas. Permite a los usuarios enviar tareas, obtener las presentaciones de tareas y aceptar o rechazar presentaciones.
- **Funciones principales**:
    - Enviar tareas (`submitTask`)
    - Obtener presentaciones de tareas (`get submissions`)
    - Aceptar o rechazar presentaciones (`accept or decline`)
- **Puertos**: 8082 (puerto configurable para el servicio de presentación de tareas)

### 5. **task-user-service**
- **Descripción**: Este servicio maneja la autenticación de usuarios, el inicio de sesión, el registro de nuevos usuarios y la asignación de roles (usuario o administrador).
- **Funciones principales**:
    - Registro de usuarios
    - Inicio de sesión
    - Asignación de roles (usuario o administrador)
- **Puertos**: 8080

## Requisitos

- **Java 17**: Este proyecto utiliza Java 17 como versión de Java.
- **MySQL**: Se usa MySQL como base de datos para almacenar información relacionada con las tareas y los usuarios.

## Instalación

### 1. Clona el repositorio:

```bash
https://github.com/Adavidfr/Adavidfr.git
