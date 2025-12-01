# Proyecto Backend - API de Recuperación y Cambio de Contraseña

Este proyecto implementa una API para la recuperación y cambio de contraseña mediante endpoints que permiten solicitar un restablecimiento de contraseña y establecer una nueva.

---

## Endpoints

### 1. POST `/api/recuperarpassword`

- **Descripción:**  
  Este endpoint recibe el correo electrónico del usuario para enviarle instrucciones de recuperación de contraseña.  
- **Request Body (JSON):**

```json
{
  "email": "usuario@ejemplo.com"
}
