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
TestDesk es un software de aprendizaje de algoritmos estructurados para principiantes
o estudiantes que apenas empiezan a programar, este software se comportara como un IDE (Entorno de desarrollo integrado) el cual te ayudará a programar tus primeros algoritmos utilizando un pseudocódigo en español.

**Screenshot**: Está es una representación de ejemplo del aplicativo; e.j.,

![](https://64.media.tumblr.com/c6824e7c10bd86f3e7b802243bf68a10/d66bf66ebb0d58a1-4a/s2048x3072/57d6c6ac2328423f63d8997fe74e57ec4095d19d.png)

### Principales características
 - Desarrollo/inserción de estructuras de pseudocódigo mediante un menú de generación de bloques
 - Filtro de teclado en el documento para campos no requeridos
 - Analizador léxico, sintáctico y semántico de las diferentes expresiones
 - Notificación visual de errores en área de codificación
 - Notificación detallada de errores en consola
 - Ejecución pausada (paso a paso)
 - Generación de tablas de prueba de escritorio (manual y automática) perfiladas con las líneas de código
 - Registro de cambios en variables en tabla de prueba de escritorio automática (algoritmo en ejecución)
 - Almacenamiento de instancias de documentos (pseudocódigo fuente) ~ Guardar código/archivo
 - Apertura de instancias de documentos (pseudocódigo fuente) ~ Abrir código/archivo
 - Generación de múltiples áreas de código

# Pseudocódigo
La herramienta se limita al uso de primitivas de programación:
## Asignación
`[    ] =  [    ];`

## Lectura
` [    ] = leer( );`

## Escritura
 `escribir([    ]);`

## Estructuras condicionales
`si ([    ])`
`{`
` `
`}`

`si ([    ])`
`{`
` `
`}`
`sino`
`{`
` `
`}`

## Estructuras cíclicas
`repetir ([    ]) veces`
`{`
` `
`}` 

`mientras que ([    ])`
`{`
` `
`}`

Por lo tanto, la complejidad de los algoritmos por los cuales se desarrolló esta propuesta son de carácter simple, sin ser extensos mayormente haciendo uso únicamente de un método principal sin invocar a secundarios (archivo principal de trabajo). 

El pseudocódigo al ser independiente es posible delimitarlo a 4 tipos de datos (entero, decimal, texto, lógico) con el propósito de acercar al estudiante al contexto de tipación en los lenguajes. Con base a estos tipos de datos se excluyeron vectores o matrices de los mismos. 

Los operadores básicos involucrados en esta herramienta son los siguientes símbolos:

| Operador  | Operación  |
|-----------|------------|
| `||` | ó    |
| `&&` | y |
| `==` | igual que  |
| `!=` | diferente que  |
| `>` | mayor que |
| `<` | menos que |
| `<=` | menor o igual que |
| `>=` | mayor o igual que |
| `!` | negación |
| `+` | suma |
| `-` | resta |
| `*` | multiplicación |
| `/` | división |
| `%` | módulo |
| `^` | potencia |


# Áreas

El aplicativo se encuentra distribuido en cuatro áreas de trabajo, las cuales se denominan:
  1. Barra superior
  1. Área de codificación
  1. Área de pruebas de escritorio (registro de lo que ocurre en memoria)
  1. Área de consolas
En la imagen se puede apreciar el la ubicación de estas respecto al índice listado.

**Screenshot**: Ubicación de las áreas de trabajo; e.j.,

![](https://64.media.tumblr.com/7cbb3dc494c569e4e630031f7f99cf9f/4abddf35b2222e06-34/s2048x3072/18f7e04151c367e3b02ba284a39a37978a943fdd.png)


## Barra superior

La barra superior constituye una serie de botones con iconos los cuales te permitirán realizar diversas acciones de manera general con tu trabajo.

### Nuevo editor de código
<img src="https://64.media.tumblr.com/d56f01096a4ab769cd6ef8a55d5d7ab3/20a2428041ebe684-62/s75x75_c1/21092ffc8b350988695c02356830caaf3185e589.png" width="40px" > 
Al pulsar este icono se creará un nuevo editor de código con el que podrás trabajar. Puedes tener diferentes editores de código pero solo podrás ejecutar uno al mismo tiempo, y por ende solo podrás interactuar con la información (errores, entradas o salidas) del mismo.
A continuación verás una secuencia de imágenes las cuales muestran el proceso para la creación de un nuevo editor de código.
![](https://64.media.tumblr.com/f4348763287521f9291ad27d7ab77d4d/f78dfb26eecdea20-83/s2048x3072/a0556ea17dfe6afb6ee11a12dc5d84a9e509757b.png)
![](https://64.media.tumblr.com/7ebfb2bf227db8c8a56fac459d11da45/f78dfb26eecdea20-19/s1280x1920/b1afe59fae0098df3943d1ecd22ff38794d2c2ff.png)
![](https://64.media.tumblr.com/520398bb0abd861b98cf742171b5617a/f78dfb26eecdea20-24/s2048x3072/cab7f442684a5effb2b01ac2ec3d8097ca741d5a.png)

### Guardar
<img src="https://64.media.tumblr.com/a321f00740e3a11dd7cf31461e08eb00/0d9f22ed59b42853-a6/s75x75_c1/8efcf0bceb9b8e7f02e1afca3f58d4350c92d29e.png" width="40px" > 
Al pulsar este icono se guardará tu algoritmo en un archivo **.td**, el nombre lo podrás cambiar a tu gusto aunque la herramienta siempre te recomendará el nombre con el que creaste el editor.
A continuación verás una secuencia de imágenes las cuales muestran el proceso para guardar tu archivo.
![](https://64.media.tumblr.com/12afabe3639824a09e168b8b4a0f3936/e32407d0e15ca0cf-07/s2048x3072/a7d6242a5925b0de4b4bb65b3fb0ae5f6069507b.png)
![](https://64.media.tumblr.com/74c080cf60f7cb5e6f2ab87c4c903920/e32407d0e15ca0cf-79/s2048x3072/c0776ee6f60a501d02d0638ec724ed403ac31071.png)

### Abrir
<img src="https://64.media.tumblr.com/8bae0a02cf9360c3d0cbbd06c3744b3c/b8ec54a9aa3865c5-25/s75x75_c1/2015b4d64fe1ed3b034d1b285fe4758a5f939672.png" width="40px" > 
Al pulsar este icono se abrirá tu archivo **.td**, solo deberás buscarlo entre tus documentos.
A continuación verás una secuencia de imágenes las cuales muestran el proceso para abrir tu archivo.
![](https://64.media.tumblr.com/637f8a742c6324e88d7c0080a598d724/eb459a3375a299b7-94/s2048x3072/cd2c45d0178e6a476e901c3f14a8c72fe07f4c2f.png)
![](https://64.media.tumblr.com/fa5197ee0211766092edee8e2faee553/eb459a3375a299b7-65/s2048x3072/9760d5225b6a4a0027feb417ffa2feba1d50f43b.png)
![](https://64.media.tumblr.com/768c36dfc90821467635b3142001b13e/eb459a3375a299b7-3e/s2048x3072/4a91045894d603666091fd266072320af8c49e5c.png)

### Ejecutar

Este icono es cambiante dependiendo del modo en que se encuentre la herramienta, por ahora solo veremos qué significa cada uno de ellos. En otro capítulo más adelante se detalla la función.
- <img src="https://64.media.tumblr.com/b134e078394f8e7768a3226f32d1463b/20a2428041ebe684-10/s75x75_c1/97539e8e6ba71f96708a69054c2a343e06eb923b.png" width="40px" > Cuando este icono está presente, significa que estás en modo edición y podrás editar tu código en el área de codificación de lo contrario no podrás realizar. Si lo pulsas pasarás al modo de ejecución y el icono cambiará al que se muestra a continuación.
- <img src="https://64.media.tumblr.com/5adf007e3b8c350644b8f7453b67d0c8/20a2428041ebe684-b9/s75x75_c1/5d58ada7ffbfc37cfdb79d98ee56f8a90ddace1a.png" width="40px" > Este icono significa que estás en el modo de ejecución el cual te permitirá ejecutar cada instrucción. Si lo pulsas volverás al modo edición y el icono cambiará al que se mostró previamente.

### Ejecutar siguiente instrucción

Este icono es cambiante dependiendo del modo (edición o ejecución) y el estado en que se encuentre si está en el modo ejecución.

- <img src="https://64.media.tumblr.com/5a41542e4a004158369c047b1155efe2/b9a22b5e6d47ab5f-ae/s75x75_c1/0e97834a23459f496f34f6bf8255a858fc3d9ba8.png" width="40px" > Cuando este icono está presente, significa que estás en modo ejecución y que podrás ejecutar la siguiente instrucción.

- <img src="https://64.media.tumblr.com/82763d99a0a3f84cfd5a00b26342858f/b9a22b5e6d47ab5f-80/s75x75_c1/c931fbf9aee548a1d1047b1445c6e49ef3774921.png" width="40px" > Si este icono está presente y estas en modo edición significa que no podrás ejecutar la siguiente instrucción porque no has entrado en modo ejecución. Por otro lado, si estás en modo ejecución y este icono está presente... significa que la herramienta ha terminado de ejecutar todas las instrucciones en tu código y no puede ejecutar la siguiente ya que no hay más. En este punto solo podrás volver al modo edición pulsando nuevamente el botón de ejecutar.

### Comparar
<img src="https://64.media.tumblr.com/9487126436949c3a7cf0c9c18260e786/20a2428041ebe684-87/s75x75_c1/f96ee404bf02ab86ee0277cc9e4db0c8a3b84aba.png" width="40px"> 
Al pulsar este icono podrás notar los errores al comparar la tabla automática y manual. Más adelante se mostrará un ejemplo.

### Limpiar
<img src="https://64.media.tumblr.com/cdd7f78d54eaf630bc54e6f0b76b9504/20a2428041ebe684-12/s75x75_c1/0e9aec7c04eaf507b097c58a6e7b56897df1dd31.png" width="40px">
Al pulsar este icono podrás limpiar la tabla automática y manual. 


## Área de codificación

Esta es la principal área de trabajo, acá podrás crear algoritmos a partir de las diferentes primitivas. Está área es un espacio de trabajo filtrado y asistido, por lo cual no tienes que preocuparte de la estructura de las primitivas.

### Inserción
Para insertar algo en tu espacio de trabajo solo debes ubicar tu cursor **|** en la línea en la que deseas insertar la primitiva. Posteriormente haces *click derecho* y aparecerá un menú desglosando las diferentes opciones de inserción. A continuación verás la estructura del menú:


* Edición
   * Nueva línea
   * Eliminar línea o bloque
* Declaración de variables
   * Entero
   * Real
   * Lógica
   * Texto
* Primitivas
   * Simples
      * Lectura
      * Escritura
      * Asignación
   * Bloque
      * Condicionales
         * Si simple
         * Si sino
      * Ciclos
         * Repetir
         * Mientras que

En la siguiente imagen verás como se muestra este menú en la herramienta.

![](https://64.media.tumblr.com/fefebebb4c1b5296a5333399e097b916/b0a1a57507ab36fb-8c/s2048x3072/9ff351f948b504e7b99b60086ff157d0d16ba5ee.png)

Después solo tienes que desglosar los sub-menús colocando el mouse sobre ellos, allí encontrarás la primitiva según la estructura ya definida y dar click izquierdo sobre el ítem.
![](https://64.media.tumblr.com/7371012e2660a84c9b148ddc56874415/b9345515e5da8102-50/s2048x3072/84a5850f661d08b4223ec8e888e72604695f1d15.png)
![](https://64.media.tumblr.com/0d04e95860522ce9aed3b89376d6e1f2/b9345515e5da8102-65/s2048x3072/c20066891dfd8a382cddc045b2242a5268a84096.png)

Cada primitiva tiene un espacio donde podrás ingresar tus expresiones libremente, es decir, podrás ingresar el contenido desde tu teclado como es habitual. Este espacio está definido por un resaltado o sombreado el cual aparecerá únicamente cuando el cursor se ubique en la línea. Este sombreado te notificará por medio de colores si la expresión es correcta o incorrecta según la primitiva. La herramienta te notificará los errores en este espacio por medio de color naranja ![](https://64.media.tumblr.com/db6ebb8dfa6269a4aa989e8a6d5a40ec/0fd4a0124c0f5562-d4/s75x75_c1/842f05eb2b31dcd97304fd97f0010d708889e36a.png), pero si tu expresión es correcta para la primitiva su color será verde ![](https://64.media.tumblr.com/228e5e7eda5e3fb5032c863d90492cfc/0fd4a0124c0f5562-85/s75x75_c1/db1b972898893e789a11fb0056b0149667666a75.png).

### Indentación
No te preocupes por la indentación (sangría), este recurso lingüístico es muy importante en programación sobre todo en lenguajes como Python. TestDesk es capaz de calcular la indentación necesaria para la inserción de alguna primitiva dentro de un bloque, a continuación verás un ejemplo de ello.

![](https://64.media.tumblr.com/30dcc4c26fef7e2720cd3fd0704386d3/b231b9a5e527f041-05/s2048x3072/3ff450fab907623c4790c181609a272cb7920407.png)
![](https://64.media.tumblr.com/f797ba4a7fe81210c9468a6f06110c96/b231b9a5e527f041-57/s2048x3072/b7223a62978a630225fdc8ebd3b59d01ebf53e47.png)
![](https://64.media.tumblr.com/32e3c3bf54e59ca58805f4f9406fac8d/b231b9a5e527f041-5c/s2048x3072/be1f9371e11b0e02f1a4d74768c7089eee0f7b4f.png)

## Área de pruebas de escritorio

En este área podrás ver lo que ocurre con tu programa en memoria, existen 2 pestañas *Tabla automática* y *Tabla manual*.

### Tabla automática
En la tabla automatica podras ver lo que ocurre con tu programa en memoria, este es un recurso que suele hacerse de manera manual por los programadores, más sin embargo esta herramienta lo hace automáticamente por ti mientras creas un modelo mental de cómo hacerlo y así no te confundirás en el futuro. Está tabla se va llenando cuando estes en modo ejecución y recorriendo (ejecutando) cada instrucción.
En la barra superior color azul con letras blancas encontrarás las variables declaradas. Cada una de sus filas está alineada con las líneas de código presentes en el área de codificación, así que para encontrar el cambio ocurrido en memoria en la ejecución solo debes ubicar la fila correspondiente a la línea y también la columna a la que corresponda la variable asignada con el cambio. En esta tabla no podrás insertar valores. En el capítulo de ejecución se hará un ejemplo de ello.

### Tabla manual
En la tabla manual es posible insertar valores correspondientes a los cambios que tu identifiques, para ello debes entrar en modo ejecución. De esta manera podrás llenarla y a medida de que se ejecuten las líneas podrás identificar las diferencias (errores) al comparar la tabla automática con la tabla manual.

### Comparar Tablas

En la siguiente imagen podrás un ejemplo de esta función explicada en el capítulo *BarraSuperior.Comparar*. En este caso la línea 1 para las variables *a* y *b* se denota una declaración, por ende se inicializa la variable con valores predefinidos (en este caso 0). Como se puede apreciar en la *Tabla automática* los valores declarados son *0* y *0* mientras que los valores denotados en la *Tabla manual* son *0* y *1*. Al pulsar el botón comparar se cambian los estilos de las celdas, para poder verlos adecuadamente es necesario que *la línea de ejecución* no se encuentre en la misma fila.

<div style="display:flex">
<img src="https://64.media.tumblr.com/438bad3a006c05ca33023b57045ed602/0657eef3635eb1e6-47/s2048x3072/e98d26a535b9b02717e07467f340b9621d1cb39d.png" width="50%" >
<img src="https://64.media.tumblr.com/f75a8087a32f0bdd5e6939ae31139d81/0657eef3635eb1e6-06/s2048x3072/746d4bb949edd887717edb2de8c6cd1bec536d04.png" width="50%" >
</div>
Cambio de estilos al comparar las tablas:
<div style="display:flex">
<img src="https://64.media.tumblr.com/4dadef7b66a41ae548c1afe3aa8ac20d/0657eef3635eb1e6-d6/s2048x3072/fdc55054a88d2d3ab1fef28ca7d28864201088ba.png" width="50%" >
<img src="https://64.media.tumblr.com/70f49b2bff73a1ff34beaec8d1dabc62/0657eef3635eb1e6-4b/s2048x3072/e2429cbc88ed349f4f14b30a72070cb4ca69368d.png" width="50%" >
</div>
Si se vuelve a comparar las tablas una vez corregido el error se cambiará el color de las celdas a blanco nuevamente.

## Área de consolas
La consola de información es la encargada de detallar los diferentes errores en las expresiones, TestDesk comprobará la expresión de manera léxica, sintáctica y semántica. En caso de encontrar un error lo notificará en la consola de información y aplicará un resaltado color naranja sobre ella. La estructura del error será **ERROR L** *#* **:** *Detalle del error*. Donde el *#* indica el numero de linea y el *Detalle del error* mostrará el error con mayor información. A continuación se muestran unos ejemplos de errores léxicos, sintácticos y semánticos.

### Error léxico
![](https://64.media.tumblr.com/7825fc24c24602a2322b1e6f6653b3fe/0ff1d4173e6a398d-16/s2048x3072/392eef6f032fddbaa2466e6d1c844da899a603e1.png)

### Error sintáctico
![](https://64.media.tumblr.com/cb22f7f33780d5336eb515e45bd1a373/0ff1d4173e6a398d-d8/s2048x3072/cc955d0149a1d36d002428c2da2bb77554411ce7.png)

### Error semántico
![](https://64.media.tumblr.com/8fe29e71c854988c90b481514048c58a/0ff1d4173e6a398d-9f/s2048x3072/63838d5750d839ff609f203170dc79d2df65331f.png)

La consola de información también es capaz de mostrar información en ejecución, como errores en la operación de expresiones o salidas. A continuación se muestra un ejemplo de cada una:

### Errores en la operación de expresiones
Los errores en ejecución se verán con la misma estructura explicada anteriormente. A continuación un ejemplo:

![](https://64.media.tumblr.com/6b2d899283799a7cf5e3efa1ff7c5a27/cdbb3bd489bd493d-bd/s2048x3072/9bfd6fc2bb40fb44f1d7b60ea71953e52763c5a6.png)
### Salidas
Las salidas (ejecutadas por la primitiva simple *escritura*) tendrán la estructura **EJECUCIÓN:** *Impresión*

![](https://64.media.tumblr.com/d0387c9fd42b5c277d7c13683371eb1e/cdbb3bd489bd493d-49/s2048x3072/0d360e48c79b86cefedb5b5566adf1ef9d54e60b.png)

Por otro lado en la *Consola de entradas* se expresa de la siguiente manera en la columna de escritura:
![](https://64.media.tumblr.com/9e0248d1130d75ead700250c621b235f/2ff8aef47ad11cf7-87/s2048x3072/8e6645e6f112ad218b94cd17cf1deebdde25e677.png)

# Ejecución
Cuando el programa entre en modo ejecución después de pulsar el botón
<img src="https://64.media.tumblr.com/b134e078394f8e7768a3226f32d1463b/20a2428041ebe684-10/s75x75_c1/97539e8e6ba71f96708a69054c2a343e06eb923b.png" width="20px" > se cambiará al icono <img src="https://64.media.tumblr.com/5adf007e3b8c350644b8f7453b67d0c8/20a2428041ebe684-b9/s75x75_c1/5d58ada7ffbfc37cfdb79d98ee56f8a90ddace1a.png" width="20px" >. De este modo no podrás alterar tu código de ninguna manera, se limpiará la información en las tablas y consolas, y aparecerá una línea sombreada azul atravesando los paneles de codificación, tablas y consola de entradas y salidas indicando que dicha línea es la actual en ejecución. La línea recorrerá el código en función al comportamiento teórico de las primitivas cada que pulses el botón *ejecutar siguiente instrucción* <img src="https://64.media.tumblr.com/5a41542e4a004158369c047b1155efe2/b9a22b5e6d47ab5f-ae/s75x75_c1/0e97834a23459f496f34f6bf8255a858fc3d9ba8.png" width="20px" >. Cada que se denote un cambio en memoria (al asignar un nuevo valor en alguna variable) se mostrará en la *Tabla automática* en la línea antes mencionada. En caso de efectuarse un error se presentará en el área de *Consola de información*. Si se expresa una escritura, entonces se denotará está en la *Consola de información* y *Consola de entradas y salidas*. Si se expresa una lectura, el programa ajustará el cursor en la columna de *Lectura* para la *Consola de entradas y salidas*, alli deberas ingresar el valor y continuar ejecutando la siguiente línea hasta llegar a la última de la  de la ejecución (donde el icono se encuentra deshabilitado <img src="https://64.media.tumblr.com/82763d99a0a3f84cfd5a00b26342858f/b9a22b5e6d47ab5f-80/s75x75_c1/c931fbf9aee548a1d1047b1445c6e49ef3774921.png" width="20px" >).

A continuación una serie de videos que muestran su función:
![](https://youtu.be/7o-QY5pZg-A)
![](https://youtu.be/NnG5Irskiok)
![](https://youtu.be/fmXKpE38qMw)

