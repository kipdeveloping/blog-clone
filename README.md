# Django Blog Project

Este es un proyecto de aplicación web de un Blog simple y funcional desarrollado con **Django**. Permite a los usuarios registrarse, iniciar sesión y gestionar sus propias publicaciones mediante operaciones CRUD (Crear, Leer, Actualizar, Eliminar).

## 🚀 Características (Features)

*   **Autenticación de Usuarios:**
    *   Registro de nuevos usuarios.
    *   Inicio de sesión (Login) y Cierre de sesión (Logout) utilizando el sistema de autenticación integrado de Django.
*   **Gestión de Publicaciones (CRUD completo):**
    *   **Crear:** Los usuarios autenticados pueden crear nuevas publicaciones.
    *   **Leer:** 
        *   Vista de lista para ver todas las publicaciones (`ListView`).
        *   Vista de detalle para leer el contenido completo de una publicación específica (`DetailView`).
    *   **Actualizar:** Posibilidad de editar publicaciones existentes (`UpdateView`).
    *   **Eliminar:** Opción para borrar publicaciones (`DeleteView`).
*   **Vistas Basadas en Clases (CBVs):** El proyecto hace uso extensivo de las vistas genéricas de Django para un código más limpio y mantenible.
*   **Relación de Modelos:** Cada publicación está vinculada a su autor (Usuario) mediante una clave foránea.

## 🛠️ Requisitos previos

*   Python 3.x
*   Django (Las versiones específicas se encuentran en `requirements.txt`)

## ⚙️ Instalación y Configuración

Sigue estos pasos para ejecutar el proyecto en tu entorno local:

1.  **Clonar el repositorio:**
    ```bash
    git clone <url-del-repositorio>
    cd blog-aug
    ```

2.  **Crear y activar un entorno virtual (recomendado):**
    *   En Windows:
        ```bash
        python -m venv .venv
        .venv\Scripts\activate
        ```
    *   En macOS/Linux:
        ```bash
        python3 -m venv .venv
        source .venv/bin/activate
        ```

3.  **Instalar las dependencias:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Aplicar las migraciones de la base de datos:**
    ```bash
    python manage.py migrate
    ```

5.  **Crear un superusuario (opcional, para acceder al panel de administración):**
    ```bash
    python manage.py createsuperuser
    ```

6.  **Ejecutar el servidor de desarrollo:**
    ```bash
    python manage.py runserver
    ```

7.  **Acceder a la aplicación:**
    Abre tu navegador web y visita `http://127.0.0.1:8000/`. Para el panel de administración, visita `http://127.0.0.1:8000/admin/`.

## 📁 Estructura Principal del Proyecto

*   `django_base/`: Contiene la configuración principal del proyecto Django (`settings.py`, `urls.py`).
*   `blogs/`: Aplicación principal que maneja los modelos, vistas, urls y la lógica del blog (CRUD de posts).
*   `signup/`: Aplicación encargada del registro de nuevos usuarios.
*   `templates/`: Contiene todos los archivos HTML (plantillas) del proyecto para renderizar las vistas.
