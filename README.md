# 📚 Biblioteca Project - Gestión de Préstamos

![Django](https://img.shields.io/badge/Django-092E20?style=for-the-badge&logo=django&logoColor=white)
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bootstrap](https://img.shields.io/badge/Bootstrap-7952B3?style=for-the-badge&logo=bootstrap&logoColor=white)
![SQLite](https://img.shields.io/badge/SQLite-07405E?style=for-the-badge&logo=sqlite&logoColor=white)

Este proyecto es un sistema de gestión de biblioteca desarrollado como parte del **Bootcamp Full Stack Python**. Permite administrar socios, libros, editoriales y el historial detallado de préstamos utilizando el potente ORM de Django.

---

## 🚀 Características Principales

* **Modelado Complejo:** Uso de relaciones `OneToOne`, `ForeignKey` y `ManyToMany` con tablas intermedias personalizadas (`through="Prestamo"`).
* **Optimización de Consultas:** Implementación de `select_related` y `prefetch_related` en las vistas para minimizar el impacto en la base de datos (evitando el problema N+1).
* **Interfaz Responsiva:** Diseño limpio y moderno utilizando **Bootstrap 5.3**.
* **Validación de Datos:** Uso de validadores integrados como `MinValueValidator` e integridad referencial con `UniqueConstraint`.

---

## 🛠️ Tecnologías Utilizadas

* **Backend:** Python 3 & Django Framework.
* **Frontend:** HTML5, Jinja2 Templates y Bootstrap 5.
* **Base de Datos:** SQLite (Entorno de desarrollo).

---

## 📦 Estructura del Modelo de Datos

El núcleo del sistema se basa en los siguientes modelos:
* **Socio:** Extensión del modelo `User` de Django mediante `OneToOneField`.
* **Libro:** Registro central que vincula categorías y editoriales.
* **Prestamo:** Tabla intermedia que gestiona la relación entre socios y libros, registrando fechas y estados (Prestado, Devuelto, Atrasado).
* **Editorial & Categoria:** Modelos maestros para la clasificación.

---

## 🔧 Instalación y Configuración

Sigue estos pasos para ejecutar el proyecto localmente:

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/CastilloFJ/biblioteca_project.git](https://github.com/CastilloFJ/biblioteca_project.git)
   cd biblioteca_project

2. **Crear y activar entorno virtual:*
   ```bash
   python -m venv venv
   # En Windows:
   venv\Scripts\activate

3. **Instalar Django:**
   ```bash
   pip install django
   
4. **Aplicar migraciones:**
   ```bash
   python manage.py migrate
   
5. **Iniciar el servidor:**
   ```bash
   python manage.py runserver

Visita [http://127.0.0.1:8000/](http://127.0.0.1:8000/) en tu navegador.

---

## 📝 Instrucciones de Uso

* **Listado de Libros:** Accede a la raíz para ver todos los libros disponibles, su ISBN y editorial.
* **Detalle del Libro:** Consulta el historial de préstamos asociados a cada ejemplar específico.
* **Panel de Administración:** Accede a `/admin` para gestionar la base de datos (requiere un superusuario creado con `python manage.py createsuperuser`).

---

## 👨‍🏫 Autor

**José Castillo** *Profesor de Química | Desarrollador Full Stack | Aprendiz Eterno*

> **Nota:** Este proyecto fue realizado con fines educativos durante el proceso de aprendizaje en el ecosistema Python/Django dentro del Bootcamp Full Stack Python.
