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

### Ejecutar siguiente instrucción

### Comparar 

### Limpiar



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
