# Examen Técnico Elektra App

La prueba consiste en diseñar lo mas cercano a la UI una aplicación en Kotlin.

Se requiere consumir las imagenes de los banners :

http://hnoscarrasco.com/images/cekt
http://hnoscarrasco.com/images/hotsale
http://hnoscarrasco.com/images/Imagen%20producto4
http://hnoscarrasco.com/images/Imagen%20producto5
http://hnoscarrasco.com/images/Imagen%20producto6

La información de los productos debe ser consumida en Graphql se muestra al final un ejemplo.

Al presionar ver todos de cada grid debe llevar a una nueva vista en donde se implementará un header o toolbar de busqueda y cargar todos los productos en forma de lista; El buscador(header o toolbar) debe filtrar esta lista por nombre de forma predictiva.

En la seccion de marcas participantes y los mas vendidos se debe implementar un carousel que se mueva por el usuario y no por tiempo.

Al regresar de cualquier vista debe regresar a Home, para salir de la aplicación en Home debe presionar dos veces back.

En la parte de la navegación se deberá agregar un boton para crear cuenta que lleve a una vista de formulario, la información de los campos no se debe perder cuando el telefono gire o entre a background.

## Petición de ejemplo en GraphQL

```bash
URL: https://stage.ektdevelopers.com/_graphql

query getProducts($skus: [String]) {
  viewer {
    products(skus: $skus) {
      id
      name
      image
      price
    }
  }
}

variables: {
  "skus": [
    "321323142",
    "321323076",
    "45025344",
    "45024957",
    "1003678",
    "321321586",
    "45025337",
    "321323141",
    "45035651",
    "45048926",
    "1007046",
    "1006062",
    "1007073",
    "321324716",
    "1006025",
    "1005116",
    "1006593",
    "1006581",
    "1006945",
    "321321538"
  ]
}
```

Si tienes dudas, puedes revisar el siguiente ejemplo [aquí](<https://stage.ektdevelopers.com/_graphql?variables=%7B%0A%20%20%22skus%22%3A%20%5B%22321323142%22%2C%20%22321323076%22%2C%20%2245025344%22%2C%20%2245024957%22%2C%20%221003678%22%2C%20%22321321586%22%2C%20%2245025337%22%2C%20%22321323141%22%2C%20%2245035651%22%2C%20%2245048926%22%2C%20%221007046%22%2C%20%221006062%22%2C%20%221007073%22%2C%20%22321324716%22%2C%20%221006025%22%2C%20%221005116%22%2C%20%221006593%22%2C%20%221006581%22%2C%20%221006945%22%2C%20%22321321538%22%5D%0A%7D&query=query%20getProducts(%24skus%3A%20%5BString%5D)%20%7B%0A%20%20viewer%20%7B%0A%20%20%20%20products(skus%3A%20%24skus)%20%7B%0A%20%20%20%20%20%20id%0A%20%20%20%20%20%20name%0A%20%20%20%20%20%20image%0A%20%20%20%20%20%20price%0A%20%20%20%20%7D%0A%20%20%7D%0A%7D>)

## UI de muestra

![](https://raw.githubusercontent.com/CristianJrd/ExampleElektra/master/01%20Season.png)
