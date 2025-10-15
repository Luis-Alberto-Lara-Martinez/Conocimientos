# Apuntes básicos de Java
Aquí se muestran los conceptos y fragmentos de código más utilizados para realizar tareas comunes en Java.

## Tipos de datos básicos
```bash
// Enteros
int numEntero = 20;

// Decimales
double numDecimal = 4.20;

// Carácter único
// ⚠️ IMPORTANTE: el tipo char SIEMPRE usa comillas simples
char caracter = 'A';

// Booleano (verdadero o falso)
boolean estado = true;
```

## Tipos de datos avanzados
### String
Cadena de texto.
⚠️ SIEMPRE usa comillas simples.

```bash
String nombre = "Luis Alberto";
```

### Integer
Versión objeto del tipo primitivo int. Puede ser null y es usado en colecciones. Conversión automática entre int e Integer
⚠️ Si haces operaciones puede salir la excepción NullPointerException si alguno es null.

```bash
Integer a = 20;
Integer b = null;
```

### BigDecimal
Clase para operaciones numéricas con alta precisión (finanzas, cálculos exactos).

```bash
BigDecimal a = new BigDecimal("10.5");
BigDecimal b = new BigDecimal("2.3");

BigDecimal suma = a.add(b);                    // 12.8
BigDecimal resta = a.subtract(b);              // 8.2
BigDecimal mult = a.multiply(b);               // 24.15
BigDecimal div = a.divide(b, 2, RoundingMode.HALF_UP); // 4.57
BigDecimal divSinScale = a.divide(b); // 4.57

BigDecimal escalado = a.setScale(2, RoundingMode.HALF_UP)

Integer comparacion = a.compareTo(b); // 1 si a > b, 0 si son iguales, -1 si a < b
```
### Arrays
Almacena en una variable múltiples valores del mismo tipo

```bash
// Declaración
int[] numeros;
// Inicialización
numeros = new int[5];

// Declaración e inicialización simultánea
int[] numeros = {10, 20, 30, 40, 50}; 
String[] nombres = {"Ana", "Luis", "Marta"};


// Acceder a un elemento
System.out.println(numeros[0]); // 10

// Modificar un valor
numeros[2] = 99;

// Longitud del array
Integer longitud = numeros.length

// Recorrer un array con for
for (int i = 0; i < numeros.length; i++) {
    System.out.println(numeros[i]);
}

// Recorrer un array con for each
for (int n : numeros) {
    System.out.println(n);
}
```

### Listas
Son una colección dinámica que te permite almacenar varios elementos del mismo tipo, pero a diferencia de los arrays, pueden crecer o reducirse en tamaño fácilmente.
  #### Declaración e inicialización
```bash
List<String> nombres = new ArrayList<>();
```
  #### Declaración e inicialización
```bash
List<String> nombres = new ArrayList<>();
```


## Leer ficheros txt
## Escribir en ficheros txt
## Leer ficheros binarios
## Escribir en ficheros binarios
## Leer un fichero xml
## Escribir en un fichero xml
