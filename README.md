# Bank Application - Microservices

Sistema bancario basado en microservicios desarrollado con Spring Boot.

## 🏗️ Arquitectura

El proyecto está dividido en 2 microservicios independientes:

- **Client Service** (Puerto 8001): Gestión de clientes y personas
- **Account Service** (Puerto 8000): Gestión de cuentas bancarias y transacciones

## 🚀 Tecnologías

- Java 11
- Spring Boot 2.4.2
- Spring Data JPA
- H2 Database (en memoria)
- Maven
- Lombok

## 📦 Estructura del Proyecto
```
BankApplication/
├── client/          # Microservicio de clientes
│   ├── controller/
│   ├── service/
│   ├── repository/
│   └── model/
└── account/         # Microservicio de cuentas
    ├── controller/
    ├── service/
    ├── repository/
    └── model/
```

## ⚙️ Ejecución

### Client Service
```bash
cd client
mvn spring-boot:run
```
Disponible en: `http://localhost:8001`

### Account Service
```bash
cd account
mvn spring-boot:run
```
Disponible en: `http://localhost:8000`

## 📡 Endpoints Principales

### Client Service
- `POST /api/clients` - Crear cliente
- `GET /api/clients` - Listar clientes
- `GET /api/clients/{id}` - Obtener cliente
- `PUT /api/clients/{id}` - Actualizar cliente
- `PATCH /api/clients/{id}` - Actualización parcial
- `DELETE /api/clients/{id}` - Eliminar cliente

### Account Service
- `POST /api/accounts` - Crear cuenta
- `GET /api/accounts` - Listar cuentas
- `POST /api/transactions` - Crear transacción
- `GET /api/transactions/clients/{id}/report` - Reporte de estado de cuenta

## 🔍 Funcionalidades

✅ CRUD completo de clientes, cuentas y transacciones  
✅ Registro automático de transacciones con actualización de saldo  
✅ Validación de saldo disponible antes de retiros  
✅ Generación de reportes de estado de cuenta por rango de fechas  
✅ Manejo de excepciones personalizado  
✅ Tests unitarios e integración

## 📮 Colección Postman

El archivo `collection_bank_postman.json` contiene todos los endpoints configurados para pruebas.

## 🧪 Tests
```bash
mvn test
```

## 👨‍💻 Autor

Desarrollado como parte de una evaluación técnica de Spring Boot y Microservicios.
```

**Enlace de tu repositorio:**
```
https://github.com/danpv95/bank-application-microservices
