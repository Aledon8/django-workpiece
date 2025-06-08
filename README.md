
---

# Django Project

## 📦 Overview

This project provides a basic Django setup with initial configuration. It includes:

* Django REST Framework for building APIs
* JWT authentication
* CORS support
* Django admin panel
* Settings structure with environment separation
* Core dependencies listed in `requirements.txt`

---

## ⚙️ Installed Dependencies

* `Django`
* `djangorestframework`
* `djangorestframework-simplejwt`
* `django-cors-headers`
* `python-dotenv` *(optional, for environment variables)*

Full dependency list is available in `requirements.txt`.

---

## 🚀 Quick Start

1. **Clone the repository:**

   ```bash
   git clone <your-repo-url>
   cd <your-project>
   ```

2. **Create and activate a virtual environment:**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```

4. **Create a `.env` file (if using environment variables):**

   ```
   DEBUG=True
   SECRET_KEY=your-secret-key
   ALLOWED_HOSTS=127.0.0.1,localhost
   ```

5. **Apply migrations and run the server:**

   ```bash
   python manage.py migrate
   python manage.py runserver
   ```

---

## 🔐 Authentication

This project uses **JWT** for authentication.
To obtain a token:

`POST /api/token/`
Request body:

```json
{
  "username": "your_username",
  "password": "your_password"
}
```

To refresh a token:

`POST /api/token/refresh/`

---

## 🔧 Configuration

The project uses a modular settings structure for different environments:

```
project_name/
│
├── settings/
│   ├── base.py
│   ├── dev.py
│   └── prod.py
```

---

## 🌐 CORS Support

CORS is enabled via `django-cors-headers`. You can configure allowed origins in `settings.py`:

```python
CORS_ALLOWED_ORIGINS = [
    "http://localhost:3000",
    "http://127.0.0.1:3000",
]
```

---

## 🛠 Useful Commands

* Create a superuser:

  ```bash
  python manage.py createsuperuser
  ```

* Freeze dependencies:

  ```bash
  pip freeze > requirements.txt
  ```

---

## 📁 Project Structure

```
project/
│
├── manage.py
├── requirements.txt
├── .env
├── project_name/
│   ├── __init__.py
│   ├── settings/
│   ├── urls.py
│   ├── wsgi.py
│   └── asgi.py
```

---