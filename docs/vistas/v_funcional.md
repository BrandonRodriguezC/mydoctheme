---
layout: default
title: Vista Funcional
parent: Vistas y Modelos
---

# Vista Funcional
{: .no_toc }


---

## Descripción

Como se menciona en una presentación académica de la Universidad de los Andes, el principal propósito de esta vista gira entorno a la descripción de elementos funcionales, incluyendo responsabilidades, interacciones e interfaces. Es por ello que se describe este modelo con el fin de comunicar la capacidad funcional del sistema, definir sus componentes más importantes, definir las estructura interna del sistema y hacer más explícito su diseño. Entre sus atributos encontramos la flexibilidad, la cohesión, el volumen de interacción, el acoplamiento de los componentes y la división de responsabilidades. A continuación, en la figura se evidencia dicho modelo y posteriormente su descripción.

![](https://64.media.tumblr.com/2aac06e5cea1018e61613efbfb8e7b54/bc03ce93c5f1e072-91/s2048x3072/5fb6d0c1903e25a70164e720b38f267a9a5823b5.png)


El sistema parte de una clase principal la cual es la responsable de inicializar todos los componentes que la integran (tanto visuales como lógicos), de allí parte la división del sistema en 4 áreas de trabajo. La primera es la barra de herramientas la cual se declara en la clase BarraSuperior, esta es la encargada de llamar funciones lógicas como el almacenamiento y carga de archivos (función que extiende de la interfaz GestorDeArchivos), la creación de áreas de codificación, la limpieza y comparación de pruebas de escritorio, por último la ejecución pausada y automática del código. Otra área integrada es el campo de edición de código que parte de la clase EditorCodigo el cual integra las múltiples áreas de código (CodeArea), cada área comprende de un motor lógico el cual le permite estilizar el contenido, insertar estructura, filtrar la inserción por teclado, y tomar las expresiones para su analisis lexico, sintactico y semantico. Estas áreas de código incorporan un menú de inserción (InsertMenu) el cual evalúa la posición de inserción y construyen el bloque con las indentación requerida para el área de código. La tercer área declarada es la de pruebas de escritorio (Tablas), áreas las cuales se componen de una tabla (Tabla) generada con las filas y columnas de manera automática para la visualización de cambios en memoria cuando se ejecuta el programa. Por último está el área de Consolas, la cual se responsabiliza de denotar información valiosa para el estudiante como errores, estructura del código, registro, además de integrar un área de entradas y salidas (ConsolaEntradas) la cual tiene como propósito definir y capturar la información que interactúa con el código. Todos estos componentes se enlazan con la parte lógica por medio de la clase Controlador.

Por otro lado, la parte lógica se compone de 3 áreas. La primera (Analizadores) permite evaluar las expresiones de manera léxica y sintáctica denotando los símbolos involucrados en el pseudocódigo en TablaDeSimbolos por medio de objetos de tipo Variable, para el análisis semántico se hace uso de la interfaz Posfijo la cual denota las expresiones notación polaca inversa (concepto explicado con mayor detalle en el siguiente subcapítulo) evaluadas en por la clase Evaluador. Después de su evaluación se almacena la expresión en ExpresionesLinea para su posterior uso en ejecución. La siguiente área es Secuenciador, la cual se encarga de generar una lista de instrucciones tal que pueda tomar sentido bajo el comportamiento de las estructuras, esta lista de instrucciones se genera haciendo uso de objetos tipo NodoSecuenciador y NodoCierre. Finalmente se encuentra Ejecutor el cual se encarga de ejecutar la lista de instrucciones haciendo uso de las interfaces Posfijo y Evaluador para la evaluación de expresiones necesarias haciendo uso de la tabla de símbolos. Cada una de los cambios realizados en ejecución son denotados en las tablas ya mencionadas en la parte visual, así como la información derivada y errores encontrados mostrados en el área de consolas.
