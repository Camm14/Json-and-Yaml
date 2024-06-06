# Json-and-Yaml #
![imagen Json_Yaml](https://pbs.twimg.com/media/Eh0RiJqX0AAWIAZ.jpg)
## JSON(JavaScript Object Notation)
Es un formato de texto pensado para el intercambio de datos, su sintaxis esta basada en JavaScript; pero es independiente de cualquier programa de programación.

### Características principales de JSON:
+ Estructura de datos simple basada en pares clave-valor.
+ Soporta diferentes tipos de datos como cadenas, números, booleanos, listas y objetos.
+ Fácilmente legible por máquinas y humanos.
+ Muy utilizado en APIs RESTful para intercambiar información estructurada.

 ### Sintaxis de JSON
 + matrices (arrays): Las matrices son listas de valores separados por comas. Las matrices se escriben entre corchetes [ ].  ``` [1, "pepe", 3.14, "Pepito Conejo"]```
 + objetos (objects). Los objetos son listas de parejas nombre / valor. El nombre y el valor están separados por dos puntos : y las parejas están separadas por comas. Los objetos se escriben entre llaves { } y los nombres de las parejas se escriben siempre entre comillas dobles. ``` {"nombre": "Pepito Conejo", "edad": 25, "carnet de conducir": true}. ```
 + Los espacios en blanco y los saltos de línea no son significativos, es decir, puede haber cualquier número de espacios en blanco o saltos de línea separando cualquier elemento o símbolo del documento. ```  [
  {
    "nombre": "Pepito Conejo",
    "edad": 25,
    "carnet de conducir": true
  },
  {
    "nombre": "Ana Barberá",
    "edad": 90,
    "carnet de conducir": false
  }
] ```
### No Hacer
![imagen Json_Yaml](https://upload.wikimedia.org/wikipedia/commons/thumb/5/5f/Red_X.svg/100px-Red_X.svg.png)
 + Un documento JSON está formado por un único elemento (objeto o matriz).```[1, 2, 3], ["a", "b", "c"] ``` ,  ``` "nombre": "Pepito Conejo"```
 + Tanto en los objetos como en las matrices, el último elemento no puede ir seguido de una coma ```{"nombre": "Pepito Conejo",} ``` , ```["nombre": "Pepito Conejo", "edad": 25, "carnet de conducir": true, ] ```
   
 ### Datos importantes de JSON
 + Los valores (tanto en los objetos como en las matrices) pueden ser:  ``` números, cadenas, valores true, false y null. ```
 + Los ficheros ``` JSON ``` no pueden contener comentarios.
   

### JSON-RPC: JSON Remote Procedure Call
+ ```jsonrpc``` una cadena que indica la versión ("2.0")
+ ```method``` una cadena que indica el método invocado.
+ ```params``` (optativo) una matriz o una lista de valores
+ ```id``` un número o cadena establecido por el cliente
 Si una llamada no incluye identificador id, se considera que es una notificación y no requiere respuesta, ni siquiera en caso de error.

### La respuesta RPC tiene que seguir también la sintaxis de JSON y contener los siguientes campos:

+ ```jsonrpc``` una cadena que indica la versión ("2.0") 
 uno de estos dos campos:
+ ```result``` (optativo) el resultado de la consulta, en forma de valor, matriz o lista.
+ ```error``` (optativo) una matriz o una lista de errores, con la estructura siguiente:
  + ```code``` código de error (número entero).
  + ```message``` descripción breve del error.
  + ```data``` (optativo) matriz o lista de valores con información adicional sobre el error.
+ ```id``` el número o cadena establecido por el cliente.

  ### Una llamada JSON-RPC puede contener varias peticiones en forma de matriz y se debe contestar con una matriz de respuestas (salvo que todas las llamadas sean notificaciones, en cuyo caso no habría respuesta).

Ejemplos de llamada y respuesta:

   + Petición  ```{
  "jsonrpc": "2.0",
  "method": "suma",
  "params": [3, 4, 5],
  "id": 181203
} ```
   + Respuesta ```{
  "jsonrpc": "2.0",
  "result": 12,
  "id": 181203
} ```
 
## YAML (YAML Ain't Markup Language)
Es un formato de texto pensado para la serialización de datos, con una alternativa a XML, su sintaxis combina conceptos de varios lenguajes (HTML, C, Perl y Python).

### Características principales de YAML:
+ Lenguaje simple y legible por humanos.
+ Soporta listas, diccionarios y tipos de datos complejos.
+ Fácil de aprender y usar.
+ No permite el uso de etiquetas o marcas específicas como otros lenguajes de marcado

