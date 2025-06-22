# Jumex

**Jumex** es una plataforma web para el análisis inteligente de vulnerabilidades en componentes de software, basada en **SBOM (Software Bill of Materials)** y potenciada con **Inteligencia Artificial**. Permite a los usuarios evaluar la seguridad de sus proyectos cruzando datos con bases como **CVE/NVD**, priorizando según criterios personalizados.

## Características principales

- Subida de proyectos con SBOM para análisis automático.
- Evaluación mediante IA basada en criterios definidos por el usuario.
- Integración con bases de datos de vulnerabilidades (CVE/NVD).
- Interfaz web intuitiva para visualización de resultados.
- Arquitectura de microservicios con Docker Compose.

## Tecnologías utilizadas

- Python + Flask
- MariaDB + SQLAlchemy
- Flask-Praetorian (autenticación y roles)
- Google Generative AI (para análisis con IA)
- Docker y Docker Compose

## Estructura del proyecto

```text
JumeX/
├── docker-compose.mac.yaml         # Versión para macOS con procesador M1/M2/M3
├── docker-compose.windows.yaml     # Versión para sistemas Windows (x86_64)
└── proyecto_web/
    ├── api/       # Microservicio de gestión de datos y seguridad
    ├── chat/      # Microservicio de IA para análisis de SBOM
    └── web/       # Frontend Flask con la interfaz de usuario
```

## Instalación y ejecución

### Requisitos

- [Docker](https://www.docker.com/)
- [Docker Compose](https://docs.docker.com/compose/)

### Iniciar el proyecto

**Para sistemas macOS con chip M1/M2/M3:**

```bash
docker compose -f docker-compose.mac.yaml up --build
```

**Para sistemas Windows o procesadores x86_64:**

```bash
docker compose -f docker-compose.windows.yaml up --build
```

### Servicios disponibles

| Servicio           | URL                    |
|--------------------|------------------------|
| Interfaz Web       | http://localhost:5010  |
| phpMyAdmin         | http://localhost:8080  |

## Estado actual

- [x] Arquitectura de microservicios operativa
- [x] Análisis de SBOM con IA funcional
- [x] Comunicación entre microservicios asegurada
- [ ] Despliegue en la nube
- [ ] Sistema de login por interfaz

## Licencia

Este proyecto se desarrolla en el marco del curso de **Ingeniería del Software Seguro**.

Pull requests y sugerencias son bienvenidas.
