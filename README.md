# 🏙️ SERVICIUDAD-CALI — Sistema Empresarial con Despliegue Canary y CI/CD

> **Proyecto Insignia — Ingeniería de Software 2 (UAO)**  
> Plataforma empresarial de gestión de servicios ciudadanos con arquitectura de microservicios, pipeline de integración y entrega continua (CI/CD) automatizado y estrategia de despliegue progresivo (*Canary Deployment*).

---

## 🚀 Características Arquitectónicas
* **Despliegue Canary:** Enrutamiento ponderado de tráfico con Docker Compose (`docker-compose-canary.yml`) para validar nuevas versiones en producción con riesgo mínimo.
* **Pipeline de CI/CD (GitHub Actions):** `.github/workflows/ci-cd.yml` con etapas de linting, testing automatizado, construcción de imágenes Docker y auditoría de seguridad.
* **Suite de Pruebas de Integración:** Colecciones completas de Postman (`ServiCiudad_API.postman_collection.json`) y entornos parametrizados (`ServiCiudad_Docker.postman_environment.json`).
* **Monitoreo y Métricas:** Tableros preconfigurados en Grafana con visualización de estado de servicios y métricas de rendimiento.

---

## 🛠️ Stack Tecnológico
* **Backend:** Node.js / Express, Docker, Docker Compose
* **CI/CD:** GitHub Actions, Postman Newman CLI
* **Monitoreo:** Grafana, Prometheus
* **Pruebas:** Jest, Postman API Testing

---
*Universidad Autónoma de Occidente — Ingeniería de Software 2.*
