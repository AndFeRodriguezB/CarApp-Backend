# 🚗 CarApp Backend API

Backend de aplicación Full Stack para gestión de solicitudes de vehículos.

API REST construida con FastAPI, conectada a PostgreSQL en la nube.
 Dockerizado y listo para ejecutarse en contenedores.

---

## 🌍 Producción

Base URL:


https://carapp-backend-34v5.onrender.com


Documentación interactiva (Swagger):


https://carapp-backend-34v5.onrender.com/docs


---

## 🛠️ Stack Tecnológico

- FastAPI
- SQLAlchemy
- Pydantic
- PostgreSQL
- Docker
- Docker Compose
- Uvicorn
- Render (deploy)

---

## 🐳 Ejecutar con Docker

Clonar el repositorio:

git clone https://github.com/tuusuario/carapp.git
cd Backend

Construir y levantar contenedores:

docker compose up --build

La API estará disponible en:

http://localhost:8000/docs


🔹 Contenedores

El sistema se compone de dos contenedores:

Backend

FastAPI

Uvicorn

SQLAlchemy

Ejecutado en python:3.11-slim

Base de datos

PostgreSQL 15

Healthcheck habilitado para asegurar disponibilidad antes de que el backend inicie
---

## 📂 Arquitectura


backend/
│
├── app/
│   ├── main.py
│   │
│   ├── api/
│   │   └── v1/
│   │       ├── endpoints/
│   │       └── __init__.py
│   │
│   ├── core/
│   │   ├── config.py
│   │   ├── database.py
│   │   └── __init__.py
│   │
│   ├── models/
│   │   └── __init__.py
│   │
│   ├── schemas/
│   │   └── __init__.py
│   │
│   ├── crud/
│   │   └── __init__.py
│   │
│   └── __init__.py
│
├── tests/
│
├── .dockerignore
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── .env


Arquitectura organizada por capas:
- Models → Definición ORM
- Schemas → Validación de datos
- CRUD → Lógica de base de datos
- Endpoints → Rutas versionadas
- Core → Configuración y conexión DB

---

## 🔗 Endpoints

Base path:


/api/v1


### Vehículos

- `POST /api/v1/cars`
- `GET /api/v1/cars`
- `PUT /api/v1/cars/{id}`
- `DELETE /api/v1/cars/{id}`

---

## ⚙️ Funcionalidades

- CRUD completo
- Filtros dinámicos (marca, localidad, solicitante)
- Paginación (skip, limit)
- Ordenamiento dinámico (sort_by, order)
- CORS configurado para entorno de producción
- API versionada

---

## 🗄 Base de Datos

PostgreSQL gestionado en la nube (Render).

Configuración mediante variable de entorno:


DATABASE_URL


---

## 🚀 Ejecución Local

1. Clonar repositorio
2. Crear entorno virtual
3. Instalar dependencias:


pip install -r requirements.txt


4. Configurar `.env`:


DATABASE_URL=postgresql://user:password@localhost:5432/dbname


5. Ejecutar:


uvicorn app.main:app --reload


---

## 🏗 Estado del Proyecto

- Backend desplegado en producción
- Conexión activa a PostgreSQL
- Documentación Swagger operativa
- API estable y funcional

---

## 🔗 Repositorio del Frontend

Interfaz web disponible en:

https://github.com/AndFeRodriguezB/CarApp-Frontend.git

Demo pública:

https://playful-tiramisu-85452d.netlify.app

--- 

## 👨‍💻 Autor

Proyecto desarrollado como aplicación Full Stack por Andrés Rodriguez