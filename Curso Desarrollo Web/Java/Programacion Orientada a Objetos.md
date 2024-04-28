![[Pasted image 20240417154235.png]]
![[Pasted image 20240417154241.png]]
![[Pasted image 20240417154354.png]]
## Paradigma de programacion
Un paradigma de programación es un enfoque o estilo fundamental para programar que los desarrolladores utilizan para estructurar, realizar y mantener sus programas. Cada paradigma representa una visión distinta de cómo se deben implementar y manejar las soluciones a los problemas a través del código. Los paradigmas de programación no son mutuamente excluyentes, y muchos lenguajes de programación admiten múltiples paradigmas, permitiendo a los desarrolladores elegir el más adecuado para cada tarea

1. **Imperativo**: Se centra en describir cómo se ejecutan las computaciones paso a paso. Se controla el estado del programa mediante asignaciones y se utiliza bucles y condicionales para manejar la ejecución. Ejemplos de lenguajes imperativos son C y Python.
    
2. **Declarativo**: En contraste con el imperativo, este paradigma se enfoca en qué se debe lograr sin especificar cómo se debe hacer. Los lenguajes que siguen este paradigma, como SQL y HTML, permiten describir el resultado deseado más que el proceso para llegar a él.
    
3. **Funcional**: Este paradigma trata las funciones matemáticas como ciudadanos de primera clase, promoviendo el uso de funciones puras y evitando el estado compartido y los datos mutables. Lisp y Haskell son ejemplos de lenguajes de programación funcional.
    
4. **Orientado a objetos (OO)**: Basado en el concepto de "objetos", que son instancias de clases que contienen datos en forma de campos (también conocidos como atributos) y código en forma de procedimientos (métodos). Java y C# son ejemplos de lenguajes orientados a objetos.
    
5. **Lógico**: Basado en la lógica formal, principalmente la lógica de predicados. Un programa lógico consta de un conjunto de hechos y reglas que describen relaciones y permiten la inferencia automática de nuevas relaciones. Prolog es uno de los lenguajes de programación lógica más conocidos.

## Diferencias 
1. **Imperativo vs. Declarativo**:
    
    - **Imperativo**: Se enfoca en el "cómo" de las operaciones. Los desarrolladores escriben código que especifica paso a paso las operaciones que la computadora debe realizar para alcanzar un objetivo. Esto puede dar más control sobre el flujo y el estado del programa, pero puede ser más complejo y propenso a errores.
    - **Declarativo**: Se concentra en el "qué" del resultado deseado más que en cómo lograrlo. Reduce la carga de cómo se manejan las operaciones a bajo nivel, lo que puede resultar en código más conciso y fácil de entender. Sin embargo, puede ofrecer menos control sobre el flujo exacto del programa.
2. **Orientado a Objetos vs. Funcional**:
    
    - **Orientado a Objetos (OO)**: Encapsula datos y comportamientos juntos en objetos, lo cual puede ser muy efectivo para modelar entidades del mundo real y relaciones complejas. Sin embargo, puede llevar a jerarquías de clases complicadas y a un acoplamiento estrecho entre partes del código.
    - **Funcional**: Al evitar el estado compartido y enfocarse en funciones puras, puede ofrecer soluciones más estables y predecibles. Esto es particularmente útil en sistemas donde la confiabilidad y la facilidad de testeo son críticas.


![[Pasted image 20240417154741.png]]
![[Pasted image 20240417155229.png]]
![[Pasted image 20240417155353.png]]
![[Pasted image 20240417155646.png]]
![[Pasted image 20240417155813.png]]
![[Pasted image 20240417160051.png]]
![[Pasted image 20240417160317.png]]
1. **Atributo**: Un atributo es una variable asociada con una clase que contiene datos que son pertinentes a los objetos creados a partir de esa clase. Los atributos son también conocidos como propiedades o campos. En esencia, son las características que definirán el estado de los objetos de una clase. Por ejemplo, para una clase `Coche`, los atributos podrían incluir `color`, `marca`, `modelo`, etc.
    
2. **Método**: Un método es una función que está asociada con una clase. Los métodos definen el comportamiento de los objetos de la clase. Son las acciones que un objeto de la clase puede realizar. Siguiendo con el ejemplo de la clase `Coche`, algunos métodos podrían ser `arrancar()`, `detener()`, `acelerar()`, etc.
    
3. **Constructor**: Un constructor es un tipo especial de método que se llama automáticamente cuando se crea un nuevo objeto de una clase. Su principal función es inicializar los atributos del nuevo objeto con valores específicos, aunque también puede contener cualquier tipo de inicialización que el objeto necesite antes de ser usado. Los constructores a menudo llevan el mismo nombre de la clase o se definen con un nombre especial, como `__init__` en Python.
    
4. **Instanciación**: Instanciar una clase es el proceso de crear un nuevo objeto a partir de esa clase. Al instanciar una clase, se invoca su constructor y se crea un nuevo objeto en memoria con sus atributos establecidos al estado inicial definido. Este nuevo objeto está listo para utilizar sus métodos y su comportamiento. Por ejemplo, si tienes la clase `Coche`, podrías instanciarla de la siguiente manera: `mi_coche = Coche()`, donde `mi_coche` sería un nuevo objeto de la clase `Coche`.
---

![[Pasted image 20240417160553.png]]
1. **Herencia**: Permite que una clase (llamada clase hija) herede atributos y métodos de otra clase (llamada clase padre), facilitando la reutilización de código y la creación de relaciones jerárquicas. Por ejemplo, imagina una clase general `Vehículo` que tiene atributos como `velocidad` y `color`, y métodos como `arrancar()` y `detener()`. Podrías tener una clase `Coche` que herede de `Vehículo` y, por lo tanto, obtenga todas esas características y comportamientos, pero además puedes añadir atributos específicos como `numeroDePuertas` y métodos específicos como `reproducirMúsica()`.
    
2. **Polimorfismo**: Se refiere a la habilidad de objetos de diferentes clases de ser tratados como instancias de una clase padre desde la perspectiva de la interfaz común que comparten. Por ejemplo, si `Coche` y `Motocicleta` son clases que heredan de `Vehículo`, ambas pueden ser tratadas como `Vehículo`. Esto significa que puedes tener una lista de `Vehículo`s y cada uno podría ser un `Coche` o una `Motocicleta`, y podrías llamar al método `arrancar()` en ellos, sin importar qué tipo de vehículo son realmente.
    
3. **Encapsulamiento**: Es el principio por el cual los datos internos de una clase (atributos) se ocultan al exterior y solo se pueden acceder a través de métodos públicos (getters y setters). Esto se hace para controlar cómo se leen o modifican los datos. Por ejemplo, si tienes un atributo `nivelDeGasolina` en la clase `Coche`, en lugar de hacerlo público, lo mantienes privado y proporcionas un método `verNivelDeGasolina()` para obtener su valor y un método `rellenarGasolina()` para cambiarlo.
    
4. **Abstracción**: Este pilar permite manejar la complejidad ocultando los detalles de implementación y mostrando solo la funcionalidad al usuario. Se crea una 'plantilla' o clase abstracta que define un conjunto de métodos abstractos que las clases derivadas deberán implementar. Un ejemplo sería una clase abstracta `Figura` que tiene un método `calcularArea()`. No puedes instanciar `Figura` porque no sabes cómo calcular el área en general, pero puedes tener clases específicas como `Circulo` y `Cuadrado` que implementan `calcularArea()` según sus propias fórmulas.
---
```JavaScript
/

* class: La clase es como una plantilla-molde con el que podemos crear un objeto

* constructor: Es una caracteristica que tiene las clases, es una funcion obligatoria que nos va a ayudar a construit el objeto. El constructor va a contener las propiedades o parametros de nuestra clase

* this.:Se refiere al objeto que estamos creando

* Metodo : Se refiere a lo que puede hacer nuestro objeto

* Instanciacion: Cuando se finalixa todo este proceso tenemos la clase instanciada (materializada) (new)

* Atributo : Es una caracteristica o propiedad asociado a un objeto

* Abstraccion : Se basa en reducir al objeto, es decir que sea lo menos complejo posible

* Herencia : Se refiere a que cuando creamos una clase, va a tomar todo lo que tiene esa clase y se lo va a "heredar" (pasar) a la siguiente clase (subclase)

* Polimorfismo : Tener instancias de clases diferentes, pero responden al mismo metodo pero de forma diferente. Como un objeto se comporta de forma distinta ante el mismo metodo

 /
```