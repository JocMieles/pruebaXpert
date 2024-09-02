# Reto BREEDS - XpertGroup
Este proyecto desarrolla una aplicación Web en el cual se uso para el Frontend Angular, TypeScript y Bootstrap, y para el Backend se uso Node, Express y Jest, y sirve para gestionar razas de gatos. Los usuarios pueden registrarse, iniciar sesion, seleccionar una raza de gato y visualizar tanto un carrusel de imágenes como una tabla detallada con información relevante sobre la raza seleccionada. La aplicación está diseñada para ser intuitiva, escalable y fácil de usar, brindando una experiencia interactiva a los usuarios.

## Configuración Inicial

Instrucciones sobre cómo clonar y configurar el proyecto para ejecutarlo localmente:
```bash
git clone --recurse-submodules https://github.com/JocMieles/pruebaXpert.git
cd pruebaXpert
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
cd backXpert
npm i
npm install

cd .. 

cd fronXpert
npm ci --legacy-peer-deps
npm install -g @angular/cli --legacy-peer-deps
npm install  --legacy-peer-deps

cd ..
docker-compose up --build

```
El API o Backend queda expuesto en el puerto 3000 - **localhost:3000**
El Frontend en el puerto 80 - **localhost:80**

- Instrucciones paso a paso para instalar y ejecutar sin Docker:

```bash
Entrar en cada carpeta 

FRONTEND

cd frontXpert
npm ci --legacy-peer-deps
npm install -g @angular/cli --legacy-peer-deps
npm install  --legacy-peer-deps

npm run start o ng serve


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

## Pruebas Unitarias

# Backend
Las pruebas unitarias en el backend se centran en validar la lógica del negocio y las respuestas del API. Se utilizan frameworks como Jest para asegurar que los servicios y controladores funcionen correctamente.
npx jest

# Frontend
Las pruebas unitarias en el frontend son fundamentales para asegurar que los componentes y servicios de Angular funcionen correctamente. Se utiliza Jasmine y Karma para llevar a cabo estas pruebas.
ng test


## Propuestas Futuras

Se sugiere como complemento a este desarrollo:

Implementar un mejor sistema de autenticación para proteger rutas específicas.
Agregar sistema de popups o modales de información para el usuario.
Optimizar la aplicación para dispositivos móviles (mejorar la responsividad del carrusel y tablas).
Agregar una funcionalidad de "favoritos" para que los usuarios puedan marcar y guardar razas preferidas.
Implementar paginación y filtrado avanzado en la tabla de razas.
