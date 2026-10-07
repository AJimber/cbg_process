# Control del contraste, brillo y gamma de una imagen digital

Programa desarrollado en C++ utilizando OpenCV para modificar el contraste, brillo y gamma de una imagen digital.

## Compilación

```bash
mkdir build
cd build
cmake ..
make
```

## Ejemplos de ejecución

El programa se ejecuta indicando las opciones deseadas, la imagen de entrada y la imagen de salida:

```bash
./cbg_process [opciones] <imagen_entrada> <imagen_salida>
```

Por ejemplo:

```bash
./cbg_process -c=1.5 -b=0.2 -g=1.2 data/imagen.jpg salida.jpg
```

Para ejecutar el programa en modo interactivo:

```bash
./cbg_process -i data/imagen.jpg salida.jpg
```

Los parámetros y opciones disponibles pueden consultarse mediante:

```bash
./cbg_process --help
```

## Imágenes de entrada

Las imágenes que se vayan a utilizar deben almacenarse en el directorio `data/`.

Por ejemplo:

```text
data/
├── imagen1.jpg
├── imagen2.png
└── imagen3.jpg
```

Las imágenes pueden utilizarse mediante su ruta relativa:

```bash
./cbg_process -i data/imagen1.jpg salida.jpg
```