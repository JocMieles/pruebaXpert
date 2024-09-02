# Reto BREEDS - XpertGroup

##C onfiguración Inicial

Instrucciones sobre cómo clonar y configurar el proyecto para ejecutarlo localmente:
```bash
git clone **https://github.com/JocMieles/Xpert.git**

cd Xpert
```

## Requisitos

- Node.js (v14 o superior)
- Angular (v17)
- Docker
- Docker Compose
- MongoDB

## Instalación y Ejecución

- Instrucciones paso a paso para instalar y ejecutar el proyecto utilizando Docker:

```bash

Iniciar Docker Compose

npm install

docker-compose up --build

```
El API o Backend queda expuesto en el puerto 3000 - **localhost:3000**
El Frontend en el puerto 80 - **localhost:80**

- Instrucciones paso a paso para instalar y ejecutar sin Docker:

```bash
Entrar en cada carpeta 

FRONTEND

cd fronXpert
npm ci --legacy-peer-deps
npm install -g @angular/cli --legacy-peer-deps
npm install  --legacy-peer-deps

npm run start

BACKEND

cd backXpert

npm i
npm run start

```

### BASE DE DATOS

#### User
- `id`: Clave primaria, identificador único para cada usuario.
- `username`: Nombre de usuario único.
- `email`: Correo electrónico del usuario.
- `contraseña`: Contraseña del usuario.

## API Endpoints

A continuación se presenta una tabla con los endpoints disponibles en la aplicación:

| Método | Ruta                    | Descripción                              |
|--------|-------------------------|------------------------------------------|
| POST    | `/users/login`                | Obtiene una lista de todos los usuarios. |
| POST   | `/users/register`                | Crea un nuevo usuario.                   |
| GET    | `/image/:id`            | Obtiene un usuario por su ID.            |
| PUT    | `/users/:id`            | Actualiza un usuario por su ID.          |
| DELETE | `/users/:id`            | Elimina un usuario por su ID.            |
| GET    | `/videos`               | Obtiene una lista de todos los videos.   |
| POST   | `/videos`               | Crea un nuevo video.                     |
| GET    | `/videos/:id`           | Obtiene un video por su ID.              |
| PUT    | `/videos/:id`           | Actualiza un video por su ID. Inhabilitado          |
| DELETE | `/videos/:id`           | Elimina un video por su ID.              |
| GET    | `/comments`             | Obtiene una lista de todos los comentarios. |
| POST   | `/comments`             | Crea un nuevo comentario.               |
| GET    | `/comments/:id`         | Obtiene un comentario por su ID.        |
| PUT    | `/comments/:id`         | Actualiza un comentario por su ID.      |
| DELETE | `/comments/:id`         | Elimina un comentario por su ID.        |