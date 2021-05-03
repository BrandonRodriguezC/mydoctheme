---
layout: default
title: Manual de Usuario
nav_order: 100
---

# Manual de Usuario
{: .no_toc }

## Tabla de contenidos
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# Descripción
TestDesk es un software de aprendizaje de algoritmos estructurados para principantes
o estudiantes que apenas empiezan a programar, este software se comportara como un IDE (Entorno de desarrollo integrado) el cual te ayudara a programar tus primeros algoritmos utilizando un pseudocodigo en español. 

**Screenshot**: Está es una repesentación de ejemplo del aplicativo; e.j.,

![](https://64.media.tumblr.com/c6824e7c10bd86f3e7b802243bf68a10/d66bf66ebb0d58a1-4a/s2048x3072/57d6c6ac2328423f63d8997fe74e57ec4095d19d.png)

### Principales características
 - Desarrollo/inserción de estructuras de pseudocodigo mediante un menu de generacion de bloques
 - Filtro de teclado en el documento para campos no requeridos
 - Analizador léxico, sintáctico y semántico de las diferentes expresiones
 - Notificación visual de errores en area de codificación
 - Notificación detalllada de errores en consola
 - Ejecución pausada (paso a paso)
 - Generación de tablas de prueba de escritorio (manual y automatica) perfiladas con las lineas de codigo
 - Registro de cambios en variables en tabla de prueba de escritorio automatica (algoritmo en ejecución)
 - Almacenamiento de instancias de documentos (pseudocodigo fuente) ~ Guardar codigo/archivo
 - Apertura de instancias de documentos (pseudocodigo fuente) ~ Abrir codigo/archivo
 - Generación de multiples areas de codigo

# Areas

El aplicativo se encuentra distribuido en cuatro areas de trabajo, las cuales se denominan:
  1. Barra superior
  1. Area de codificación
  1. Area de pruebas de escritorio (registro de lo que ocurre en memoria)
  1. Area de consolas
En la imagen se puede apreciar el la ubicación de estas respecto al indice listado.

**Screenshot**: Ubicación de las areas de trabajo; e.j.,

![](https://64.media.tumblr.com/7cbb3dc494c569e4e630031f7f99cf9f/4abddf35b2222e06-34/s2048x3072/18f7e04151c367e3b02ba284a39a37978a943fdd.png)


## Barra superior

La barra superior constituye una serie de botones con iconos los cuales te permitirán realizar diversas acciones de manera general con tu trabajo. 

### Nuevo editor de codigo
![](https://64.media.tumblr.com/d56f01096a4ab769cd6ef8a55d5d7ab3/20a2428041ebe684-62/s75x75_c1/21092ffc8b350988695c02356830caaf3185e589.png)
  Al pulsar este icono se creará un nuevo editor de codigo con el que podras trabajar. Puedes tener diferentes editores de codigo pero solo podrás ejecutar uno al mismo tiempo, y por ende solo podras interactura con la información (errores, entradas o salidas) del mismo. 
A continuación veras una secuencia de imagenes las cuales muestran el proceso para la creación de un nuevo editor de codigo.
![](https://64.media.tumblr.com/f4348763287521f9291ad27d7ab77d4d/f78dfb26eecdea20-83/s2048x3072/a0556ea17dfe6afb6ee11a12dc5d84a9e509757b.png)
![](https://64.media.tumblr.com/7ebfb2bf227db8c8a56fac459d11da45/f78dfb26eecdea20-19/s1280x1920/b1afe59fae0098df3943d1ecd22ff38794d2c2ff.png)
![](https://64.media.tumblr.com/520398bb0abd861b98cf742171b5617a/f78dfb26eecdea20-24/s2048x3072/cab7f442684a5effb2b01ac2ec3d8097ca741d5a.png)

### Guardar
![](https://64.media.tumblr.com/a321f00740e3a11dd7cf31461e08eb00/0d9f22ed59b42853-a6/s75x75_c1/8efcf0bceb9b8e7f02e1afca3f58d4350c92d29e.png)
  Al pulsar este icono se guardará tu algoritmo en un archivo **.td**, el nombre lo podras cambiar a tu gusto aunque la herramienta siempre te recomendará el nombre con el que creaste el editor. 
A continuación veras una secuencia de imagenes las cuales muestran el proceso para guardar tu archivo.
![](https://64.media.tumblr.com/12afabe3639824a09e168b8b4a0f3936/e32407d0e15ca0cf-07/s2048x3072/a7d6242a5925b0de4b4bb65b3fb0ae5f6069507b.png)
![](https://64.media.tumblr.com/74c080cf60f7cb5e6f2ab87c4c903920/e32407d0e15ca0cf-79/s2048x3072/c0776ee6f60a501d02d0638ec724ed403ac31071.png)

### Abrir
![](https://64.media.tumblr.com/8bae0a02cf9360c3d0cbbd06c3744b3c/b8ec54a9aa3865c5-25/s75x75_c1/2015b4d64fe1ed3b034d1b285fe4758a5f939672.png)
  Al pulsar este icono se abrirá tu archivo **.td**, solo deberás buscarlo entre tus documentos. 
A continuación veras una secuencia de imagenes las cuales muestran el proceso para abrir tu archivo.
![](https://64.media.tumblr.com/637f8a742c6324e88d7c0080a598d724/eb459a3375a299b7-94/s2048x3072/cd2c45d0178e6a476e901c3f14a8c72fe07f4c2f.png)
![](https://64.media.tumblr.com/fa5197ee0211766092edee8e2faee553/eb459a3375a299b7-65/s2048x3072/9760d5225b6a4a0027feb417ffa2feba1d50f43b.png)
![](https://64.media.tumblr.com/768c36dfc90821467635b3142001b13e/eb459a3375a299b7-3e/s2048x3072/4a91045894d603666091fd266072320af8c49e5c.png)

### Ejecutar

Este icono es cambiante dependiendo del modo en que se encuentre la herramienta, por ahora solo veremos que significa cada uno de ellos. En otro capitulo más adelante se detallará la función. 
- ![](https://64.media.tumblr.com/b134e078394f8e7768a3226f32d1463b/20a2428041ebe684-10/s75x75_c1/97539e8e6ba71f96708a69054c2a343e06eb923b.png) Cuando este icono esté presente, significa que estás en modo edición y podrás editar tu codigo en el area de codificación de lo contrario no podras realizar. Si lo pulsas psaras al modo de ejecución y el icono cambiará al que se muestra a continuación. 
- ![](https://64.media.tumblr.com/5adf007e3b8c350644b8f7453b67d0c8/20a2428041ebe684-b9/s75x75_c1/5d58ada7ffbfc37cfdb79d98ee56f8a90ddace1a.png) Este icono significa que estás en el modo de ejecuión el cual te permitirá ejecutar cada instrucción. Si lo pulsas volveras al modo deición y el icono cambiará al que se mostró previamente. 

### Ejecutar siguiente instrucción

Este icono es cambiante dependiendo del modo (edición o ejecución) y el estado en que se encuentre si está en el modo ejecución. 

- ![](https://64.media.tumblr.com/5a41542e4a004158369c047b1155efe2/b9a22b5e6d47ab5f-ae/s75x75_c1/0e97834a23459f496f34f6bf8255a858fc3d9ba8.png) Cuando este icono esté presente, significa que estás en modo ejecución y que podras ejecutar la siguiente instrucción.
- ![](https://64.media.tumblr.com/82763d99a0a3f84cfd5a00b26342858f/b9a22b5e6d47ab5f-80/s75x75_c1/c931fbf9aee548a1d1047b1445c6e49ef3774921.png) Si este icono está presente y estas en modo edición significa que no podras ejecutar la siguiente instrucción porque no has entrado en modo ejecución. Por otro lado, si estás en modo ejecución y este icono está presente... significa que la herramienta ha terminado de ejecutar todas las intrucciónes en tu codigo y no puede ejecutar la siguiente ya que no hay más. En este punto solo podras volver al modo edición pulsando nuevamente el boón de ejecutar.

### Comparar 

![](https://64.media.tumblr.com/9487126436949c3a7cf0c9c18260e786/20a2428041ebe684-87/s75x75_c1/f96ee404bf02ab86ee0277cc9e4db0c8a3b84aba.png) Al pulsar este icono podras notar los errores al comparar la tabla automatica y manual. Más adelante se mostrará un ejemplo. 

### Limpiar

![](https://64.media.tumblr.com/cdd7f78d54eaf630bc54e6f0b76b9504/20a2428041ebe684-12/s75x75_c1/0e9aec7c04eaf507b097c58a6e7b56897df1dd31.png) Al pulsar este icono podras limpiar la tabla automatica y manual. Más adelante se mostrará un ejemplo.  

## Area de codificación

Está es la principal area de trabajo, acá podras crear algoritmos apartir de las diferentes primitivas. Está area es un espacio de trabajo filtrado y asistido, por lo cual no tienes que preocuparte de la estructura de las primitivas. 

## Inserción 
Para insertar algo en tu espacio de trabajo solo debes ubicar tu cursor **|** en la linea en la que deseas insertar la primitiva. Posteriormente haces *click derecho* y aparecerá un menú desglozando las diferentes opciones de inserción. A continuación veras la estructura del menú:

1. Edición
 1. Nueva línea
 1. Eliminar línea o bloque
1. Declaración de variables
 1. Entero
 1. Real
 1. Lógica
 1. Texto
1. Primitivas
 1. Simples
  1. Lectura
  1. Escritura
  1. Asignación
 1. Bloque
  1. Condicionales
   1. Si simple
   1. Si sino
  1. Ciclos
   1. Repetir
   1. Mientras que

En la siguiente imagen verás como se muestra este menú en la herramienta. 

![](https://64.media.tumblr.com/fefebebb4c1b5296a5333399e097b916/b0a1a57507ab36fb-8c/s2048x3072/9ff351f948b504e7b99b60086ff157d0d16ba5ee.png)

Despues solo tienes que desglosar los sub-menus colocando el mouse sobre ellos, allí encontrarás la primitiva según la estructura ya definida y dar click izquierdo sobre el item.
![](https://64.media.tumblr.com/7371012e2660a84c9b148ddc56874415/b9345515e5da8102-50/s2048x3072/84a5850f661d08b4223ec8e888e72604695f1d15.png)
![](https://64.media.tumblr.com/0d04e95860522ce9aed3b89376d6e1f2/b9345515e5da8102-65/s2048x3072/c20066891dfd8a382cddc045b2242a5268a84096.png)

Cada primitiva tiene un espacio donde podras ingresar tus expresiones libremente, es decir, podras ingresar el contenido desde tu teclado como es habitual. Este espacio esta definido por un resaltado o sombreado el cual aparecerá unicamente cuando el cursor se ubique en la linea. Este sombreado te notificará por medio de colores si la expresion es correcta o incorrecta según la primitiva. La herramienta te notificará los errores en este espacio por medio de color naranja ![](https://64.media.tumblr.com/db6ebb8dfa6269a4aa989e8a6d5a40ec/0fd4a0124c0f5562-d4/s75x75_c1/842f05eb2b31dcd97304fd97f0010d708889e36a.png), pero si tu expresion es correcta para la primitiva su color será verde ![](https://64.media.tumblr.com/228e5e7eda5e3fb5032c863d90492cfc/0fd4a0124c0f5562-85/s75x75_c1/db1b972898893e789a11fb0056b0149667666a75.png).

### Uso

* Sobre el area de codigo has click izquierdo y encontraras el menu de inserción de estructuras de codigo.
* Unicamente podras escribir con el teclado sobre las areas sombreadas
* El programa te sombreará la expresion de color amarillo en caso de que la entrada tenga un error ya sea lexicamente, sintacticamente o semanticamente  
* Para saber mas detalle del error, has click en el panel derecho en la pestaña "Consola de errores"
* Para ejecutar tu codigo, has click en el botón *Secuenciar* y luego has click en el botón *Ejecutar siguiente* para ejecutar la siguiente instrucción (ambos botones se encuentran en la barra superior)
* Los cambios se verán efectuados en el panel central en la pestaña *Tabla Automatica*
* Para guardar el archivo has click en el botón *Guardar archivo* (ubicado en la barra superior)
* Para abrir un archivo has click en el botón *Abrir archivo* (ubicado en la barra superior)
* Si deseas utilizar otro editor de codigo en paralelo has click en el botón *Nueva pestaña* (ubicado en la barra superior)
