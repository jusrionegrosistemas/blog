# Aplicación Blog de Ejemplo

## Requisitos
- PHP 8.1 (con la librería GD para procesar imagenes), Composer y Nodejs.
- Si preferis usar docker, fijate la última sección.
## Instalación
- git clone https://github.com/jusrionegrosistemas/blog.git blog-ejemplo
- cd blog-ejemplo
- npm install && npm run build
- crear en el directorio /database, el archivo `database.sqlite`
- - Linux: touch database/database.sqlite
- - Windows: cd database y luego echo.> database.sqlite
- - Si quisieran usar otra DB, hay que configurar el archivo `.env` a gusto.
- crear carpeta `blog_images` en el directorio `public`
- composer install
- php artisan migrate;
- php artisan serve --host=0.0.0.0
- http://TU_IP:8000/
- - Ir a Registrarse
- - Crear un usuario cualquier
- Una vez logueado, ir a: http://TU_IP:8000/blog_admin/setup y aprentar el boton "SETUP PACKAGE".
- **Importante**: La búsqueda dentro del admin panel no funciona. No la vamos a usar.

## Blog
- Admin panel: http://TU_IP:8000/blog_admin
- Blog: http://TU_IP:8000/en/blog

## Si usas Docker
```yml
FROM php:8.1

RUN apt-get update && apt-get install -y \
    libzip-dev \
    zip \
    git \
    npm \
    && docker-php-ext-install zip

#instalar composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer

RUN apt-get install -y libpng-dev
RUN docker-php-ext-install gd
``` 
## Creditos 

Fork de: https://github.com/binshops/laravel-blog