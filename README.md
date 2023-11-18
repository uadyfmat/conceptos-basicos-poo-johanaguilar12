[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/ytCADFsI)

## Johan Ricardo Aguilar Pérez - Conceptos POO

## **Diferencia entre Clase y Objeto**

Una clase actúa como un "esqueleto" o una forma abstracta que define tanto los atributos como los métodos de un objeto o entidad, especificando la manera en que deben crearse estos objetos. En cambio, un objeto es una instancia específica de esa clase; es decir, es la entidad que posee valores particulares para sus atributos. La clase proporciona una idea "abstracta", mientras que el objeto representa la implementación concreta de esa idea, llevándola a la realidad con valores específicos.

## **Diferencia entre Clase e Interfaz**

Una clase funciona como una plantilla que establece tanto la abstracción como la implementación de los métodos de un objeto, definiendo su estructura y especificando los valores asociados. En contraste, una interfaz define métodos de manera abstracta, sin proporcionar implementaciones concretas. Actúa como un contrato que las clases que la implementan deben seguir, vinculándose así al concepto de "Programación Bajo Contrato". En este enfoque, las clases se comprometen a cumplir con el contrato establecido por la interfaz 

## **¿Qué es el polimorfismo?**

El polimorfismo se refiere a la capacidad o la forma de abstracción que permite que diferentes clases puedan reutilizar fragmentos de código específicos (como métodos). En otras palabras, objetos de clases distintas pueden interpretar y responder a un mismo método de manera específica para cada clase.

### **Ejemplo con el proyecto (Inventario con RFID)**

El polimorfismo aplicado a las clases Usuario y Empleado permite que objetos de ambas clases respondan de manera única a un método común, como por ejemplo mostrarDetalles(). Aunque ambas comparten este método, cada clase tiene su propia implementación específica. La clase Usuario podría mostrar información básica, como el nombre del usuario, mientras que la clase Empleado que hereda de Usuario podría proporcionar detalles adicionales, como el rol del empleado.

## **¿Qué representan las asociaciones en un DC (Diagrama de Clases)?**

En un Diagrama de Clases, las asociaciones representan las relaciones entre las clases. Estas relaciones indican cómo las instancias de una clase interactúan con las instancias de otra clase. Las asociaciones son esenciales para modelar la interacción y la colaboración entre diferentes objetos.

### **Código (herencia entre Usuario y Empleado en el proyecto)**

En el contexto de herencia entre las clases Usuario y Empleado, la herencia representa una relación jerárquica donde la clase Empleado hereda atributos y métodos de la clase Usuario. La clase Usuario actúa como una clase "padre”, proporcionando atributos y métodos comunes para todos los usuarios del sistema. Por otro lado, la clase Empleado, la clase “hija”, extiende esta funcionalidad al agregar atributos específicos para los empleados, como un puesto.

## **Diferencia entre Composición y Agregación**

La composición implica una relación más fuerte, donde una clase compuesta está formada por otras clases componentes y no puede existir de manera independiente. En otras palabras, la existencia de la clase compuesta depende completamente de las clases componentes. Si la clase compuesta se destruye, sus componentes también lo son.

En cambio, la agregación implica una relación más débil. En esta relación, una clase agregadora puede contener instancias de otra clase agregada, pero estas instancias pueden existir de manera independiente. La destrucción de la clase agregadora no implica necesariamente la destrucción de las instancias de la clase agregada.

### **Ejemplo aplicado al proyecto (sistema de inventario)**

La composición podría representarse considerando una clase principal llamada Inventario, que está compuesta por otra clase, como Producto. En este caso, los productos existen dentro del inventario y no tienen sentido fuera de él. El inventario se encarga de gestionar y controlar directamente los productos. La existencia de los productos está vinculada completamente al inventario, si se elimina el inventario, los productos también se eliminan.

En cuanto a la agregación, esta podría aplicarse en el contexto de una clase Pedido que agrega temporalmente productos al inventario. Los productos pueden existir de manera independiente del pedido, aunque el pedido contiene temporalmente referencias a productos, estos productos no están directamente vinculados a la existencia del pedido.

## **¿Qué es el encapsulamiento?, ¿Qué ventaja representa?**

El encapsulamiento se refiere a la implementación interna de un objeto y la exposición solo de la información necesaria para interactuar con él. Esto se logra mediante la definición de atributos y métodos como públicos, privados, protegidos o default, controlando así el acceso a ellos. La ventaja principal del encapsulamiento es que permite el control y la protección de los datos internos de una clase, evitando modificaciones no autorizadas.

En un sistema de inventario, el encapsulamiento podría aplicarse mediante una clase Producto, donde el atributo, como la cantidad disponible en el inventario, se define como privado. Se podrían proporcionar métodos públicos para acceder y actualizar la cantidad de productos de manera controlada. Esto significa que la modificación de la cantidad de productos se realizaría a través de estos métodos públicos, lo que proporciona una capa de control y seguridad sobre los datos internos de la clase Producto.

## **¿De qué manera se representa la Modularidad en POO?**

La Modularidad se representa mediante la capacidad de dividir un programa en módulos o fragmentos de código independientes y reutilizables. Cada clase en POO actúa como un módulo que encapsula una funcionalidad o responsabilidad específica, permitiendo cambios en un módulo sin afectar el resto del programa.

Por ejemplo, en un sistema de inventario, la modularidad se ve reflejada al organizar las responsabilidades en clases (módulos) independientes, cada una enfocada en tareas específicas. Por ejemplo, la clase Producto se encarga de representar y gestionar la información detallada de un producto, mientras que la clase Almacenamiento administra el inventario y sus operaciones; por último, La clase Pedido se centra en representar y procesar pedidos. Así, pueden realizarse cambios sin afectar directamente otras partes del sistema de inventario.

## **Considera Polimorfismo. ¿Cuál es la diferencia de usar Herencia vs Interfaz?**

La herencia proporciona una forma de reutilizar el código al permitir que una clase herede atributos y métodos de otra, estableciendo una relación jerárquica. Sin embargo, la desventaja radica en que puede generar jerarquías complicadas y, a veces, resultar en una fuerte dependencia entre clases, lo que podría limitar la flexibilidad y complicar futuras modificaciones.

Por otro lado, las interfaces establecen contratos que las clases deben cumplir, pero no definen la implementación concreta de los métodos; esto permite que clases no relacionadas implementen la misma interfaz, brindando una flexibilidad significativa. Esta flexibilidad es útil para adaptarse a cambios y para integrar nuevas funcionalidades de manera más independiente. Sin embargo, el uso extensivo de interfaces puede llevar a una implementación repetitiva en múltiples clases, aumentando la complejidad del código.
