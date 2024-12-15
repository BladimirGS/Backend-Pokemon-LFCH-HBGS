# API en Laravel
Este proyecto está desarrollado con Laravel 11 y proporciona una API para gestionar usuarios y Pokémon, incluyendo funcionalidades de autenticación y operaciones CRUD.

## Características

- **Validación del login:**
  Permite la autenticación de usuarios.

- **API de Usuarios:**
  - Obtención de la lista de usuarios.
  - Creación, edición y eliminación de usuarios.

- **API de Pokémon:**
  - Obtención de la lista de Pokémon.
  - Creación, edición y eliminación de Pokémon.

## Requisitos Previos
- PHP 
- Composer
- MySQL

## Instalación y Ejecución

### Clonar el repositorio
```bash
https://github.com/BladimirGS/Backend-Pokemon-LFCH-HBGS.git
```

### Ir a la carpeta del proyecto
```bash
cd Backend-Pokemon-LFCH-HBGS
```

### Instalar dependencias
```bash
composer install
```

### Genera tus variables de entorno
```bash
cp .env.example .env
```

### Configurar el archivo `.env`

```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=nombre_de_tu_base_de_datos
DB_USERNAME=tu_usuario
DB_PASSWORD=tu_contraseña
```

### genera una clave con
```bash
php artisan key:generate
```

### Ejecutar migraciones y seeders
```bash
php artisan migrate --seed
```

### Iniciar el servidor de desarrollo
```bash
php artisan serve
```
El servidor estará disponible en:
```
http://127.0.0.1:8000
```

## Endpoints Principales

### Autenticación
- **POST** `/api/login`: Inicia sesión.
- **POST** `/api/logout`: Cierra la sesión.

### Usuarios
- **GET** `/api/users`: Obtiene la lista de usuarios.
- **POST** `/api/users`: Crea un nuevo usuario.
- **PUT** `/api/users/{id}`: Actualiza los datos de un usuario.
- **DELETE** `/api/users/{id}`: Elimina un usuario.

### Pokémon
- **GET** `/api/pokemon`: Obtiene la lista de Pokémon.
- **POST** `/api/pokemon`: Crea un nuevo Pokémon.
- **PUT** `/api/pokemon/{id}`: Actualiza los datos de un Pokémon.
- **DELETE** `/api/pokemon/{id}`: Elimina un Pokémon.

## Estructura de las Tablas (Esquema)

### Usuarios
- `id`: Identificador del usuario.
- `name`: Nombre del usuario.
- `email`: Correo electrónico.
- `password`: Contraseña encriptada.

### Pokémon
- `id`: Identificador del Pokémon.
- `name`: Nombre del Pokémon.
- `image`: Imagen del Pokémon.

## Licencia
![MIT License](https://img.shields.io/badge/License-MIT-green.svg)

