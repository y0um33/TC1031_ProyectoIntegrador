# EVIDENCIA 1 PROYECTO INTEGRADOR (TC1031)
Este proyecto es una dulcería. Cada dulce tendrá un constructor por defecto con los siguientes atributos: Nombre del producto, Origen y Calorías. El cliente podrá ver todos los productos disponibles en la dulcería y organizar los productos en el orden de menor a mayor cantidad de calorías. El vendedor podrá agregar nuevos dulces y consultar la lista de productos.

## SICT0301: Evalúa los componentes
### Análisis de coplejidad correcto y completo para los algoritmos de ordeamiento usandos en el programa
- Ordenamiento por caloría -> ordenamiento por mezcla (Merge Sort): complejidad temporal peor caso O(n log(n)) y complejidad espacial peor caso O(n)

### Análisis de complejidad correcto y completo todas las estructuras de datos y cada uno de sus usos en el programa
- Vector de los dulces: complejidad tempeoral peor caso para acceso O(1) e inserción al final O(1) y complejidad espacial peor caso O(n).
- Lista doblemente encadenada: complejidad temporal peor caso para acceso O(n) e inserción O(1) y eliminación O(1) y complejidad espacial peor caso O(n).

### Análisis de complejidad correcto y completo para todos los demás componentes del programa y determina la complejidad final del programa
**Lista de empleados** 
- Lista doblemente encadenada: Inserción: O(1) y Eliminación: O(1)

**Vector de dulces**
- Acceso a datos: muestra_dulce O(1) va leer los objetos en el vector
- Inserción en datos: agrega_dulce, crea_dulce O(n) va agregar dulces en el vector

**Ordenamiento de dulces**
- Por mezcla: O(n log(n))
- _copyArray: para crear copia del vector para realizar la división y mezcla._
- _mergeSplit: se divide en mitad low to mid y mid+1 a high_
- _mergeArray: cuando ya no se puede dividir, se empiezan a juntar_
- _mergeSort: modifica_

## SICT0302: Toma decisiones
### Selecciona un algoritmo de ordenamiento adecuado al problema
El algoritmo de ordenamiento utilizado en este programa es el ordenamiento por mezcla, que se emplea para ordenar las calorías de los dulces en orden numérico ascendente. El ordenamiento por mezcla tiene una complejidad temporal en el peor caso de O(n log(n)) y una complejidad espacial en el peor caso de O(n). Por lo tanto, se puede concluir que, comparado con otros algoritmos de ordenamiento que tienen un peor rendimiento en el peor caso, el ordenamiento por mezcla es muy eficiente y rápido para este programa.

### Selecciona una estructura de datos adecuada al problema
En este programa se utilizaron dos estructuras de datos: el vector y la lista doblemente enlazada. Para realizar el algoritmo de ordenamiento, se generó un vector que guarda los objetos (dulces). La lista doblemente enlazada se utilizó para insertar y eliminar objetos (empleados). El problema implica la inserción (agregar dulces) y eliminación de objetos (eliminar dulces), y la lista doblemente enlazada tiene un mejor caso de O(1) para la inserción y eliminación, y O(n) para el acceso. Por lo tanto, comparada con otras estructuras, es la más eficiente y rápida.

## SICT0303: Implementa acciones científicas
### Implementa mecanismos para consultar información de las estructras correctos
Para consultar los dulces en el menú ingresas _opción 1_ y para ordenar por mezcla ingresas otra vez el número _1_. Y para agregar dulces, en el menú inicio ingresas _opción 2_ e ingresas número _1_. Para agregar empleados, en ese _opción 2_ ingresar número _2_ y finalment para poder eliminar los empleados, en ese _opción 2_ ingresar número _3_.
### Implementa mecanismos de lectura de archivos para cargar datos a las estructuras de manera correcta
Las dulces están registradas en el archivo _dulces.csv_. Y con la función _muestra_datos_ puede cargar datos.

### Implementa mecanismos de escritura de archivos para guardar los datos de las estructuras de manera correcta
A través de la función _agrega_dulces_ el usuario (staff) puede guardar los datos en el archivo _dulces.csv_. 

## Correciones
Avance 1: El algoritmo de ordenamiento que implementé no fue adecuado para mi código (Ordenamiento de Burbuja), así que lo cambié a ordenamiento por mezcla. Además, en lugar de guardar los objetos en un arreglo, cambié a un vector (para almacenar objetos de tipo Dulce) y añadí una estructura de lista doblemente enlazada (para guardar objetos de tipo Empleado).

Avance 2: Al ingresar una opción en el menú principal, si el usuario introducía un valor no numérico (letras), el programa se crasheaba. Para evitar esto, agregué un else if de _cin.fail()_ para que el código no se crashee aunque el usuario ingrese un valor que genere un error.

Avance 3:
