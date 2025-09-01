
# configData_wingTrip

Servidor de configuración centralizada para los microservicios del proyecto Wing Trip - Sistema de reservas de vuelos.

## 📋 Estado del Proyecto

**Configuraciones Activas (Completadas):**

-   `api-gateway.yml` - Gateway de API configurado y funcionando
-   `api-user.yml` - Microservicio de usuarios (100% funcional)

**Configuraciones en Desarrollo:**

-   `api-booking.yml` - Microservicio de reservas (CRUD básico en progreso)

**Configuraciones Pendientes:**

-   `api-payment.yml` - Sistema de pagos + Resilience4j + MySQL
-   `api-flight.yml` - Catálogo de vuelos + MongoDB
-   `api-seat.yml` - Gestión de asientos + MongoDB + Feign
-   `api-flight-details.yml` - Detalles de vuelos + MongoDB
-   `keycloak.yml` - Autenticación centralizada

## 🏗️ Arquitectura

Este servidor de configuración centralizada soporta la arquitectura de microservicios usando **Spring Cloud Config Server**, actualmente configurado para:

-   **Desarrollo** (dev) - Ambiente principal de trabajo

## 📁 Estructura de Configuraciones

```
configData_wingTrip/
├── api-gateway.yml          # ✅ Gateway principal
├── api-user.yml             # ✅ Gestión de usuarios
├── api-booking.yml          # 🔄 Reservas (en desarrollo)
└── [futuras configuraciones para otros microservicios]

```

## 🚀 Uso

Las configuraciones se cargan automáticamente por cada microservicio al arrancar, conectándose a:

```
http://localhost:8888/{microservice-name}/{profile}

```

## 🎯 Proyecto Personal

Parte del proyecto **Wing Trip** - un sistema completo de reservas de vuelos desarrollado como proyecto personal de aprendizaje en arquitecturas de microservicios.

### Tecnologías Integradas:

-   Spring Cloud Config Server
-   Docker Compose para desarrollo
-   Service Discovery con Eureka
-   API Gateway
-   Próximamente: RabbitMQ, MongoDB, Resilience4j, Keycloak
