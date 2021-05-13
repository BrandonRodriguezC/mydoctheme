---
layout: default
title: Documentación teórica del sistema
nav_order: 99
---

# Documentación teórica del sistema
{: .no_toc }

## Tabla de contenidos
{: .no_toc .text-delta }

1. TOC
{:toc}

---
# Sistema
## Entorno gráfico.  
Para el desarrollo de la herramienta se evaluaron las librerías de componentes gráficos en Java, actualmente no existen librerías tan ricas en dichos componentes por lo cual solo se evaluaron dos familias de elementos gráficos. Una de ellas fue java.swing mientras que la otra fue JavaFX, para el presente proyecto se decidió trabajar con esta última a razón de su vigencia y alta variedad de componentes gráficos adaptables para los sistemas operativos actuales. Mientras que por otro lado, java.swing se encuentra depreciada y poco abordada en aplicaciones actuales. Además de ello, JavaFX se encuentra denominada como un entorno gráfico robusto a la hora de incorporarse con componentes externos. Este entorno gráfico se encuentra incorporado en el java developer kit 1.8 para Java Standard Edition.

Una vez definido el entorno gráfico a utilizar surgió la necesidad de hacer una búsqueda de componentes gráficos que pudieran representar un editor de código estilizado. Para ello fue necesario clasificar los componentes existentes y filtrar únicamente los que funcionan con JavaFx. De esta búsqueda solo surgieron dos candidatos los cuales se pueden apreciar en la Figura 1, RichText y StyledTextArea. Si bien RichText es un componente vigente y propiamente documentado, y StyledTextArea es un componente poco documentado y depreciado; se decidió utilizar este último. El factor que permitió la decisión fue la visibilidad del cursor cuando la edición del componente se encontraba inhabilitada. Esto a razón de que la herramienta tendría un sistema de generación de bloques asistido, con lo cual únicamente es posible insertar los bloques desde un menú que se despliega al dar click derecho y se agrega en la posición del cursor, así como ingresar libremente donde sea requerida una expresión (tema que se abordará más adelante).


Figura 1. Componentes gráficos de editores de código estilizados (RichText a la izquierda, StyledTextArea a la derecha).

<div style="display:flex">
<img src="https://64.media.tumblr.com/a7f4a2a3559c07f69683b590f02b7932/151f3562a4036efc-12/s500x750/1f70637ad403fee9b3482dcb42d750e872d0bf67.png" width="25%" >
<img src="https://64.media.tumblr.com/8630b485ad63ddcf8240271ff30dd75d/151f3562a4036efc-16/s400x600/da20dde0154d0e922bd06739f941b73a4aa69b83.png" width="25%" >
</div>

Fuente: Propia.


## Sistema de generación de bloques.  
En cumplimiento al requerimiento pre-establecido, la herramienta sería un entorno de desarrollo de algoritmos limitado y asistido, por lo tanto no permitirá la inserción libremente de texto en campos no requeridos. Es por ello que se creó un filtro el cual determinará según la posición del cursor si el componente adquiere la característica editable o no. Dicho filtro funciona al identificar los rangos de los campos de libre edición (campos que se componen de nombres de variables, expresiones aritméticas o lógicas) y verificar si el cursor se encuentra dentro de alguno de esos rangos.

En el proceso de estilizado al insertar una estructura básica de programación, se debe reconocer cada elemento perteneciente al pseudocódigo. Para ello se utilizaron las clases Pattern y Matcher de la librería java.util.regex, las cuales facilitaron la búsqueda de elementos en el texto. Es por ello que se definieron expresiones regulares (patrones de escritura) los cuales identificaran el elemento y encima lo clasificará según determinado grupo. Entre los grupos se definieron palabras clave, tipos de datos, patrones de paréntesis, operador de asignación, signo de cierre, apertura y cierre de bloques, estructura de comentario, y por último método de lectura y escritura. Dados estos grupos, a la hora de identificar el elemento en el texto y posteriormente clasificarlo, se asigna un estilo y se identifica su función dentro del pseudocódigo. De esta manera se podían identificar los campos de libre escritura y los rangos de estos. El proceso de inserción se puede evidenciar en la Figura 2.


Figura 2. Proceso de inserción de estructuras (campo habilitado a edicion libre en amarillo)

 <div style="display:flex">
<img src="https://64.media.tumblr.com/bbaac3ea9a81ae9cdeb3fa1ba5d1eb7c/0a7037249979876e-06/s400x600/3b534d5fa4a190d23e77bf76ec8432508f395ae0.png" width="25%" >
<img src="https://64.media.tumblr.com/08ce0bc46de26f6862dd47a738227a9d/0a7037249979876e-79/s400x600/74f7d94c2e5d3d1a6e7bffea9300ed4a90059bb1.png" width="25%" >
</div> 

Fuente: Propia


## Analizador léxico.  
En los campos de libre escritura para dichos identificadores (nombres de variables) o expresiones aritméticas o lógicas, nace la necesidad de la creación de un evaluador léxico, sintáctico y semántico. Dependiendo del tipo de campo libre se deben asignar determinadas propiedades al evaluador el cual dará respuesta basado en dichos argumentos. Evaluador el cual determina si dicha expresión era válida para el campo al cual pertenece y si su composición es correcta. Como lo explica Alfonseca , para lograr un análisis léxico de la expresión es necesario un autómata finito determinista (concepto mencionado en el capítulo 5.1.4) este autómata recorre la expresión y se encarga de dividirla en unidades sintácticas. Desde un análisis léxico en caso de no reconocer el elemento dentro del diccionario preestablecido se denota un error en la expresión. Nuevamente se utilizaron las clases Matcher y Pattern las cuales permiten un apoyo a la hora de identificar las unidades sintácticas. En este caso las expresiones regulares establecidas como unidades sintácticas en el diccionario fueron datos de tipo entero, real, lógico, texto, paréntesis, operadores, espacios, comas, identificadores y palabras restringidas. De esta manera al evaluar la expresión en caso de encontrar diferencias del último índice del último elemento reconocido y el primer índice del nuevo elemento reconocido se procederá a notificar un error de tipo léxico. Del mismo se notifica el error en caso de que encuentre un elemento perteneciente a un grupo restringido. Un ejemplo de su notificación se puede ver en la Figura 3.


Figura 3. Notificación de error léxico.

 <div style="display:flex">
<img src="https://64.media.tumblr.com/e8a4d7d89df994a6d0735dda997a53a4/ae0cffb0ac56d97c-f5/s500x750/57aa2103acb5dd7cfc5e6d936823fc6de2aa5cf3.png" width="25%" >
<img src="https://64.media.tumblr.com/496cab94620c366be048204293adfc47/ae0cffb0ac56d97c-9d/s500x750/5114f3614ac8ea8a374696113399462b5672e41b.png" width="25%" >
</div> 

Fuente: Propia


Las propiedades asignadas para el evaluador, además de permitir la evaluación de campos libres de diferentes tipos, permite insertar identificadores en la tabla de símbolos (concepto explicado más adelante). La inserción de identificadores en la tabla de símbolos es vital para el análisis de expresiones posteriores, bien sea un análisis de tipo léxico, sintáctico o semántico; es importante tener conocimiento de las variables declaradas para no alertar falsos errores.


## Analizador sintáctico.  
Nuevamente, Alfonseca  explica el uso de autómatas finitos deterministas como medio de análisis sintáctico para un texto, expresión o conjunto gramatical. A diferencia del análisis léxico, el análisis sintáctico pretende evaluar la composición de una expresión la cual posee todas sus unidades sintácticas correctas. Los autómatas finitos deterministas tienen la capacidad de definir estados respecto a las unidades sintácticas. De esta manera es posible determinar si la transición de un estado a otro es correcta. En la Figura 4 se puede evidenciar un ejemplo de autómata determinista finito para la declaración de variables, expresión la cual corresponde a un campo libre compuesto y de declaración (propiedades vitales para el evaluador construido).


Figura 4. Ejemplo de autómata determinista finito para la declaración de una o varias variables.

 <div style="display:flex">
<img src="https://64.media.tumblr.com/97c8a1704088ad62d6833accb8ed7109/b823531c57a8403b-3b/s540x810/7dda84885bf9f6836fa6cb363b9baa08b6574a99.png" width="50%" >
</div>

Fuente: Propia


Como se puede ver en la imagen, para que una declaración de variables compuesta pueda ser válida debe transitar por al menos 4 estados. Cada nodo puede representar un carácter, una secuencia de caracteres o una expresión regular, dependiendo del grado de composición que se esté evaluando. En este caso cada nodo de estado 1 representa una expresión regular, que a su vez son autómatas finitos deterministas que se manejaron desde la clase principal java.regex. Si bien el autómata estaría en completitud con los 4 estados, únicamente se evaluó y se integraron los estados 1 y 2 (color negro), esto a razón de que el sistema generador de bloques asegura la completitud de unidades sintácticas para los nodos de estado 0 y 3 (color azul). Esto siendo únicamente un ejemplo de las múltiples composiciones presentes en los campos libres disponibles, los cuales pueden resultar en autómatas deterministas complejos o no deterministas complejos; debido a la presencia de expresiones lógicas y aritméticas, siendo estas mismas mucho más complejas si existe la presencia de paréntesis los cuales están compuestos de otras expresiones internamente. En el caso de que exista una transición de estados no válida, sea por ejemplo de 0 a 2, automáticamente se descarta el continuo análisis y se declara el error (ausencia de estado tipo 1 o ausencia de identificador previo a la coma). En la Figura 5 se puede apreciar un ejemplo de error sintáctico determinado por el autómata de la aplicación. 


Figura 5. Notificación de error sintáctico.

 <div style="display:flex">
<img src="https://64.media.tumblr.com/aab6235194ab007082358ac42be9da4f/6423509ae87b139f-0d/s400x600/41193d48d1cb62d98651cc29088c53811b5dc6a6.png" width="25%" >
<img src="https://64.media.tumblr.com/35c9fbfb7223b35ddd330ecf2ffce5c9/6423509ae87b139f-47/s500x750/d61b8d8654db3fd3b86018e0d0920e6d48084d00.png" width="25%" >
</div> 

Fuente: Propia


## Analizador semántico.  
Al determinar la presencia de una expresión válida en términos léxicos y sintácticos  es necesario un análisis semántico, el cual permita verificar la validez semántica. Es decir, que sea válido el sentido de la expresión. Nuevamente se analiza únicamente los campos libres a razón de que el generador de bloques asegura la cohesión completa (sintáctica, léxica y semántica) de la estructura a excepción de la expresión, ya que esta puede variar. Alfonseca  denota que la salida de este analizador puede recaer en un árbol del análisis del programa con anotaciones como el de la Figura 6. Análisis el cual tiene en cuenta aspectos como:
•	El uso de un identificadores declarados previamente.
•	En las expresiones, los operandos respetan las reglas sobre los tipos de datos permitidos por los operadores.
•	El resultado de una expresión coincide con el dato asignado.
•	Verificación de operadores respecto a las estructuras y sus tipos correspondientes.


Figura 6. Ejemplo de árbol de análisis del programa con anotaciones.

 <div style="display:flex">
<img src="https://64.media.tumblr.com/5f6bf5b57c1d86604c34ec1bc28c8672/8aa66b18aa919f56-b4/s540x810/cf0d61e56178c66be7918c1f168966e85fa1dc46.png" width="50%" >
</div>

Fuente: Alfonseca (Capítulo 5.1) Compiladores e Intérpretes


Asimismo, Alfonseca  declara que este resultado o análisis puede variar ya que es bien sabido que diferentes intérpretes y compiladores pueden analizar estos aspectos en etapas anteriores como el analisis lexico y sintactico, lo cual puede resultar en una mezcla de estos. Que en este caso, por ejemplo, se evalúa la declaración previa de un identificador en caso de estar inmerso en una expresión desde el análisis léxico. Para el presente proyecto, en vista de que se están analizando los campos libres (expresiones y declaraciones) de manera individual, se decidió utilizar otro método de análisis el cual determina la validez semántica sin generar un árbol como el mencionado. Esto a razón de que se tuvieron determinados aspectos en cuenta en los análisis léxicos y sintácticos, por lo cual únicamente fue necesario un análisis semántico de segundo paso.


### Notacion polaca inversa.  
Alfonseca  lo denota como una de las alternativas de código intermedio o análisis de segundo paso, ya que otra alternativa son las cuádruplas (tema que no se abordará ya que no se incorporó en el proyecto). La notación polaca inversa o notación postfija tiene el propósito de transcribir la expresión en un orden tal que para el sistema le sea más claro operar respetando la jerarquía de los operadores. En la Tabla 1 se puede evidenciar un ejemplo de transcripción en notación polaca inversa.


Tabla 1. Ejemplos de expresiones en notación polaca inversa.

 | Expresión | Notación sufija |
| --- | --- |
| `a*b` | `a b *` |
| `a*(b+c/d)` | `abcd/+*` |
| `a*(b+c*d)` | `ab*cd*+` |

Fuente: Alfonseca  (Capítulo 6.2.1) Compiladores e Intérpretes


Por medio de un algoritmo de transformación de notación infija a postfija se logró este objetivo haciendo uso de tecnologías como java.util.Stack,  java.util.List y  java.util.ArrayList. Donde se declaró una jerarquía como la que se puede apreciar en la Tabla 2.


Tabla 2. Jerarquía de los operadores.

| Operador | Prioridad |
| --- | --- |
| `|``|` | 1 |
| `&&` | 2 |
| `== != < > <= >=` | 3 |
| `+ -` | 4 |
| `* / %` | 5 |
| `!` | 6 |
| `()` | 7 |

Fuente: Propia


### Evaluación de notación polaca inversa.  
Posteriormente a la transcripción, se evalúa cada expresión únicamente respecto al tipo de dato generado tras cada operación. La evaluación de estas notaciones procede en la lectura de la expresión, almacenando los operandos en una pila (stack), y encontrado un operador se recogen los últimos 2 operandos y se computará respecto al operador; una vez computado se almacena el resultado en la pila nuevamente. De esta manera es posible determinar si la expresión es adecuada para el campo donde se indica. Ejemplo de esto es la validación de que el resultado de la operación de una expresión en un campo condicional (sea una estructura if o while) coincida con el tipo de dato lógico en su resultado. De esta manera se puede corroborar si la expresión es correcta semánticamente.


En principio, los valores al ser evaluados desde la notación postfija poseen un inicial (cero, falso o texto vacío dependiendo del tipo de variable). Pero la evaluación en el momento de la ejecución, las variables si toman un sentido y valor respecto al entorno dinámico donde se desarrollan, más sin embargo la notación polaca inversa es la misma en el momento del análisis semántico. En la Figura 7 se puede apreciar un ejemplo de notificación de error semántico en el aplicativo.


Figura 7. Notificación de error semántico.

 <div style="display:flex">
<img src="https://64.media.tumblr.com/6ea4795955180a6d9a1ab13743cc3ec4/2a183850c94af93e-77/s500x750/84cd9df9275f1de823657b4f31e6021f54de753f.png" width="25%" >
<img src="https://64.media.tumblr.com/a45ba8cadfa31d63903971c1c4d8c836/2a183850c94af93e-65/s500x750/3bc1979bd919d587e2338d754e134c95bb6ea2d6.png" width="25%" >
</div> 

Fuente: Propia


### Tabla de símbolos.  
La tabla de símbolos, es una tabla encargada de almacenar cada uno de los identificadores que se encuentran en el pseudocódigo. Los símbolos para esta ocasión representan las variables o identificadores en el algoritmo. Es importante tener registro de estas para reconocer la variable, su tipo y valor en el momento de la evaluación de las expresiones. Para Alfonseca , existen diferentes maneras de albergar este registro bien sea desde una lista doblemente anidada hasta un árbol binario, más sin embargo su estructura refiere a una parte importante del intérprete debido al método de búsqueda que incorpora para el uso de identificadores registrados. Es por ello que el método más eficiente y veloz para la búsqueda de estos es haciendo uso de una  HashTable, la cual es una estructura en forma de tabla cuyo índice de almacenamiento recae en una llave para acceder su valor. Esta llave proviene de una particularidad del dato que se esté llamando la cual debe ser única para los elemento almacenados, en este caso puede ser el nombre ya que en los lenguajes formales de programación no es posible declarar la misma variable en el mismo entorno 2 veces. Esta particularidad no siempre es identificable por lo cual debe tratar el dato por medio de una función o método hash, el cual permite generar la llave correspondiente. Para el presente desarrollo se incorporó una tabla símbolos la cual en la Figura 8 se puede apreciar un ejemplo visual. Esta tabla cumple una función primordial  en el análisis léxico, en el cálculo de expresiones en notación polaca inversa y en el registro de la prueba de escritorio, ya que con ella se accede al valor de dicha variable y le hace posible asignar nuevos valores.


Figura 8. Ejemplo de tabla de símbolos usando una HashTable.

<div style="display:flex">
<img src="https://64.media.tumblr.com/86b2e69a98e4faec47a07738d7087889/f166869a32cc16a1-7e/s540x810/8755f3f2df1d5d7a4d1dffb036ec52fad3efd820.png" width="50%" >
</div> 

Fuente: Propia

## Secuenciador.  
En esta etapa, una vez validado el   algoritmo en términos léxicos, sintácticos y semánticos, se procede a secuenciar el pseudocódigo el cual es un proceso que en términos formales transcribe el algoritmo en lenguaje ensamblador. Este proceso suele ser riguroso ya que el resultado de la transcripción es una serie de instrucciones (granulares) dependientes del computador, microprocesador, microcontrolador u otro circuito integrado para el cual se esté desarrollando ya que este puede variar en el número de bits que constituye la arquitectura de la CPU. Este lenguaje ensamblador es la representación cercana al lenguaje máquina. Aun así, debido a que la herramienta expuesta constituye un intérprete y no un compilador. Para Alfonseca  un compilador y un intérprete, difiere en su ejecución, ya que un compilador recorre el algoritmo en lenguaje máquina sin analizar cada expresión, contrario a un intérprete. Además de ello, teniendo en cuenta que se está elaborando en un lenguaje de alto nivel (Java); se desarrolló un Simulador de conjunto de instrucciones compilado. Cabe aclarar la diferencia pues el propósito de este simulador es reproducir la ejecución del algoritmo manteniendo el entorno en un alto nivel respecto al procesador, es decir, excluyendo el lenguaje máquina o lenguajes intermedios. Es por ello que se generaron instrucciones simples que simularán este proceso netamente para Java.

Para poder reproducir estructuras básicas de alto nivel como lo son condicionales y ciclos (a nivel de hardware y en lenguaje ensamblador) no es posible reproducir limpiamente en el concepto teórico la composición de estos conceptos. Es por ello que internamente se simula su ejecución con una lista de instrucciones que incluyan saltos. Estos saltos son ejecutados dependiendo del resultado de las expresiones. En donde un condicional o un iterador condicional tendría definido su salto dependiendo del resultado de la expresión que lo compone. Por el contrario, en una iteración definida (ciclo for) internamente opera bajo la condición intermedia la cual define si el índice aún cumple con la cláusula mayor a 0. En la Figura 9 se puede apreciar un ejemplo de pseudocódigo y la lista de instrucciones generada partiendo del mismo.

Figura 9. Ejemplo de pseudocódigo y de lista de instrucciones del mismo.

<div style="display:flex">
<img src="https://64.media.tumblr.com/07ef3f53dc76aa29a009dc05091da4c3/77c5b2ee809297c5-ad/s1280x1920/378ced0769ff7d36a1abb635113d437183253d66.png" width="50%" >
</div> 

Fuente: Propia


En la Figura 9 se puede apreciar una lista de instrucciones en el area de Consola de Errores la cual se constituye de 7 campos, el primero es el número de la instrucción, el segundo es el numero de linea al cual corresponde, el tercer y cuarto campo corresponde a las partes de la expresión (por ejemplo, en una asignación existen dos partes mientras que en una declaración solo existe una parte), el quinto campo corresponde al salto, posteriormente está el campo donde se denota el tipo de instrucción y finalmente, de ser una declaracion, el ultimo campo constituye el primer caracter del tipo de dato declarado. Para la generación de esta lista de instrucciones se utilizaron objetos de 2 tipos, nodos secuenciadores y nodos de cierre. Donde los nodos secuenciadores representan la instrucción granular, mientras que los nodos de cierre representan los saltos indicados.


### Nodo secuenciador.  
Los nodos secuenciadores se componen en este sistema de atributos como número de línea, número de línea para el salto, número de instrucción, tipo de instrucción, primera  y segunda parte de la expresión. Para las instrucciones que corresponden a bloques condicionales o iterativos, el valor del salto equivale al nodo de cierre (concepto explicado a continuación) mientras que para instrucciones simples como la asignación o declaración este valor constituye 0 ya que posee fin en la misma línea. 

### Nodo de cierre.  
Los nodos de cierre expresan el fin de un bloque, siendo este útil para indicar el fin de un condicional simple o compuesto, o el fin de alguno de los iteradores. Siendo este vital para el retorno del inicio del bloque e identificar si este ha culminado en su evaluación. Por ejemplo, al ejecutar la última iteración de un ciclo condicional es necesario verificar si la cláusula declarada en el inicio del bloque sigue siendo válida. Este nodo posee dos atributos, el número de instrucción y el tipo que corresponde al cierre.

Una vez explicado esto, la generación de la lista de instrucciones parte del pseudocódigo donde se analiza cada línea y se limpian las líneas vacías. En el análisis, si la línea comprende a una inicio de bloque entonces corresponde a un nodo de cierre y nodo secuenciador. Se procede a instanciar los nodos, el nodo secuenciador se adjunta a la lista de instrucciones mientras que el nodo de cierre se integra en una pila. En el momento de encontrar una línea que indique el cierre de un bloque, entonces se depura el último nodo de la pila y se le indica el salto (índice actual más uno de instrucciones) a la instrucción que denotaba el inicio del bloque, posteriormente se integra un nodo secuenciador con el tipo JUMP el cual en su atributo de salto indica el valor que poseía el nodo depurado de la pila. De esta manera en la ejecución, el intérprete se encarga de la evaluación de expresiones y obedece según su resultado a continuar con la siguiente instrucción o al salto indicado.


## Ejecutor.  
Para la simulación de ejecución, se recorre la lista de instrucciones y dependiendo del tipo de instrucción se evalúa 1 o 2 campos.  La evaluación de cada expresión se realiza con la última tabla de símbolos, es decir, la última que registre un cambio. De esta manera se asume el valor de las variables en la instancia actual. La evaluación de las expresiones reace en la evaluacion postfija que se vio anteriormente. En la evaluación de estas notaciones se verifica que los operando sean calculables respecto al tipo de dato esperado, también se verifica que cumpla con las normas aritméticas o lógicas. Por ejemplo la detección de una expresión incalculable a/b donde a es igual a 1 y b es igual a 0. Posteriormente, al obtener valores cuyos tipos de datos sean válidos para la expresión, se procede a tratar con la tabla de símbolos o a decidir el salto de la lista de instrucción (esto depende del tipo de instrucción). 


### Declaración.  
En el momento de encontrar una declaración, se busca la variable en la tabla de símbolos y se inicializa su valor. Este valor de inicio depende del tipo de dato al que pertenezca. Una vez asignado el valor, se indica en el registro el tipo de operación efectuada y en la prueba de escritorio automática (en la columna de la variable y en la fila de la línea) se indica el valor nuevo valor el cual asume dicha variable. 


### Asignación.  
En este caso, busca la variable indicada en el 1 campo y se almacena el tipo de dato correspondiente a la variable encontrada. Posteriormente se evalúa la notación postfija la cual está declarada en el 2 campo, si la evaluación de esta expresión es exitosa entonces se asigna el nuevo valor en la tabla de símbolos, se indica en la prueba de escritorio el nuevo valor. 


### Condicional e Iteración condicional.  
A razón de que esta instrucción expresa un bloque condicional, se evalúa la expresión postfija en el 1 (y único) campo. Si la evaluación de esta expresión es exitosa y su resultado es de tipo lógico, se decide el salto que tendrá el ejecutor, bien sea en la siguiente instrucción o en la instrucción que procede al cierre del bloque. 


### Iteración definida.  
En este caso particular se toma el valor simple expresado en el 1 campo de tipo entero positivo, se resta 1 unidad y se asigna en el campo su nuevo valor. En caso de que este nuevo valor sea igual a 0, se procede a indicar el salto a la instrucción posterior al fin del bloque, se asigna su valor inicial (denotado en la tabla de símbolos de manera oculta) y efectúa el salto. De lo contrario, solo se asigna el valor en la expresión y se continúa en la siguiente línea. Nuevamente se registra su resultado, pero no se declara ningún valor en la prueba de escritorio. 


### Lectura.  
En caso de que la expresión sea de tipo lectura, se verifica si el la línea correspondiente a la línea de la instrucción en la columna de Lectura en la consola de entradas posee algún valor, en caso contrario se frena la ejecución hasta no cumplir esta cláusula. En caso de estar lleno el campo, se hace búsqueda de la variable perteneciente a la instrucción (denotada en el 1 campo), se almacena el tipo de dato, se transcribe la expresión del campo de lectura en notación polaca inversa, se evalúa y se verifica el tipo de dato del resultado respecto al tipo de dato de la variable. Si este proceso es exitoso, se asigna a la variable su nuevo valor en la tabla de símbolos, se registra el cambio en la prueba de escritorio,y finalmente se declara el tipo de operación y el resultado.


### Escritura.  
Si la instrucción es de tipo escritura, solo se evalúa la expresión en notación polaca inversa del método ubicada en el 1 campo, y su resultado se convierte en un tipo de dato texto. Posteriormente se registra su resultado.

En la Figura 10 se puede ver una instantánea en el momento de ejecución.

Figura 10. Instantánea de ejecución.

<div style="display:flex">
<img src="https://64.media.tumblr.com/19981f5db31a4278e9851e590b7ef5d1/b8f51aeb7b731568-cc/s1280x1920/af57846f6506af71a2cddf218bfbe9555ac1df92.png" width="50%" >
</div>
 
Fuente: Propia 
