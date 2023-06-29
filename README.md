# Cafetería Nanacao

Esta es una API simple para administrar una lista de cafés. Permite realizar operaciones CRUD (Crear, Leer, Actualizar y Eliminar) sobre los cafés disponibles.

## Instalación

1. Clona este repositorio en tu máquina local.
2. Abre una terminal y navega hasta el directorio del proyecto.
3. Ejecuta el siguiente comando para instalar las dependencias necesarias:

```
npm install
```

## Uso

1. Ejecuta el siguiente comando para iniciar el servidor:

```
npm run dev
```

2. El servidor estará disponible en `http://localhost:3000`.

## Endpoints

### Obtener todos los cafés

```http
GET /cafes
```

Este endpoint devuelve todos los cafés disponibles.

### Obtener un café por ID

```http
GET /cafes/:id
```

Este endpoint devuelve un café específico según el ID proporcionado.

### Agregar un nuevo café

```http
POST /cafes
```

Este endpoint permite agregar un nuevo café a la lista. Debe proporcionar un objeto JSON en el cuerpo de la solicitud con la siguiente estructura:

```json
{
  "id": 5,
  "nombre": "Expreso"
}
```

### Actualizar un café existente

```http
PUT /cafes/:id
```

Este endpoint permite actualizar un café existente según el ID proporcionado. Debe proporcionar un objeto JSON en el cuerpo de la solicitud con la siguiente estructura:

```json
{
  "id": 5,
  "nombre": "Latte"
}
```

**Nota:** El ID del café debe coincidir tanto en los parámetros de la ruta como en el cuerpo de la solicitud. Si el ID no coincide, se devolverá un código de estado 400.

### Eliminar un café

```http
DELETE /cafes/:id
```

Este endpoint permite eliminar un café según el ID proporcionado. También se debe proporcionar un encabezado `Authorization` con un token válido para autorizar la eliminación. Si el café no se encuentra, se devolverá un código de estado 404.

## Pruebas

Este proyecto incluye pruebas automatizadas utilizando el framework Jest y la librería Supertest.

```bash
npm install jest
```

Para ejecutar las pruebas, utiliza el siguiente comando:

```bash
npm test
```

## Contribución

Si deseas contribuir a este proyecto, siéntete libre de crear un *pull request* con tus mejoras o correcciones de errores.
