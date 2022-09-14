# Teoría Backend

## Routing básico

El `routing` hace referencia a la determinación de cómo responde una aplicación a una solicitud de cliente en un determinado `endpoint`, que es un URI (o una vía de acceso) y un método de solicitud HTTP específico (GET, POST, etc.).

Cada ruta puede tener una o varias funciones de `controlador`, que se excluyen cuando se correlaciona la ruta.


### Estructura

app.METODO(ENDPOINT, CONTROLADOR)

Ejemplo:
```javascript
app.get('/about', function (req, res) {
  res.send('about');
});
```