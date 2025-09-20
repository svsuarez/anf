### 1. Clonar el repositorio
```bash
git clone https://github.com/svsuarez/anf.git
cd anf
```

### 2. Configurar Backend (Laravel)
```bash
# Instalar dependencias Laravel
composer install

# Configurar variables de entorno
cp .env.example .env
```

**En el archivo `.env` configurar conexión a base de datos:**
```env
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=tu_database
DB_USERNAME=tu_usuario
DB_PASSWORD=tu_contraseña
```

```bash
# Generar clave de aplicación
php artisan key:generate

# Ejecutar migraciones
php artisan migrate

# Generar las claves de cifrado
php artisan passport:keys

# Crear un cliente de concesión de credenciales de cliente
php artisan passport:client --client

Los datos proporcionados seran utilizados para obtener token de acceso
```