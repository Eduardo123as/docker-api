# docker-api

Una aplicación Flask containerizada con Docker que proporciona una API REST simple para demostrar la integración de aplicaciones Python con Docker.

## 📋 Descripción General

Este repositorio contiene una aplicación web construida con Flask que se ejecuta dentro de un contenedor Docker. Proporciona endpoints REST básicos para verificar el estado de la aplicación y obtener mensajes de saludo.

## 🛠️ Stack Tecnológico

- **Python** (67.3%) - Lógica principal de la aplicación usando Flask
- **Dockerfile** (32.7%) - Configuración de contenedorización

### Dependencias principales
- **Flask 3.0.0** - Framework web para crear la API REST

## ✨ Características

- 🚀 API REST basada en Flask
- 🐳 Completamente containerizada con Docker
- 🏥 Endpoint de health check para verificar el estado
- 📨 Endpoint simple que retorna mensajes en JSON
- 🔧 Imagen Docker basada en Python 3.11-slim (optimizada)
- 🌐 Servidor accesible en puerto 5000

## 📦 Instalación

### Opción 1: Ejecutar localmente con Python

```bash
# Clonar el repositorio
git clone https://github.com/Eduardo123as/docker-api.git
cd docker-api/docker-api

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar la aplicación
python app.py
```

### Opción 2: Ejecutar con Docker

```bash
# Clonar el repositorio
git clone https://github.com/Eduardo123as/docker-api.git
cd docker-api/docker-api

# Construir la imagen de Docker
docker build -t docker-api .

# Ejecutar el contenedor
docker run -p 5000:5000 docker-api
```

## 🚀 Uso

Una vez que la aplicación esté en ejecución, accede a los siguientes endpoints:

### Endpoint Principal
```bash
curl http://localhost:5000/
# Respuesta: {"message": "Hola desde docker"}
```

### Health Check
```bash
curl http://localhost:5000/health
# Respuesta: {"status": "ok"}
```

## 📁 Estructura del Proyecto

```
docker-api/
├── Dockerfile              # Definición del contenedor Docker
├── requirements.txt        # Dependencias de Python
├── README.md              # Este archivo
└── app.py                 # Aplicación Flask principal
```

## 🔧 Configuración de Docker

El `Dockerfile` utiliza:
- **Imagen base**: `python:3.11-slim` - Versión ligera de Python 3.11
- **Puerto expuesto**: 5000
- **Directorio de trabajo**: /app
- **Comando de inicio**: `python app.py`

## 📝 Notas

- La aplicación se ejecuta en modo debug cuando se inicia localmente
- El servidor escucha en todas las interfaces de red (0.0.0.0)
- Accesible a través del puerto 5000

---

**Hecho con ❤️ por Eduardo123as**
