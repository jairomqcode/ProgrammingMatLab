# Comandos en MatLab.
## Comentarios en MatLab.

Los **comentarios en MATLAB** se utilizan para explicar el código y hacerlo más legible. Pueden ayudar a otros a entender el código, incluso si no están familiarizados con MATLAB. También pueden ayudar al autor del código a recordar lo que hace el código.  

Los comentarios en MATLAB se pueden escribir usando el **símbolo de porcentaje (%)**. Cualquier texto que siga a un símbolo de porcentaje en una línea se considera un comentario y no se ejecutará. Por ejemplo:  

```MatLab
% Este es un comentario
```

Los comentarios también se pueden escribir en varias líneas usando los operadores de comentario en bloque, %{ y %}. Cualquier texto entre los operadores de comentario en bloque se considerará un comentario. Por ejemplo:

```MatLab
%{
Este es un comentario en varias líneas.
Puede ser tan largo como sea necesario.
}%
```

Los comentarios son una parte importante de la programación en MATLAB. Ayudan a que el código sea más legible y fácil de entender. Aquí hay algunos consejos para escribir comentarios de MATLAB:  
- Sea claro y conciso.  
- Use palabras y frases que sean fáciles de entender.  
- No asuma que el lector sabe lo que está haciendo el código.  
- Actualice los comentarios a medida que cambie el código.  

Escribir comentarios de MATLAB puede parecer una tarea adicional, pero vale la pena el esfuerzo. Los comentarios pueden ayudar a que su código sea más legible y fácil de entender, lo que puede ahorrarle tiempo y frustraciones en el futuro.

## Variables en MatLab.  
En MATLAB, una **variable** es una ubicación con nombre en la memoria que **almacena un valor**. Las variables se pueden usar para almacenar cualquier tipo de datos, incluidos números, cadenas, caracteres y matrices.  

Para crear una variable en MATLAB, se debe asignar un valor. El signo (=) en MatLab es el **operador de asignación**, lo que significa que la expresión a la derecha del signo igual se asigna a la variable de la izquierda.

```MatLab
x = 7    % x es la variable y 7 es el valor.
```

Otro ejemplo:  
```MatLab
y = 3 + 4
% MatLab primero evalua la expresión 3 + 4, y luego el resultado "7" se lo asigna a la variable y.
```
Es importante destacar que si se agrega un punto y coma al final de un comando, se suprime la salida, aunque el comando seguirá ejecutándose. Cuando se introduce un comando sin punto y como al final, MatLab muestra el resultado en la línea de comandos.  

## Almacenamiento y carga de variables.  

Las variables se pueden guardar en un espacio de trabajo en un formato de archivo especifico de MatLab, llamado archivo MAT, usando el comando save.

```MatLab
save datafile.mat
```
Se puede observar el contenido de cualquier variable introduciendo su nombre. También, podemos utilizar la función **clear** para vaciar el espacio de trabajo. Por otro lado, podemos utilizar la función o comando **load** para cargar las variables de un archivo MAT.  

```MatLab
load datafile.mat
```
Finalmente, se usa la función **clc** para vaciar la ventana de comandos.

## Uso de constantes y funciones incorporadas.  

MatLab contiene constantes incorporadas, una de ellas es **pi** para representar π.
```MatLab
a = pi
Sol: 3.1416  
```


MatLab contiene una amplia variedad de funciones, como **abs** (valor absoluto) **eig** (cálculo de valores propios). MatLab utiliza paréntesis para pasar las entradas a las funciones, de forma similar a la notación matemática estándar.  

```MatLab
% Asignamos a una variable "y" el resultado de la función seno evaluada en x. 
y = sin(x)
```
```MatLab
% Asignamos a una variable "z" el resultado de la raíz cuadrada de -9.
z = sqrt(-9)
Sol: 0.0000 + 3.0000i
```

# Vectores y Matrices.    
Los arrays son el tipo de datos más fundamental en MATLAB. Son una colección de valores del mismo tipo, almacenados en ubicaciones de memoria contiguas. Las matrices pueden ser unidimensionales, bidimensionales, tridimensionales o incluso de dimensiones superiores.

Un solo número llamado escalar, es en realidad un arreglo de 1x1, lo que significa que contiene 1 fila y 1 columna. Por ejemplo:  
```MatLab
x = 4
```
Se pueden crear arrays con varios elementos utilizando corchetes.  
```MatLab
x = [7 9]
```
Sol:   
| row | col 1 | col 2 |
|:-:|:-:|:-:|
| 1 | 7 | 9 |

Cuando se separan los números con espacios o comas, MatLab combina los números en un vector fila, lo cual, es una matriz con una fila y varias columnas (1 por n). Cuando se separan los números mediante punto y coma, MatLab crea un vector columna (n por 1).  
```MatLab
x = [7; 9]
```
Sol:  
| Column |
|:-:|
|7|  
|9|  

Creamos un vector fila que contiene los valores 3, 10, 5:
```MatLab
x = [3, 10, 5]
```
Sol:  
| row | col 1 | col 2 | col 3 |
| :-: | :-: | :-: | :-:|
| 1 | 3 | 10 | 5 |  

Creamos un vector columna que contiene los valores 8, 2, -4:  
```MatLab
x = [8; 2; -4]
```
Sol: 
| Col |
| :-: |
| 8 |  
| 2 | 
| -4 |   

Podemos combinar espacios con punto y coma para crear una matriz, que es un arreglo con varias filas y columnas. Cuando se introduce una matriz, se debe introducir línea por línea.  
```MatLab
x = [5 6 7; 8 9 10]
```
Sol:  
| row | Col 1 | Col 2 | Col 3 |
| :-: | :-: | :-: | :-: | 
| 1 | 5 | 6 | 7 | 
| 2 | 8 | 9 | 10 |  

MatLab puede realizar cálculos entre los corchetes:  
```MatLab
x = [sqrt(10) pi^2]
```
Sol:  
| row | Col 1 | Col 2 |
| :-: | :-: | :-: |
| 1 | 3.1623 |  9.8696 |

También, podemos crear vectores uniformemente espaciados utilizando el operador : y especificar solo los puntos de inicio y fin.  

```MatLab
x = 1 : 4
```
Sol:  
x = 1  2  3  4  

El operador : utiliza un espacio predeterminado de 1, sin embargo, podemos especificar nuestro propio espacio de la siguiente manera:  

```MatLab
x = 1 : 0.5 : 3
```
Sol:  
x = 1.000  1.500  2.000  2.500  3.000  3.500  4.000  4.500  5.000  

Podemos generar un vector con un número de elementos deseados utilizando la función **linspace()**, su sintaxis es la siguiente:  

```MatLab
x = linspace(primero, último, número_de_elementos)
```

Tanto la función **linspace** y el operador : crean vectores fila. Sin embargo, se puede convertir un vector fila en un vector columna utilizando el operador de transposición (').

```MatLab
x = 1 : 3;
x = x'
```
Sol:  
X =  
1   
2  
3  

MatLab contiene funciones que ayudan a crear matrices de uso habitual, como matrices de números aleatorios, la sintaxis es rand(n):
```MatLab
x = rand(2)
```
Sol:  
| N. Fila | Col 1 | Col 2 |
|:-----:|:-----:|:-----:|
| 1 | 0.814 | 0.127 |  
| 2 | 0.905 | 0.913 | 

El 2 en el comando rand(2) especifica que la salida será una matriz de 2 por 2 de números aleatorios.  También, podemos utilizar la sintaxis rand(n,m) para crear matrices no cuadradas de números aleatorios.
```MatLab
x = rand(2,3)
```
Sol:  
| N. Fila | Col 1 | Col 2 | col 3 |
|:-----:|:-----:|:-----:| :-----: |
| 1 | 0.632 | 0.278 | 0.957 | 
| 2 | 0.097 | 0.546 | 0.964 |

Podemos utilizar la función zeros(n,m) para crear una matriz de n filas, m columnas y elementos ceros.

## Indexación y modeificación de arreglos.

