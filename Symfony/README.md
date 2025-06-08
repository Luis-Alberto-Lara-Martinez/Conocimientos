# Symfony
Aquí se muestran todos los comandos necesarios para hacer un proyecto de Symfony (PHP)
## Crear nuevo proyecto
- Primero descargamos [Composer](https://getcomposer.org/download/), el cual es un gestor de dependencias. Nota: hay que tener una versión de PHP superior a la versión 8.1, sino la tienes instalada en tus variables de entorno, hazlo. Después ejecutamos estos dos comandos en la ruta en la que vayas a querer crear tu proyecto.
```bash
php -r "copy('https://getcomposer.org/installer', 'composer-setup.php');"
```
```bash
php composer-setup.php
```
- Finalmente creamos nuestro proyecto con estos comandos. La opción webapp instala los paquetes necesarios para crear una aplicación web.
```bash
composer create-project symfony/skeleton nombreProyecto
```
```bash
cd nombreProyecto
```
```bash
composer require webapp
```
## Actualizar versión del proyecto
- Con este comando compruebas si alguna de las dependencias que usa tu proyecto tiene alguna actualización disponible.
```bash
composer outdated symfony/*
```
- Con este comando instalas las actualizaciones disponibles.
```bash
composer update symfony/*
```
## Conexión con MySQL
- Este comando ayuda a generar código creando controladores, clases de formulario, etc, para no tener que escribir código repetitivo.
```bash
composer require maker --dev
```
  - Este comando instala el soporte ORM de doctrine.
```bash
composer require doctrine
```
## Comandos útiles para la gestión de la BBDD
- Primero, hay que poner el archivo .env la siguiente línea:
```bash
DATABASE_URL="mysql://root@127.0.0.1:3306/nombreBBDD"
```
## Crear tabla en BBDD
```bash
php bin/console make:entity
```
## Crear esquema de la BBDD
```bash
php bin/console doctrine:schema:create
```
## Actualizar esquema de la BBDD
```bash
php bin/console doctrine:schema:update --dump-sql --force
```
## Ejecutar proyecto descargado de GitHub
- Es necesario reinstalar las librerias configuradas
```bash
composer install
```
