# MiniScrum Distribuido

## Objetivo

Explicar brevemente que hace la aplicacion.

## Arquitectura

Navegador -> Node Gateway -> PHP API -> MySQL
Navegador -> Node Gateway -> Python ML API

## Servicios

- gateway: frontend y API Gateway.
- php-api: CRUD de tareas.
- python-ml: prediccion de puntos Scrum.
- mysql: base de datos relacional.

## Endpoints principales

- GET /api/tasks
- POST /api/tasks
- PUT /api/tasks/:id/status
- POST /api/predict

## Base de datos

Tabla principal: tasks.

## Como ejecutar localmente

docker compose up --build

## URL desplegada

http://rojo-m2integrador-fzzk1n-5e44b3-10-14-255-92.traefik.me/

## Evidencias

Agregar capturas de:
- aplicacion funcionando
- tareas guardadas
- contenedores activos
- repositorio con commits

## Retrospectiva

Que salio bien:
Salio bien el deploy tanto en local como en el servidor. Tuve que poner un archivo .htaccess (recomendación de Claude para un error que no encontraba el servicio de php en local) pero creo que es porque mi prueba local la hice desde wsl y el navegador que lo consume estaba en windows, normalmente tengo algunos problemas de conexiones con wsl, pero poniendo eso todo lo demás funcionó bien.

Que fue dificil:
Fue dificil hacer las configuraciones en dokploy pero es principalmente falta de experiencia usando su interfaz

Que mejoraria:
El diseño de la aplicación, yo personalmente igual nunca había usado php y esta un poco raro, tal vez debería aprender lo básico por si encuentro un sistema que lo use, no estar tan perdido.