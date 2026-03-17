# 📦 Jumbox - Sistema de Gestión de Supermercado

Jumbox es una aplicación web desarrollada en Python que simula el funcionamiento de un sistema de gestión para supermercados con múltiples sucursales. Permite administrar productos, stock, pedidos, usuarios y compras de clientes.

> 📚 Este proyecto fue desarrollado como trabajo académico, con el objetivo de aplicar conceptos de desarrollo web, bases de datos y arquitectura de software.

---

## 🚀 Características principales

- 🏪 Gestión de sucursales
- 📦 Control de stock desde depósito central
- 🛒 Sistema de compras con carrito
- 👤 Registro e inicio de sesión de usuarios
- 🧑‍💼 Panel de administrador
- 📊 Estadísticas y gestión de solicitudes
- 🔄 Pedidos de sucursales al depósito
- 📦 Envíos desde depósito a sucursales

---

## 🧱 Arquitectura del proyecto

El proyecto sigue una estructura modular basada en Flask:

```
Jumbox-Python-main/
│
├── app/
│   ├── admin/        # Funcionalidades del administrador
│   ├── auth/         # Login, registro y autenticación
│   ├── main/         # Rutas principales
│   ├── sucursal/     # Gestión de sucursales
│   ├── user/         # Funcionalidades del cliente
│   ├── utils.py      # Funciones auxiliares
│
├── templates/        # Vistas HTML organizadas por módulos
├── static/           # CSS e imágenes
├── run.py            # Punto de entrada de la app
├── requirements.txt  # Dependencias
├── jumbox.db         # Base de datos SQLite
└── bd.jumbox.py      # Script de base de datos
```

---

## 🛠️ Tecnologías utilizadas

| Tecnología    | Uso                 |
| ------------- | ------------------- |
| 🐍 Python     | Backend principal   |
| 🌐 Flask      | Framework web       |
| 🗄️ SQLite     | Base de datos       |
| 🎨 HTML + CSS | Interfaz de usuario |

---

## ⚙️ Instalación y ejecución

### 1. Clonar el repositorio

```bash
git clone https://github.com/tuusuario/jumbox.git
cd jumbox
```

### 2. Crear entorno virtual _(opcional pero recomendado)_

```bash
python -m venv venv
source venv/bin/activate   # Linux/Mac
venv\Scripts\activate      # Windows
```

### 3. Instalar dependencias

```bash
pip install -r requirements.txt
```

### 4. Ejecutar la aplicación

```bash
python run.py
```

### 5. Abrir en el navegador

```
http://localhost:5000
```

---

## 👥 Tipos de usuarios

### 🧑‍💼 Administrador

- Gestiona productos
- Visualiza estadísticas
- Administra solicitudes

### 🏪 Sucursal

- Consulta stock
- Realiza pedidos al depósito
- Gestiona pedidos de clientes

### 👤 Cliente

- Se registra e inicia sesión
- Compra productos
- Maneja carrito

---

## 🔄 Flujo del sistema

```
Cliente → selecciona sucursal
       → agrega productos al carrito
       → realiza la compra
             ↓
Sucursal → procesa el pedido
         → si no hay stock, solicita al depósito
               ↓
Depósito → arma el envío
         → se actualizan los stocks automáticamente
```

---

## 📌 Funcionalidades destacadas

- Separación por módulos (`admin`, `user`, `sucursal`, `auth`)
- Persistencia de datos con SQLite
- Sistema completo de carrito de compras
- Interfaz web simple y funcional
- Escalable para futuras mejoras

---

## 📄 Licencia

Este proyecto es de uso educativo y puede ser modificado libremente.

---
