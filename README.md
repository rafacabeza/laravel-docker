# laravel-docker

- Ejemplo entorno de de sarrollo php y Laravel
- En pruebas hay dos ejemplos base de php
- En data habría que colocar dos carpetas con poyectos "laravel" y "laravel2"

## Para desplegar/instalar un proyecto Laravel:

- Clonar este entorno docker
- Clonar repositorio Laravel dentro de data
- Levantar el servicio: 

  ```docker-compose up -d```
  
- Entrar en el contenedor para poder usar composer:

  ```docker exec -it -u devuser "nombrecontedor" bash```
  
- Una vez dentro:

  ```
  composer install
  cp .env.example .env
  php artisan key:generate
  exit
  ```

- Cambio de permisos

 ```
  sudo chown -R www-data: storage
  sudo chmod -R 755 storage
  sudo chmod 777 storage/logs
  ```
