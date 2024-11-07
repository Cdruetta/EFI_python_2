
# EFI Práctica Profesionalizante "Python"

**Desarrolladores:**
- Octavio Victorio :computer:
- Druetta Cristian :computer:

---

## Comenzando 🚀

Estas instrucciones te permitirán obtener una copia del proyecto en funcionamiento en tu máquina local para propósitos de desarrollo y pruebas.

### Clonar el proyecto
```bash
git clone git@github.com:Cdruetta/EFI-python.git
```

### Pre-requisitos 📋

Qué necesitas para instalar el software y cómo instalarlo:

1. **Instalar y correr XAMPP**  
   ```bash
   sudo /opt/lampp/lampp start
   ```

2. **Crear una base de datos (DB) en SQL**  
   Abre el navegador y accede a `http://localhost/phpmyadmin/`

3. **Crear el entorno virtual**
   ```bash
   python3 -m venv env
   ```

4. **Activar el entorno virtual**
   ```bash
   source env/bin/activate
   ```

5. **Instalar los requisitos**
   ```bash
   pip install -r requirements.txt
   ```

6. **Correr el proyecto**
   ```bash
   flask run --reload
   ```

---

## Endpoints API 📋

A continuación se describen los endpoints de la API:

### Autenticación y Registro

#### Iniciar sesión

- **Método:** `POST`  
- **Endpoint:** `/login`

**Descripción:**  
Permite al usuario iniciar sesión verificando las credenciales proporcionadas. Si las credenciales son correctas, establece la sesión.

**Ejemplo de cuerpo de solicitud:**
```json
{
    "usuario": "admin",
    "contrasenia": "admin"
}
```

---

#### Registro de usuario 📋

- **Método:** `POST`  
- **Endpoint:** `/register`

**Descripción:**  
Registra un nuevo usuario con un nombre de usuario y una contraseña hasheada.

**Ejemplo de cuerpo de solicitud:**
```json
{
    "usuario": "octavio",
    "contrasenia": "12345678"
}
```

### Gestión de Usuarios

- **Método:** `POST`  
- **Endpoint:** `/usuario`

#### Mostrar Usuarios 📋

**Descripción:**  
Lista todos los usuarios registrados. Solo accesible para administradores.

**Ejemplo de respuesta:**
```json
[
    {
       "id": 1,
       "usuario": "admin",
       "contrasenia": true
    },
    {
       "id": 2,
       "usuario": "octavio",
       "contrasenia": false
    }
    // Otros usuarios (si los hubiese)
]
```

---

### Crear un nuevo usuario (Admin) 📋

- **Método:** `POST`  
- **Endpoint:** `/admin`

**Descripción:**  
Crea un nuevo usuario, accesible solo para usuarios con permisos de administrador.

**Ejemplo de cuerpo de solicitud:**
```json
{
    "usuario": "matias",
    "contrasenia": "matias1234"
}
```

---

## Contribuir

Si deseas contribuir al desarrollo de este proyecto, por favor abre un "issue" o envía un "pull request" con tus cambios.

---

# EFI-python
