# Ejemplo de Uso de Gorilla Mux en Go

Este repositorio contiene un ejemplo simple de cómo crear un servidor web en Go utilizando el enrutador Gorilla Mux.

## Requisitos Previos

- Go (debe estar instalado en su sistema, consulte https://golang.org/doc/install)
- Git (opcional, pero recomendado para clonar este repositorio)
- postgreSQL o dokcer ya que se usa una base de datos para guardar los usuarios y las tareas relacionadas a ellos
- Air (un live reload de go), ve a https://github.com/cosmtrek/air para saber sobre la instalacion

## Cómo Ejecutar

1. Clona este repositorio en tu máquina local (si no tienes Git, puedes descargar el código fuente en formato ZIP):

    ```bash
    git clone https://github.com/Giankrp/ejemplo-gorilla-mux.git
    ```

2. Cambia al directorio del proyecto:

    ```bash
    cd firstback
    ```
4.Para generar una configuracion de air y poder ejecutar el live reload:
 ```bash
    air init
    ```

3. Ejecuta el programa:

    ```bash
    air
    ```

4. Abre tu navegador web y visita http://localhost:8000 para ver la aplicación en funcionamiento.

## En caso de usar docker

- En caso de usar docker ejecutar el siguiente comando:
  ```bash
    docker run --name some-postgres -e POSTGRES_USER=gian -e POSTGRES_PASSWORD=admin -p 5432:5432 -d postgres
   ```
- Para hacer las consultas ejecutar el siguiente comando:
  ```bash
    docker exec -it some-postgres bash
   ```

## Detalles del Proyecto

- `main.go`: Este es el archivo principal que contiene la lógica para configurar y ejecutar el servidor web utilizando Gorilla Mux.

- `routes`: En esta carpeta se definen las rutas y se configuran los manejadores correspondientes utilizando Gorilla Mux.

- `db`: Aqui se define la conexion de la base de datos (postgreSQL)

- `models`: En esta carpte se definen los modelos de las tablas "tasks" y "users"


## Contribuciones

¡Las contribuciones son bienvenidas! Si deseas mejorar este ejemplo, agregar más funcionalidades o corregir errores, no dudes en enviar un Pull Request.

## Recursos Adicionales

- Documentación de Gorilla Mux: https://github.com/gorilla/mux && https://gorilla.github.io/

- Documentación de ari (live Reload utilizado): https://github.com/cosmtrek/air

- Documentación de Go: https://golang.org/doc/

- Documentación del contenedor de postgreSQL: https://hub.docker.com/_/postgres
