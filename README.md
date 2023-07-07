# Aplicación Blog de Ejemplo

## Instalación

- git clone https://github.com/jusrionegrosistemas/blog.git blog-ejemplo
- cd blog-ejemplo
- npm install && npm run build
- crear en el directorio /database, el archivo ```database.sqlite```
- crear carpeta ```blog_images``` en el directorio ```/public```
- composer install
- php artisan migrate;
- php artisan serve --host=0.0.0.0
- http://TU_IP:8000/
- - Ir a Registrarse
- - Crear un usuario cualquier
- Una vez logueado, ir a: http://TU_IP:8000/blog_admin/setup y aprentar el boton "SETUP PACKAGE".

## Creditos 

Fork de: https://github.com/binshops/laravel-blog