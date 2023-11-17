[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ytCADFsI)

## **Diferencia entre Clase y Objeto**

Una clase funciona como un "esqueleto" o una forma abstracta que define tanto los atributos como los métodos de un objeto o entidad, especificando la manera en la que deben ser creados estos objetos. En cambio, un objeto es una instancia específica de esa clase, es decir, es la entidad que posee valores particulares para sus atributos. La clase es la idea "abstracta”, y el objeto es la implementación de dicha idea.

## **Diferencia entre Clase e Interfaz**

Una clase funciona como plantilla que define tanto la abstracción como la implementación de los métodos del objeto, especificando sus valores. Por otra parte, una interfaz, define métodos de manera abstracta, es decir, en dicha interfaz no se hará la implementación, pues funcionará como un contrato que las clases (que implementen esta interfaz) deben seguir, por ello se relaciona con el concepto de “Programación Bajo Contrato”.

## **¿Qué es el polimorfismo?**

El polimorfismo se refiere a la capacidad o la forma de abstracción que permite que diferentes clases puedan reutilizar fragmentos de código específicos, como métodos. En otras palabras, objetos de clases distintas pueden interpretar y responder a un mismo método de manera específica para cada clase.

### **Ejemplo con el proyecto (Inventario con RFID)**

El polimorfismo aplicado a las clases Usuario y Empleado permite que objetos de ambas clases respondan de manera única a un método común, como por ejemplo mostrarDetalles(). Aunque ambas comparten este método, cada clase tiene su propia implementación específica. La clase Usuario podría mostrar información básica, como el nombre del usuario, mientras que la clase Empleado que hereda de Usuario podría proporcionar detalles adicionales, como el rol del empleado.

## **¿Qué representan las asociaciones en un DC (Diagrama de Clases)?**

En un Diagrama de Clases, las asociaciones representan las relaciones entre las clases. Estas relaciones indican cómo las instancias de una clase interactúan con las instancias de otra clase. Las asociaciones son esenciales para modelar la interacción y la colaboración entre diferentes objetos.

### **Código (herencia entre Usuario y Empleado en el proyecto)**

En el contexto de herencia entre las clases Usuario y Empleado, la herencia representa una relación jerárquica donde la clase Empleado hereda atributos y métodos de la clase Usuario. La clase Usuario actúa como una clase "padre”, proporcionando atributos y métodos comunes para todos los usuarios del sistema. Por otro lado, la clase Empleado, la clase “hija”, extiende esta funcionalidad al agregar atributos específicos para los empleados, como un puesto.

## **Diferencia entre Composición y Agregación**

La composición implica una relación más fuerte, donde una clase (compuesta) está compuesta por otras clases (componentes) y no pueden existir de manera independiente. En cambio, la agregación implica una relación más débil, donde una clase (agregadora) puede contener instancias de otra clase (agregada), pero estas pueden existir de manera independiente.

### **Ejemplo aplicado al proyecto (sistema de inventario)**

La composición podría representarse si consideramos una clase principal llamada Inventario, compuesta por otra clase como Producto. Los productos existen en el inventario y no tienen sentido fuera de él, y el inventario se encarga de gestionar y controlar directamente los productos. En cambio, la agregación podría aplicarse si tenemos una clase Pedido que agrega temporalmente productos al inventario. En este escenario, los productos pueden existir de manera independiente del pedido.

## **¿Qué es el encapsulamiento?, ¿Qué ventaja representa?**

Definido como la implementación interna de un objeto y la exposición de solo la interfaz necesaria para interactuar con él. Se logra mediante la definición de atributos y métodos como públicos, privados o protegidos, controlando así el acceso. La ventaja principal del encapsulamiento es que permite el control y la protección de los datos internos de una clase, evitando modificaciones no autorizadas.

En un sistema de inventario, el encapsulamiento podría aplicarse mediante una clase Producto, donde el atributo, como la cantidad disponible en el inventario, se define como privado. Se podrían proporcionar métodos públicos para acceder y actualizar la cantidad de productos de manera controlada.

## **¿De qué manera se representa la Modularidad en POO?**

La Modularidad se representa mediante la capacidad de dividir un programa en módulos o fragmentos de código independientes y reutilizables. Cada clase en POO actúa como un módulo que encapsula una funcionalidad o responsabilidad específica, permitiendo cambios en un módulo sin afectar el resto del programa.

Por ejemplo, en un sistema de inventario, podríamos tener clases o métodos separados para gestionar productos, manejar el almacenamiento y gestionar o eliminar pedidos.

## **Considera Polimorfismo. ¿Cuál es la diferencia de usar Herencia vs Interfaz?**

La herencia permite que una clase herede atributos y métodos de otra clase, aceptando la reutilización del código. En cambio, las interfaces establecen contratos que las clases deben cumplir, permitiendo a diferentes clases implementar la misma interfaz sin compartir una relación directa.

La ventaja de la herencia radica en la facilidad de compartir código entre clases relacionadas, pero puede generar una jerarquía compleja. Por otro lado, las interfaces permiten una mayor flexibilidad al no requerir una relación lógica directa, facilitando la adaptación a cambios y la inclusión de funcionalidades en clases no relacionadas.
