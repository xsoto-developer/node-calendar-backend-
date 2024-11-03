# Node.js Calendar Backend

## Descripción
Este proyecto es un backend para una aplicación de calendario, desarrollado en Node.js y Express, con MongoDB como base de datos. La API permite gestionar eventos de calendario y autenticación de usuarios utilizando JSON Web Tokens (JWT). Incluye un CRUD completo de eventos, con validaciones automáticas y personalizadas, además de un despliegue en Railway para un fácil acceso en la nube.

¡Explora la aplicación en acción!
https://react-mern-backend-test.up.railway.app/

Credenciales de Acceso (para pruebas)

- **Usuario**: demo_user
- **Contraseña**: demo_pass

Usa estas credenciales para acceder a la versión de prueba de la aplicación.

## Funcionalidades Principales
**1. Autenticación de Usuarios:** Login seguro utilizando JWT y revalidación de tokens para mantener sesiones activas.
**2. CRUD de Eventos de Calendario:** Creación, lectura, actualización y eliminación de eventos almacenados en MongoDB.  
**3. Validaciones:**  Validaciones automáticas y personalizadas para garantizar la integridad de los datos.

## Tecnologías y Estructura
### Backend
- **Node.js:** Plataforma para ejecutar JavaScript en el backend.
- **Express:** Framework para construir y gestionar la API RESTful.
- **MongoDB:** Base de datos NoSQL para almacenar usuarios y eventos.
-- **MongoAtlas:** Base de datos en la nube para la administración de datos.
-- **MongoCompass:** Herramienta GUI para gestionar y explorar la base de datos localmente.

### Estructura y Componentes Clave
- **Modelos:** Definición de los esquemas de datos utilizando Mongoose.
- **Controllers:** Controladores para gestionar las operaciones del CRUD de eventos y autenticación.
- **Middlewares de Express:** Funciones intermedias para manejar autenticación, validación y permisos.
- **JWT (JSON Web Token):** Gestión de sesiones con tokens para autenticación pasiva y revalidación automática.
- **Encriptación:** Para almacenamiento seguro de contraseñas y protección de datos sensibles.
- **Rutas:** Definición de rutas de la API para acceso a los servicios.
- **CORS:** Configuración de CORS para permitir el acceso seguro desde el frontend.

## Configuración de Eventos
- **Inserción, Actualización y Eliminación de Eventos:** La API permite realizar operaciones CRUD en eventos de calendario, integrando validaciones y comprobaciones para evitar inconsistencias de datos.
- **Payloads y Validaciones Personalizadas:** Cada operación en eventos cuenta con validaciones específicas para mantener la integridad de los datos y evitar conflictos de fechas.

## Despliegue en Railway
Este backend se despliega en Railway, un servicio en la nube para aplicaciones de Node.js. Los pasos realizados para el despliegue son:

- **Configuración de Railway:** Creación de un proyecto en Railway y configuración para Node.js.
- **Subida a GitHub:** Repositorio de control de versiones con integración continua hacia Railway.
- **Configuración de Variables de Entorno:** Configuración de secretos y variables de entorno para acceso a MongoDB y manejo de tokens.
- **Prueba del Backend en la Nube:** Verificación del funcionamiento completo del backend en Railway, garantizando accesibilidad desde el frontend.

**Nota: Las instrucciones detalladas para la instalación y despliegue se encuentran en las secciones siguientes.**

## Instalación y Configuración Local

### 1. Clonar el repositorio:
```
git clone https://github.com/xsoto-developer/node-calendar-backend.git
```
### 2. Instala las dependencias:
```
npm install
```
### 3. Renombrar el archivo de configuración:
- Cambiar el nombre del archivo `env.template` a `.env.`

### 2. Configurar las Variables de Entorno:
- Revise el apartado de Configuración de Variables de Entorno

### 4. Ejecutar en modo desarrollo:   
```
npm start
```
### Ejecuta la aplicación en el modo de desarrollo
Abre [http://localhost:4000] para verla en tu navegador.

## Configuración de Variables de Entorno
Para ejecutar este proyecto Node.js correctamente, es necesario configurar las siguientes variables de entorno en un archivo `.env.`. Estas variables permiten establecer la conexión con la base de datos, definir el puerto de ejecución y gestionar la autenticación mediante JWT.

Asegúrate de cambiar los valores entre `{ }` por los valores correctos según tu configuración:
```
# Puerto en el que el servidor escuchará las peticiones
PORT=4000

# Cadena de conexión a MongoDB
DB_CNN=mongodb+srv://{USER}:{PASSWORD}@cluster0.spaa6.mongodb.net/{NAME_BD}

# Clave secreta para firmar los JWT (JSON Web Tokens)
SECRET_JWT_SEED={SECRET}
```
### Explicación de cada variable
- `PORT`: El puerto en el cual el servidor escuchará las peticiones. Puedes cambiarlo a cualquier puerto disponible (por ejemplo, 4000).
- `DB_CNN`: La URL de conexión a MongoDB en la nube. Reemplaza `{USER}`, `{PASSWORD}`, y `{NAME_BD}` con el nombre de usuario, contraseña y nombre de la base de datos de tu MongoDB. Asegúrate de configurar correctamente los permisos en MongoDB Atlas para el acceso.
- `SECRET_JWT_SEED`: Un valor secreto para firmar y validar los JWT. Este valor debe ser una cadena aleatoria y segura, ya que se usa para la autenticación de usuarios.

**Importante: Nunca compartas tu archivo .env ni subas este archivo al control de versiones, ya que contiene información sensible para el funcionamiento de la aplicación.**

