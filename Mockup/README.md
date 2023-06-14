## Prueba técnica desarrollador Junior

### Ejercicios de lógica de programación

**1. Función para la verificación de palíndromos**

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/7234512d-d1d2-4137-8493-88c5d4a3699b)

Para cumplir con el objetivo del ejercicio se plantea una funcion que recibe una cadena de texto como parámetro, 
la cual se convierte en minúsculas con el método *toLowerCase()* y se eliminan todos los espacios (En caso de haberlos)
con el método *replaceAll(' ', '')* luego se convierte esta cadena a un Array mediante el método *split('')*, se invierte según
el orden de sus entradas con el método *reverse()* y luego se convierte nuevamente este Array a un String el cual se compara con 
el String que se pasa como argumento de la función, si son iguales la función retorna **True**, en caso contrario retorna **False**.

Este archivo esta disponible en la ruta 'src/Prueba Técnica/palindrome.js'


**2. Función para filtrar mayores de 18 años en orden alfabético** 

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/88351677-6c16-44e1-b360-8c9783b9d320)

Para realizar la función requerida se plantea primero filtrar y almacenar en una constante los objetos que cumplan la condición
de edad igual o superior a 18, para esto se utiliza el método *filter(person => person.edad >= 18)*, a este array obtenido se le 
aplica la el método *sort()* con la intención de ordenar sus entradas bajo la propiedad name, este procedimiento garantiza el
filtrado por edad y el ordenamiento alfabético de la lista inicial.

Este archivo esta disponible en la ruta 'src/Prueba Técnica/OrderAdult.js'


**3. Función para determinar Fizz, Buzz o FizzBuzz**

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/98103d7c-9214-4279-8349-7a0d8db25e33)

Para lograr el objetivo de esta función se plantea tomar un número como parámetro y verificar si es divisible por 3, 5 y/o 15
(15 significa también ser divisible por 3 y 5 al mismo tiempo) esto se realiza mediante el residuo de la división que provee
JavaScript con el método *%*, se realizan múltiples condicionales con los casos anterior mencionados en el orden indicado en la
imagen en caso de entrar a algunos condicionales retornará los Strings (Fizz, Buzz, FizzBuzz), o en caso de no cumplir ninguno retornará
el argumento de la función transformado a String.

Este archivo esta disponible en la ruta 'src/Prueba Técnica/FizzBuzz.js'


### Ejercicios de interfaz de usuario en React

La aplicación se inicializó con Vite y Tailwind en el template de React para facilitar el uso de los estilos mediante clases,
se realizó una estructuración de carpetas entre componentes, contenedores y contexto:

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/e54a6946-ec2b-40c7-9ce1-b20e2c55dba0)

**Contenedor App**

Es el contenedor principal de nuestra aplicación encargado de renderizar todos los componentes presentes en el, además también almacena
los demás componentes dentro del *Provider* creado mediante *createContext*

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/69236c94-034d-42ae-b259-18adc8edd8a4)

**Contexto global de la aplicación (ApplicationContext)**

Contiene la información de los estados que se transmiten entre los componentes, para actualizar el estado de una manera más eficiente
además de que también contiene la información inicial de la tabla que se renderiza a traves del componente ApplicationList

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/199d7c74-336a-4ed7-b2b1-a8d9a89e32b7)

**Componente ApplicationCard**

Es un componente utilizado para maquetar una de las filas de la aplicación contiene el template base para dicha fila, en el se
almacena un método asociado al ícono de *Trash* encargado de eliminar una fila de la lista mediante la actualización del estado 
global de la aplicación.

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/3dcf4549-ec3b-4439-a56d-5bbc26cdbead)

**Componente Setter**

Es un componente que tiene en su interior un formulario que toma sus valores y mediante un botón de tipo submit ejecuta una función 
que permite añadir nuevos elementos correspondientes a filas al estado global de la aplicación, que se renderiza dando una vista al 
usuario de añadir una nueva entrada (fila) también renderiza un mensaje de alerta cuando se realiza submit sin haber completado todos
los campos.

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/445b4575-8de8-4b2d-908d-4aad5c9fc6e7)

**Componente TableHeader**

Es un componente Stateless que se encarga de aportar a la interfaz sirve para indicar el encabezado de la tabla 

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/9481b0b8-ed4b-4552-8d1f-5fdab6942177)

**Contenedor ApplicationList**

Es un contenedor el cual renderiza un componente ApplicationCard segun la cantidad de elementos presentes en el estado global
(context.state) y les pasa mediante props, el nombre, id, key, categoría y el contexto para que puedan ser utilizadas dentro
del componente hijo.

![image](https://github.com/Alejou343/PruebaTecnicaCPocket/assets/115825608/002de233-2eb5-4835-80c1-c5b7de9fb857)

Todos los elementos anterior mencionados dan lugar a una aplicación con una interfaz que permite crear una tabla con el nombre de
una red social (ingresada por teclado) y una categoría seleccionada mediante un menú desplegable con algunas opciones, que posee 
un boton para añadir un elemento a la tabla y esta tabla tiene un ícono que permite la eliminación de cualquiera de sus entradas
Se destaca una buena interfaz de usuario y una buena experiencia para el usuario. 








 







