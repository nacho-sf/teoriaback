# Teoría Backend

# Routing básico

El `routing` hace referencia a la determinación de cómo responde una aplicación a una solicitud de cliente en una determinada `ruta`, que es un URI (o una vía de acceso) y un método de solicitud HTTP específico (GET, POST, etc.).

Cada `ruta` puede tener una o varias funciones de `controlador`, que se excluyen cuando se correlaciona la ruta.

.
## Estructura

`app.MÉTODO(RUTA, CONTROLADOR)`

En el siguiente ejemplo, el código responde a una solicitud `GET` en la ruta `/about`:

```javascript
app.get('/about', function (req, res) {
  res.send('about');
});
```
- `app` es una instancia de express
- `MÉTODO` es un método de solicitud HTTP (GET, POST, PUT, DELETE)
- `RUTA` es una vía de acceso en el servidor
- `CONTROLADOR` es la función que se ejecuta cuando se correlaciona la ruta

.
### Métodos de ruta

Express da soporte a los métodos de direccionamiento que se corresponden con los métodos HTTP. Los básicos son `GET - POST - PUT - DELETE`

.
### Vías de aceso de ruta

Las vías de acceso de `ruta`, en combinación con un `método` de solicitud, definen los `endpoints` en los que pueden realizarse las solicitudes.

Las vías de acceso de `ruta` pueden ser series, patrones de serie o expresiones regulares:

- Express utiliza `path-to-regexp` para correlacionar las vías de acceso de ruta; consulte la documentación de [path-to-regexp](https://www.npmjs.com/package/path-to-regexp) para ver todas las posibilidades para definir vías de acceso de ruta.