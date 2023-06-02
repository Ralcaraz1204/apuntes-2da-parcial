![](file:///C:/Users/52313/OneDrive/Documentos/1.jpg)

class Estudiante {

  String nombre = "";
  int? aNacimiento;
}

void reporte(Estudiante e) {
  print("Nombre: ${e.nombre}");
  print("Edad: ${2023 - e.aNacimiento!}");
  

 
  ![](file:///C:/Users/52313/OneDrive/Documentos/2.jpg)
  
  class Animal {
  String nombre = "";
  String sonido = "";
}

void reporte(Animal a) {
  print("Nombre: ${a.nombre}");
  print("Sonido: ${a.sonido}");
} 


![](file:///C:/Users/52313/OneDrive/Documentos/3.jpg)

void main(List<String> args) {
  Dias d1 = new Dias('martes', 25, 'abril');
  d1.calcula(2023);
}

class Dias{
  String? dia ;
  int? numeroDia ;
  String? mes ;
  Dias(String dia, int numeroDia, String mes){
    this.dia = dia;
    this.mes = mes;
    this.numeroDia = numeroDia;
      }
  void calcula(int a_Actual){
    print('hoy es $dia $numeroDia del mes de $mes del $a_Actual');
  }

}


![](file:///C:/Users/52313/OneDrive/Documentos/4.jpg)

class Figura{
  int? base;
  int? altura;
Figura.rectangulo(this.base, this.altura);
Figura.cuadrado(this.base, );


int arearectangulo(){
  if(altura ==null  || base == null){
  print("no se puede calcular");
  return 0;
}
return base! * altura!;
}

int areacuadrado(){
  int res = 0;
  if (base == null){
    print("no se puede calcular");
  }else{
    res = base! * base!;
  }
  return res;
}
}

int perimetrorectangulo(int base, int altura){
  return 2 * base + 2 * altura;
}
int perimetrocuadrado(int base){
  return 4 * base;
}


![](file:///C:/Users/52313/OneDrive/Documentos/5.jpg)

class Shape{

  int? _base;
  
  int? _altura;
  

  Shape(this._base, this._altura);
  
  int getArea(){
  

    return _calcularArea();
    
  }
  
  int _calcularArea(){
  
    return _base! * _altura!;

  }
  
  void set base(int base){
    _base = base;
  } 
  
  //seters
  
  void set base(int? base) => _base = base;
  
  void set altura(int? altura) => _altura = altura;
  
  //geteers
  
  int? get base => _base;
  
  int? get altura => _altura;
}


![](file:///C:/Users/52313/OneDrive/Documentos/6.jpg)

class Auto{

  String _marca;
  
  int _modelo;
  
  String _transmision;
  
 String _color;
 
  
  Auto(this._marca, 
  
  this._modelo, 
  
  this._transmision, 
  
  this._color);

void set marca(String marca) => this._marca = marca;

void set modelo(int modelo) => this._modelo = modelo;

void set transmisison(String transmision) => this._transmision = transmision;

void set color(String color) => this._color = color;

String get marca => this._marca;

int get modelo => this._modelo;

String get transmisison => this._transmision;

String get color => this._color;


void showAuto(){

  print(''' marca : ${this._marca}
  
  modelo: ${_modelo}
  
  transmision : ${_transmision}
  
  color : ${_color} ''');

}
  }
  
  ![](file:///C:/Users/52313/OneDrive/Documentos/7.jpg)
  
  void main(List<String> args) {
  
  Animal a1 = Animal('vaca', 10);
  
  a1.instancia();
  
  Animal.instanciaStatic();
  
  print('-' *20);
  
  Animal a2 = Animal('CERDO', 20);
  
  a2.instancia();
  
  Animal.instanciaStatic();
  
  Animal a3 = Animal('vaca', 10);
  
  a3.instancia();
  
  Animal.instanciaStatic();
  
  print('-' *20);
  
  List<Animal> animales=[a1,a2,a3];
  
  int suma =0;
  
  animales.forEach((element) {
  
    suma += element.cantidad;
    
   });
   
   print('total de animales: $suma');
   
} 
class Animal{

  String tipoAnimal;
  
  int cantidad;
  
  static int cantidadS = 0;
  

  Animal(this.tipoAnimal, this.cantidad){
  
    cantidadS ++;
     }
     
  void instancia(){
  
    print('el animal es: $tipoAnimal');
    
    print('la cantidad es: $cantidad');
    
  }

  static void instanciaStatic(){
    
    print('la cantidad es:$cantidadS');
    
  }
}



![](file:///C:/Users/52313/OneDrive/Documentos/unnamed8.jpg)


class Animal {
  String? breed;
  int? quantity;

String? get getBreed => breed;
int? get getQuantity => quantity;

set setBreed(String? breed) => this.breed = breed;
set setQuantity(int? quantity) => this.quantity = quantity; 

  void showProperties() {
    print("Name: pekines");
    print("Quantity: $quantity");
  }
}

import 'animal.dart';

class Caballo extends Animal {

  String? tipo_crin;
  @override
  void showProperties() {
    super.showProperties();
    print("tipo de crin: $tipo_crin");
  }
}


import 'animal.dart';
class Pato extends Animal {

  String? tipo_pico;
  @override
  void showProperties() {
    super.showProperties();
    print("tipo de pico: $tipo_pico");
  }
}

import 'animal.dart';

class Vaca extends Animal {

  String? tipo_cola;
  @override
  void showProperties() {
    super.showProperties();
    print("tipo de cola: $tipo_cola");
  }
}


![](file:///C:/Users/52313/OneDrive/Documentos/unnamed9.jpg)

void main(List<String> args) {
  final Carro jeep= Carro("Rojo", 100, "jeep", "SUV");
  jeep.showVehiculo();
  jeep.maximaVelocidad();

  final Motocicleta yamaha= Motocicleta("Azul", 50, "r6");
  yamaha.showVehiculo();
  yamaha.maximaVelocidad();
}


abstract class Vehiculo{

  String? _color;
  int? _velocidad;

  Vehiculo(this._color, this._velocidad){
    print("costructor padre Vehiculo");
  }
  set color(String? color) => this._color = color;
  set velocidad (int? velocidad) => this._velocidad = velocidad;

  String? get color => this._color;
  int? get velocidad => this._velocidad;

  int maximaVelocidad() => _velocidad! * 2;

  void showVehiculo(){
    print("Color: $_color");
    print("Velocidad: $_velocidad");
  }
}

class Carro extends Vehiculo{
  String? _marca;
  String? _tipo;

  Carro(super._color, super._velocidad, this._marca, this._tipo ){
    print("costructor hijo Carro");
  }
  
  @override
  void showVehiculo(){
    super.showVehiculo();
    print("Marca: $_marca");
    print("Tipo: $_tipo");
  }

}

class Motocicleta extends Vehiculo{
  String? _marca;
 
  Motocicleta(super._color, super._velocidad, this._marca, ){
    print("costructor hijo Motocicleta");
  }
  
  @override
  void showVehiculo(){
    super.showVehiculo();
    print("Marca: $_marca");
   
  }

}



![](file:///C:/Users/52313/OneDrive/Documentos/unnamed10.jpg)

void main(List<String> args) {

    Dolphin flippy= Dolphin();
    flippy.swim();
  }

class Animal{

  Animal (){
    print("animal constructor");
    

  }
}
class Mammal extends Animal{

  Mammal(){
  
    print("Mammal constructor");
    
  }
  
}
class Bird extends Animal{


  Bird(){
  
    print("Bird constructor");
    
  }
}

class Fish extends Animal{

  Fish(){
  
    print("Fish constructor");
  }
}

abstract class Swimmer{

  void swim(){
  
    print("Swimming");
  }
}

class Dolphin extends Mammal with Swimmer{

  Dolphin(){
  
    print("Dolphin constructor");
  }
}
 