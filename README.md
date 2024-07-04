# flutter20240704

# variables:
* Para definir una variable se escribe lo siguiente:
   * **tipodedato** **nombrevariable**= **opcionalmente el valor**;
   * var **nombrevariable**=**valor**
* Tipos de datos:
   * int: entero
   * double: decimal
   * String: texto
   * bool: booleano (true o false)
   * List: listado
       *  var paises=["Chile","Argentina","Peru"]; // en algunos casos define un List<dynamic>
       *  List<String> paises=["Chile","Argentina","Peru"]; 
   * Map: define un arreglo (diccionario)
       *  var producto={"nombre":"cocacola","precio":200};
       *  Map<String,dynamic> producto={"nombre":"cocacola","precio":200};
   * dynamic: un tipo de dato variable
   * objetos
* Si el tipo de dato termina con un simbolo de pregunta: "int?" entonces el valor admite nulo. 
  

```dart
void main() {
  int numero1=20;
  var numero2=30;
  int? numero3=null;
  String? texto="hola";  
  print("El valor del numero 1 es: ${numero1}");
  print(numero2);
  print(numero3);
  print(texto);
  print(numero1+numero2);
  if(numero3!=null) {
    print(numero1+numero3);
  }
  bool valido; // indefinido (no es nulo)  
  valido=true;
  print(valido);
  var valido2=true;
  print(valido2);
  var paises=["Chile","Argentina","Peru"];
  var cliente={"Nombre":"john","apellido":"doe"};
  dynamic vardin="222";
  print(paises);
  print(cliente);
  print(vardin);  
}
```
## clases
* Para definir una clase, se ocupa la siguiente notacion:  class **nombre** { }
* Las clases no necesariamente tienen que ir dentro de un archivo separado.
* Las clases se recomiendan que partan en mayuscula.
   * Ejemplo : OK
   * ejemplo : NO
* En el lenguaje dart, si agrego un archivo de codigo, siempre es en minuscula.     
```dart
class Ejemplo {
  
}

void main() {
  var obj=new Ejemplo();
  print(obj);
}
```
## ejemplo lista usando mapas

```dart
class Producto {
  // campo
  // en dart no se definen propiedades y los campos son publicos
  String nombre;
  int precio;
  // constructor
  Producto(this.nombre,this.precio);
}

void main() {
  // tabla de productos
  // nombre | precio
  // --------------------
  var productos=[
    {"nombre":"cocacola","precio":100},
    {"nombre":"fanta","precio":200},
    {"nombre":"sprite","precio":400},
  ];
  print(productos);
  List<Map<String,dynamic>> productos2=[
    {"nombre":"cocacola","precio":100},
    {"nombre":"fanta","precio":200},
    {"nombre":"sprite","precio":400},
  ];  
  print(productos2);
  var prod1=Producto("cocacola",100);
  var prod2=Producto("fanta",200);
  var prod3=Producto("sprite",300);
  var productos3=[prod1,prod2,prod3];
  print(productos3);
  List<Producto> productos4=[
    Producto("cocacola",100),
    Producto("fanta",200),
    Producto("sprite",300)
  ];
  print(productos4);
  
}
```
# constructores y clases

```dart
class Cliente {
  // campos
  String nombre;
  String apellido;
  String direccion;
  int edad;
  
  Cliente(this.nombre,this.apellido,this.direccion,this.edad);
  Cliente.solonombre(this.nombre,this.apellido):
    this.direccion="",
    this.edad=0; 
}

void main() {
  var cli=Cliente("john","doe","sunset",200);
  var cli2=Cliente.solonombre("anna","smith");
  
}
```
