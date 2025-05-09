# wagtailboiler

**Boilerplate modular para proyectos con [Wagtail CMS](https://wagtail.org/)**

Este proyecto está pensado como un punto de partida flexible para desarrolladores que trabajan con Wagtail. La idea es tener una base mínima (rama `main`) y luego ramas auxiliares que implementan funcionalidades específicas, como `wagtailmenus`, `django-allauth`, `blog`, etc.

---

## 🚀 ¿Qué incluye la rama `main`?

- Configuración base de Django y Wagtail.
- Separación de settings (`base.py`, `dev.py`, etc.).
- Gestión de variables de entorno con `python-decouple`.
- Estructura limpia y lista para escalar.
- Página inicial mínima con una `HomePage`.

---

## 🌿 Filosofía

Cada funcionalidad adicional vive en su propia rama:
- Puedes hacer `git merge` de las ramas que necesites.
- Evitas incluir cosas que tu proyecto no requiere.
- Mantienes un historial claro y modular.

---

## 🛠️ Cómo empezar

```bash
git clone -b main https://github.com/rypptc/wagtailboiler.git mi_proyecto
cd mi_proyecto

# Crear entorno virtual
python -m venv env
source env/bin/activate  # o env\Scripts\activate en Windows

# Instalar dependencias
pip install -r requirements.txt

# Crear archivo .env
cp .env.example .env

# Migraciones e iniciar el server
python manage.py migrate
python manage.py runserver
```

---

## ➕ Agregar funcionalidades desde ramas auxiliares

Este proyecto sigue una estructura modular. Si quieres extender tu proyecto con funcionalidades adicionales, simplemente puedes hacer merge desde ramas auxiliares. Por ejemplo:

```bash
git remote add boiler https://github.com/rypptc/wagtailboiler.git

git fetch boiler

# Traer la funcionalidad wagtailmenus
git merge boiler/wagtailmenus
```

Cada rama auxiliar está diseñada para ser incorporada de forma opcional y modular.

---

## 🌱 Ejemplo de `.env`

```env
DEBUG=True
SECRET_KEY=tu_clave_secreta
ALLOWED_HOSTS=localhost,127.0.0.1
DB_ENGINE=django.db.backends.sqlite3
DB_NAME=db.sqlite3
ENABLE_WAGTAILMENUS=False
ENABLE_AUTH=False
```

---

## 📦 Funcionalidades planificadas

- [x] Configuración base (`main`)
- [ ] `wagtailmenus`
- [ ] Blog
- [ ] Integración con Django REST
- [ ] Allauth

---

## 📜 Licencia

MIT License – libre para usar, modificar y compartir.

---

> Proyecto creado por [HolaWagtail](https://www.youtube.com/@holawagtail)
