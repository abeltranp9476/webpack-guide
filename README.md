## Webpack

Es un paquete de módulos de JavaScripts, totalmente configurable y a diferencia de los Task Runners (como **Grunt** y **Gulp**) donde los procesos se gestionan de forma separada, en **webpack**, se conoce el origen y todo se compila en un único archivo.

Cuenta con un archivo de configuración *webpack.config.js*, donde definimos todo el proceso de construcción en un objeto Javascript.

1. **Entry**: Indica cuál es el punto(s) de entrada.
1. **Output**: Indica cuál es el punto(s) de salida.
1. **Loaders**: Realizan transformaciones en los archivos.
1. **Plugins**: Realizan acciones en los archivos.

## Instalación de webpack y su CLI

Para instalar la última versión o una versión específica, ejecute uno de los siguientes comandos:

```
npm install --save-dev webpack
# o una versión específica
npm install --save-dev webpack@<version>
```

Si estamos utilizando webpack v4 o posterior y deseamos llamar webpack desde la línea de comandos, debemos instalar su **CLI**:

```
npm install --save-dev webpack-cli
```

## Modo de producción y desarrollo

En webpack un patrón común es tener 2 archivos de configuración uno para las tareas de desarrollo y otro para las de producción. Es posible especificar el tipo de configuración en una sola línea de configuración. Webpack 4 introduce el modo de producción y el modo de desarrollo.

De hecho cuando corremos el comando webpack desde la terminal nos envía un mensaje de advertencia:

```
WARNING in configuration
The 'mode' option has not been set, webpack will fallback to 'production' for this value. Set 'mode' option to 'development' or 'production' to enable defaults for each environment.
You can also set it to 'none' to disable any default behavior. Learn more: https://webpack.js.org/concepts/mode/
```

👆 La opción 'modo' no se ha configurado. Establezca la opción 'modo' en 'desarrollo' o 'producción' para habilitar los valores predeterminados para este entorno.

- Ejecutando el comando para cada ambiente (desarrollo/producción):

```
# Generará un archivo indentado y con comentarios
webpack --mode development

# Generará un archivo minificado y sin comentarios
webpack --mode productio
```

- Modificar punto de entrada y salida predeterminado:

```
webpack ./src/index.js --output ./dist/main.js
```

[Guia en Notion](https://www.notion.so/Curso-de-Webpack-797d35d9af4a4c13b5ddfa3160e953ed)
