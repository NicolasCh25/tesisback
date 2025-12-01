# 💻 Proyecto Backend - API de Gestión de Usuarios y Recuperación de Contraseña  

*Escuela:* Escuela Politécnica Nacional  
*Carrera:* Desarrollo de Software  
*Asignatura:* Desarrollo de Aplicaciones Web  
*Profesor:* Ing. Byron Loarte  
*Período Académico:* 2025B  
*Grupo:* 3  
*Integrantes:*  
- Nicolás Chiguano  
- Adrian Ramos  
- Edison Escobar  

---

## 🧩 Descripción del proyecto

Este proyecto implementa una API backend para gestión de usuarios que incluye registro, confirmación de cuenta por correo, recuperación y cambio de contraseña, así como autenticación y gestión del perfil de administrador.

---

## 🚀 Endpoints disponibles

### 1. POST `/registro`

- **Funcionalidad:**  
  Registra un nuevo usuario y envía un correo de confirmación con un token para validar la cuenta.  
- **Request Body:**  
  Datos del usuario para registro.  
- **Respuesta:**  
  Confirmación del registro y envío de correo.

<!-- Inserta imagen POST registro -->
![Registro](https://github.com/NicolasCh25/tesisback/blob/main/registro.png?raw=true)

---

### 2. GET `/confirmar/:token`

- **Funcionalidad:**  
  Valida el token enviado al correo para activar la cuenta de usuario.  
- **Parámetros:**  
  `:token` recibido en el correo.  
- **Respuesta:**  
  Confirmación de cuenta activada.

<!-- Inserta imagen GET confirmar -->
![Confirmar Cuenta](./imagenes/confirmar.png)

---

### 3. POST `/recuperarpassword`

- **Funcionalidad:**  
  Envía un correo para recuperar la contraseña al usuario que lo solicite.  
- **Request Body:**  
  Email del usuario.  
- **Respuesta:**  
  Mensaje confirmando envío de correo.

<!-- Inserta imagen POST recuperarpassword -->
![Recuperar Password]([./imagenes/recuperarpassword.png](https://github.com/NicolasCh25/tesisback/blob/main/recuperarpassword.png?raw=true))

---

### 4. GET `/recuperarpassword/:token`

- **Funcionalidad:**  
  Verifica que el token para cambiar la contraseña sea válido y no haya expirado.  
- **Parámetros:**  
  `:token` recibido por correo.  
- **Respuesta:**  
  Confirmación o error de validación.

<!-- Inserta imagen GET comprobar token -->
![Comprobar Token Password](./imagenes/comprobartokenpassword.png)

---

### 5. POST `/nuevopassword/:token`

- **Funcionalidad:**  
  Establece una nueva contraseña para el usuario validando el token recibido.  
- **Parámetros:**  
  `:token` para validar la acción.  
- **Request Body:**  
  Nueva contraseña y confirmación.  
- **Respuesta:**  
  Confirmación de cambio exitoso.

<!-- Inserta imagen POST nuevopassword -->
![Nuevo Password](./imagenes/nuevopassword.png)

---

### 6. POST `/administrador/login`

- **Funcionalidad:**  
  Permite al administrador iniciar sesión y recibir un token JWT para autenticación.  
- **Request Body:**  
  Credenciales de administrador.  
- **Respuesta:**  
  Token JWT y datos del administrador.

<!-- Inserta imagen POST login -->
![Login Administrador](./imagenes/login.png)

---

### 7. GET `/administrador/perfil`

- **Funcionalidad:**  
  Obtiene el perfil del administrador usando el token JWT para validar la sesión.  
- **Headers:**  
  Token JWT en autorización.  
- **Respuesta:**  
  Datos del perfil.

<!-- Inserta imagen GET perfil -->
![Perfil Administrador](./imagenes/perfil.png)

---

### 8. PUT `/actualizarperfil/:id`

- **Funcionalidad:**  
  Actualiza los datos del perfil del administrador identificado por ID, validando el token JWT.  
- **Parámetros:**  
  ID del administrador.  
- **Request Body:**  
  Nuevos datos del perfil.  
- **Headers:**  
  Token JWT en autorización.  
- **Respuesta:**  
  Confirmación de actualización.

<!-- Inserta imagen PUT actualizar perfil -->
![Actualizar Perfil](./imagenes/actualizarperfil.png)

---

### 9. PUT `/actualizarpassword/:id`

- **Funcionalidad:**  
  Cambia la contraseña del administrador identificado por ID, validando el token JWT.  
- **Parámetros:**  
  ID del administrador.  
- **Request Body:**  
  Contraseña actual y nueva.  
- **Headers:**  
  Token JWT en autorización.  
- **Respuesta:**  
  Confirmación de cambio de contraseña.

<!-- Inserta imagen PUT actualizar password -->
![Actualizar Password](./imagenes/actualizarpassword.png)

---

## ⚙️ Tecnologías utilizadas

- Node.js  
- Express.js  
- JWT para autenticación  
- SMTP para envío de correos  
- Base de datos (indicar cuál usas si quieres)  

---

## 📂 Organización del proyecto

- Carpeta `routes/` para definir rutas.  
- Controladores para manejar la lógica de cada funcionalidad.  
- Middleware para verificar tokens JWT y seguridad.  

---

## Autor

Nicolás Chiguano  
