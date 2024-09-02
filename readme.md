# Reto BREEDS - XpertGroup

## Configuración Inicial

Instrucciones sobre cómo clonar y configurar el proyecto para ejecutarlo localmente:
```bash
git clone --recurse-submodules https://github.com/JocMieles/pruebaXpert.git

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
| POST    | `/users/login`                | Recibir el token del usuario. |
| POST   | `/users/register`                | Crea un nuevo usuario.                   |
| GET    | `/breeds`            | Obtiene todas las razas.            |
| PUT    | `/breeds/search`            | Filtra los nombres de las razas por lo que escribas.          |
| DELETE | `/breeds/:breed_id`            | Obtiene una raza por su ID.            |
| GET    | `/imagesbybreedid/:breed_id`               | Obtiene una lista imagenes por el ID de la raza.   |

## Consumo api y ejemplos

Para crear debes enviar en el body: 
```json
{
  "name": "daniel Mieles",
  "email": "josedmieslses@ejemplo.com",
  "password": "test123*"
}

```

Para recibir el token debes enviar en el body:
```json
{
  "email": "josedmieslses@ejemplo.com",
  "password": "test123*"
}
```