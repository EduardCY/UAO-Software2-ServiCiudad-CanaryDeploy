# 🏢 UAO - SERVICIUDAD Cali: Sistema Empresarial con Despliegues Canarios (Canary Deploy)

[![UAO](https://img.shields.io/badge/Universidad-Aut%C3%B3noma_de_Occidente-red?style=for-the-badge&logo=academia)](https://www.uao.edu.co/)
[![Materia](https://img.shields.io/badge/Asignatura-Ingenier%C3%ADa_de_Software_2-blue?style=for-the-badge)](https://github.com/EduardCY/UAO-Software2-ServiCiudad-CanaryDeploy)
[![Spring Boot](https://img.shields.io/badge/Backend-Spring_Boot_3-6DB33F?style=for-the-badge&logo=springboot)](https://spring.io/)
[![Docker](https://img.shields.io/badge/Contenedores-Docker_Compose-2496ED?style=for-the-badge&logo=docker)](https://www.docker.com/)
[![Nginx](https://img.shields.io/badge/Proxy_Inverso-NGINX_Canary-009639?style=for-the-badge&logo=nginx)](https://nginx.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)
[![Author](https://img.shields.io/badge/Author-Eduard_Criollo_Yule-purple?style=for-the-badge&logo=github)](https://github.com/EduardCY)

> **Sistema de Información Empresarial para la Gestión de Servicios Públicos y Ciudadanos (`SERVICIUDAD-CALI`)**, implementado con arquitectura Spring Boot, PostgreSQL, contenedorización Docker y una estrategia de **Despliegue Canario (Canary Deployment)** ponderado con NGINX para actualización sin caída de servicio (*Zero-Downtime Deployment*).

---

## 🎯 Arquitectura de Despliegue Canario (Canary Routing)

```mermaid
flowchart TD
    Users[👥 Tráfico de Usuarios Externos] --> Nginx[NGINX Reverse Proxy & Load Balancer]
    
    Nginx -->|90% del Tráfico| Prod[Servidor Producción Estable v1.0
Spring Boot Backend]
    Nginx -->|10% del Tráfico| Canary[Servidor Canario Experimental v2.0
Spring Boot Backend]
    
    Prod --> DB[(PostgreSQL Database)]
    Canary --> DB
    
    Metrics[Sistema de Telemetría & Logs] -. Audita Errores .-> Canary
```

---

## 📁 Estructura del Repositorio

* **[`SERVICIUDAD-CALI/`](SERVICIUDAD-CALI/)**: Aplicación Spring Boot completa (`pom.xml`, endpoints REST, lógica de negocio, migraciones SQL, suites de prueba y configuraciones de Docker Compose).
* **[`ProyectoFinal_Original/`](ProyectoFinal_Original/)**: Justificación teórica, informes de calidad de software y documentación académica de soporte.

---

## 🚀 Puesta en Marcha

```bash
git clone https://github.com/EduardCY/UAO-Software2-ServiCiudad-CanaryDeploy.git
cd UAO-Software2-ServiCiudad-CanaryDeploy/SERVICIUDAD-CALI

# Ejecutar con Docker Compose
docker compose up -d --build
```

---

## 👨‍💻 Autor

* **Autor:** Eduard Criollo Yule ([@EduardCY](https://github.com/EduardCY))
* **Licencia:** [MIT](LICENSE).
