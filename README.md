# 🚀 Sistema de Gestión de Microservicios - Proyecto Fullstack

Proyecto desarrollado como parte de la formación en IT en el **DUOC**. Este sistema implementa una arquitectura robusta de **microservicios** para la gestión integral de ventas, catálogo de productos y usuarios.

## 👥 Equipo de Desarrollo
* **Kevin Sosa**
* **Jaime Rodriguez**

## 🏗️ Estructura del Proyecto
El sistema está compuesto por servicios independientes comunicados vía **Spring Cloud**:
* **Config-Server**: Servidor de configuración centralizada.
* **Eureka-Server**: Service Discovery.
* **Api-Gateway**: Punto de entrada centralizado.
* **Microservicios**: `usuario-service`, `producto-service`, `carrito-service`, `pagos-service`, `facturaciones-service`, `inventario-service`, `transporte-service`, `notificaciones-service`.

## ⚙️ Tecnologías Utilizadas
* **Java 25** con **Spring Boot**.
* **Spring Cloud** (Config, Eureka, Gateway, OpenFeign).
* **JPA/Hibernate** con base de datos **MySQL**.
* **Lombok** para optimización de código.
* **Docker & Docker Compose** para la contenedorización y orquestación.

## 📖 Documentación de la API (Swagger)
La documentación interactiva de los endpoints está disponible a través de Swagger. El puerto de acceso dependerá del entorno desde donde levantes el ecosistema:

* 💻 **Ejecución local (IntelliJ IDEA):** `http://localhost:9000/swagger-ui.html`
* 🐳 **Ejecución con Docker:** `http://localhost:9090/swagger-ui.html`

## 🐳 Despliegue con Docker (Docker Compose)
Para levantar todo el ecosistema (bases de datos MySQL independientes y microservicios) de forma automatizada:

1. Sitúate en la raíz del proyecto donde está el archivo `docker-compose.yml`.
2. Ejecuta el siguiente comando para compilar y levantar los contenedores:
```bash
   docker-compose up --build
   ```
3. Para detener y bajar los contenedores:
```bash
   docker-compose down
   ```

## 🚀 Guía de Inicio Manual (Orden de ejecución)
Si prefieres levantar el ecosistema a mano desde tu IDE, es vital seguir este orden:

1. Iniciar **Config-Server**.
2. Iniciar **Eureka-Server**.
3. Iniciar los **microservicios restantes**.
4. Iniciar **Api-Gateway**.

## 📡 Endpoints principales (Ejemplos)
* **Listar productos**: `GET http://localhost:9000/api/v1/productos` *(O usa el puerto `9090` si levantaste con Docker)*
* **Crear producto**: `POST http://localhost:9000/api/v1/productos` *(O usa el puerto `9090` si levantaste con Docker)*

---
> *"Lo único que importa es ganar."* — Inspirado por Harvey Specter, pero construido con el código de Kevin y Jaime.
