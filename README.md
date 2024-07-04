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
