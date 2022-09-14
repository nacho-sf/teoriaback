# Teoría Backend

## Routing básico

El `routing` hace referencia a la determinación de cómo responde una aplicación a una solicitud de cliente en un determinado `endpoint`, que es un URI (o una vía de acceso) y un método de solicitud HTTP específico (GET, POST, etc.).

Cada ruta puede tener una o varias funciones de `controlador`, que se excluyen cuando se correlaciona la ruta.

### Estructura

`app.MÉTODO(ENDPOINT, CONTROLADOR)`

En el siguiente ejemplo, el código responda a una solicitud `GET` en la ruta `/about`:

```javascript
app.get('/about', function (req, res) {
  res.send('about');
});
```
- `app` es una instancia de express
- `MÉTODO` es un método de solicitud HTTP (GET, POST, PUT, DELETE)
- `ENDPOITN` es una vía de acceso en el servidor
- `CONTROLADOR` es la función que se ejecuta cuando se correlaciona la ruta