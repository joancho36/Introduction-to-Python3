Primer notebook

# Breve introducción a Python

Con ayuda de https://www.youtube.com/channel/UCLEQMN2aaUD9VfBVPxG0IOg

#  Contenido

1- Operadores
2-Variables
3-Strings
4-Conversión de tipos
5- Más recursos del print
6- Tipo Boolean
7-Operadores logicos
8-Estructuras con if, elif y else
9-Operadores de atribuición y while
10-Repetición for
11-Función Range
12-Programas genricos usando input
13-Introducción a funciones
14-Trabajar con fechas y horas.

# Comentarios


```python
# ver que sucede
a = "hola "
b = "Mundo"
print(a + b)
```

    hola Mundo
    

# 1 Operadores
+ = suma
- = resta
/ = división
** = exponente
// = parte entera de la división
% = resto de la división

```python
# suma
2+2
```




    4




```python
#resta
1-2
```




    -1




```python
#Multiplicación
2*2
```




    4




```python
#División
4/2
```




    2.0




```python
#exponencial
2**2
```




    4




```python
#Parte entera de la división
11//2
```




    5




```python
# resto de la división
4%2
```




    0



# 2 Variables
Guardan refetencias para objetos

```python
a=1
b=2
a+b
```




    3




```python
c=2
b=-1
c,b
```




    (2, -1)




```python
r,s= 2,9
r
```




    2



# 2-1Tipos de variables

int=numero entero (1, 2, 3)
complex=numero complejo(1j, 1+1j, -2j) NUNCA DEJAR j SOLO, DARA ERROR
float= numero decimal (2.2, 3.1, 1.0)
str=palabra, string.


```python
#Padrones numericos:
a= 7.4 + 3
print (a)
print (type(a))
#type se refiere al tipo de numero que es a (float = decimal)
```

    10.4
    <class 'float'>
    


```python
b = 2+2
print(b)
print(type(b))
# int=entero
```

    4
    <class 'int'>
    


```python
c="Joan"
print(type(c))
# str=string
```

    <class 'str'>
    


```python
s= 4+2j
print(type(s))
#j=unidad imaginaria,complex=complejo
```

    <class 'complex'>
    


```python
e=True
print(type(e))
#bool= clases de numeros de verdadero o falso, 1= true, 0= false
```

    <class 'bool'>
    

Programa calcular aumento de salario


```python
# sal= salario, aum=aumento, n_sal=nuevo salario
sal= 2000
aum=5
n_sal= sal + (sal*(aum/100))
print(n_sal)
```

    2100.0
    

# 2-2Notación cientifica
notação: (n)e(expoente), onde n é o numero e expoente é a potencia de e=10

```python
#exm:
1.13e10
```




    11300000000.0



# 2-3 Operadores Relacionales


```python
a=1
b=5
c=2
d=1
```


```python
a==b #a es igual b?
```




    False




```python
a<b #a es menor que b?
```




    True




```python
a>b #a es mayor que b?
```




    False




```python
c<=b # c es menor o igual a b?
```




    True




```python
c>=d #c es mayor o igual a d?
```




    True




```python
c!=b #c es diferente de b?
```




    True



# 3 Strings
Un string es un conjunto ordenado de caracteres (palabras, textos, etc)

```python
"Soy un string"
```




    'Soy un string'



# 3-1 Variables y operaciones aritmeticas


```python
var= "Hola señorita"
var
```




    'Hola señorita'




```python
"quiero"+" helado"
```




    'quiero helado'




```python
"hola"+ 10
```


    ---------------------------------------------------------------------------

    TypeError                                 Traceback (most recent call last)

    <ipython-input-99-cc467acb0736> in <module>
    ----> 1 "hola"+ 10
    

    TypeError: can only concatenate str (not "int") to str

no se pueden suma o restar letra y numeros con strings

```python
"a"*2
```




    'aa'



# 3-2 Tamaño e indexión de un String
len("string") función para saber el tamaño (numero de letras) de un string

```python
len("banana")
```




    6


Podemos dar un "zoom" en un string 

```python
s="luna"
s[0]
```




    'l'




```python
s[1]
```




    'u'



  s--4 s--3  s--2   s--1
# L    u    n    a
  s-0   s-1   s-2   s-3

# 3-3 Slice de strings
Muchas veces no queremos ver una string toda, solo parte de ella. 

1- Primera forma de hacer slice: "zoom"

2- Segunda forma: Sea S la stringm y A y B numeros enteros, S[A:B] representa el cuerpo del string en el intervalo [A:B]
NOTA: EL INICIO DE UN STRING ES SIEMPRE CERO

3- Tercera forma: S[A:B:C]  
A=inicio del intervalo
B=final del intervalo
C=pasos saltados dentro del intervalo

```python
#Ejemplos:
S="buenos dias"
S[0:6]
```




    'buenos'




```python
S[0:6:2]
```




    'beo'




```python
S[::-1]
#Tomamos toda la palabra, solo que invertida 
```




    'said soneub'



# 3.4 Comparación de Strings


```python
"abc"=="abc"
```




    True




```python
"Abc"=="abc"
```




    False



Función ord("string") convierte un caracter en un numero,su inversa es chr.


```python
ord("1")
```




    49




```python
ord("a")
```




    97




```python
"a">"1"
#porque "a"=97 y "1"=49
```




    True




```python
chr(97)
```




    'a'



# 4 Conversión de tipos 
Pasar a escribir un caracter en otro tipo de carater, por ejemplom pasar de decimal (floar) a entero (int)

```python
int(2.9)
```




    2




```python
float(2)
```




    2.0




```python
str("49")
```




    '49'



# 5 Más recursos del print


```python
print("quiero un final", end =" feliz")
```

    quiero un final feliz


```python
print("salta")
print("la valla")
```

    salta
    la valla
    


```python
print(1,1,1, sep="a")
#sep=coloca un caracter en lugar de comas
```

    1a1a1
    


```python
dia=20
mes=7
año=2001
print(dia, mes, año, sep="/")
```

    20/7/2001
    

# 6 Tipo Boolean
El tipo boolean solo admite dos operadores lógicos: Verdadero (True) y falso (False)

```python
boolVer=True
boolVer
```




    True




```python
boolVer=False
boolVer
```




    False



# 7 Operadores Logicos
Extisten tres tipos de operadores logicos (Booleano) en python:
-and
-or
-not
#  7.1 Operador and
and opera entre dos valores, quedando en medio de estos dos. 
Su retorno será True si los dos valores son True, contrario su retorno será False

```python
True and True
```




    True




```python
True and False
```




    False




```python
4 == 2**2 and 9 == 81**0.5
```




    True



# 7.2 Operador or
Opera sobre dos valores, devolviendo True si uno de los valores es verdadero

```python
True or False
```




    True




```python
False or False
```




    False




```python
2==2 or 3==8
```




    True



#  7.3 Operador not
not trabaja solo con un valor, invirtiendo su valor logico, o sea, convierte True en False y vice-versa.

```python
not False
```




    True




```python
not True
```




    False



# 8 Estructura de indectación, if, elif y else
Permiten que un codigo se adeque a situaciones previstas.
Por ejemplo: "Si" eso sucede, ejecute este codigo, "y sino", ejecute este.
En python, "Si"= if y "y sino"= (elif, else)
# 8.1 Desición con if
if implementa una condición

```python
n = 10
if n == 10:
    print("entrar")
```

    entrar
    


```python
if str(n)=="10":
    print("entrar")

```

    entrar
    


```python
if n != 11 or n > 14 or n < 10:
    print("entrar!")
```

    entrar!
    

# 8.2 elif
Cuando la condición if no es satisfecha, entonces no será ejectuda, por lo que el programa sigue en frente para ejecutar una condición a seguir. Esa siguiente condición se llama con el comando elif.

```python
n = 2
if n < 1:
    print("n < 1")
elif n==2:
    print ("n=2")
```

    n=2
    
Podemos usar todos los elif que necesitemos.
Si usamso dos if, ellos son independientes, o sea, pueden ejecutar dos codigos caso los dos sean verdaderos, a diferencia de elif, que solo ejetuca uno solo.

```python
n=13
if n == 2*2:
    print ("hola")
elif n == 3:
    print("bienvenido")
elif n < 20:
    print("Buen dia")
```

    Buen dia
    

# 8.3 else
Sirve para ejcutar un codigo cuando el mismo no satisface ni if ni elif

```python
n=0
if n==1:
    print("n=1")
elif n == 2:
    print("n=2")
elif n==3:
    print("n=3")
else:
    print("n no es ni 1, 2 ni 3")
```

    n no es ni 1, 2 ni 3
    
En situaciones Binarias, donde solo queremos saber si o no, usamos unicamente if y else, una vez que elif sirve como "recurso" caso el no se ejecute la condicion impuesta por if

```python
n =-3
if n > 0:
    print("n>0")
else:
    print("n es negativo")
```

    n es negativo
    

# 8.4 if dentro de if


```python
edad=25
sexo="f"
if edad>21:
    if sexo =="f":
        print ("Bienvenida!")
    else:
        print("Bienvenido")
#Nota: else y elif estan ligados al if más proximo de ellos por arriba.
```

    Bienvenida!
    

# 8.5 Indectación 


```python
if 1==1:
    print("1==1")
```

    1==1
    
Nota que print, debajo de if, tiene un espacio. Ese espacio el la indectación y significa que ese print está dentro de la estructura del if, osea, si if se cumplen, entonces print se ejecuta.
# 9. Operadores de atribuición
Usando repeticiones, es comun cambiar el valor de la variables

```python
n=10
n=n+1
n
```




    11


podemos simplicifar de la siguiente manera:

```python
n=10
n +=1
n
```




    11




```python
n=4
n /=2
int(n)
```




    2




```python
n=4
n -=3
n
```




    1



# 9.1 Repetición con while
While es usado para ejecutar una intrucción siempre que una condición sea satisfecha

```python
n=0
while n < 4:
    print(n)
    n += 1
```

    0
    1
    2
    3
    
CUIDADO: Si la condición es siempre vedadera, por ejemplo: while 1 < 2, print ("a"), "a" será ejecutado infinitamente 
# 9.2 Condiciones más complejas


```python
n=0
while 1!=2 and  n <=3:
    print(n, end =" ")
    n+=1
```

    0 1 2 3 


```python
#Inecuaciones
n=0
while n < 3 < 5:
    print(n, end=" ")
    n+=1
```

    0 1 2 

# 9.3 Comando Break
El comando break sirve para quebrar las repeticiones del comando while, quebrando todo lo que este por debajo de break

```python
n=10
while n>0:
    if n==15:
        break
    print(n, end=" ")
    n+=1
print("Salio de while en n=", n)
```

    10 11 12 13 14 Salio de while en n= 15
    

# 9.4 Comando continue
Su funcuión es ignorar todo lo que este por debajo de él, pero vuelve a la condición inicial y sigue ejecutando, retoma su trabajo y no para a diferencia de break

```python
n=0
while n < 5:
    n+=1
    if n==3:
        continue
    print(n, end=" ")
```

    1 2 4 5 
Cuando if es satisfecho, continue es ejecutado por lo que salta n==3 y vuelve a retomar while.
# 9.5 Else 


```python
n=1
while n < 0:
    print(n, end=" ")
    n+=1
else:
    print("no entró en while")
```

    no entró en while
    


```python
n=-1
while n < 0:
    print( "n< 0")
    n+=1
else:
    print("Salió de while porque n no es menor que cero")
```

    n< 0
    Salió de while porque n no es menor que cero
    

# 10 Repetición con for
Sintaxis del for:
for "variable" in "iterable", donde un iterable es cualquier objeto con un orden especifico para acceder a sus elementos.
Un string es un ejemplo  de un iterable .
Además del iterable es necesaria una variable, en cada ejecució de for, esa variable recibirá el valor del elemento actual.
# Ejemplos iniciales


```python
s="abcd"
for i in s:
    print("el iterador esta en", i)
```

    el iterador esta en a
    el iterador esta en b
    el iterador esta en c
    el iterador esta en d
    

# 10.1 Ejemplos con listas
Una lista es un conjunto de elementos. Las listas son iterables.

```python
L= [1, 2, 4, 4]
L
```




    [1, 2, 4, 4]




```python
L= [1, "a", 3.2, 7]
L
```




    [1, 'a', 3.2, 7]




```python
L=[1,2,3,4]
for i in L:
    print("el iterable está en", i)
```

    el iterable está en 1
    el iterable está en 2
    el iterable está en 3
    el iterable está en 4
    

# 10.2 Break, continue y else con for y listas
Así como while, for tambien acepta el uso de break, else,if y elif.

```python
L=[1,2,3,4]
for i in L:
    if i==3:
        break
    print("el iterdador está en", i)
    
```

    el iterdador está en 1
    el iterdador está en 2
    


```python
L=[1,2,3,4]
for i in L:
    if i==3:
        continue
    print("el iterador está en", i)
```

    el iterador está en 1
    el iterador está en 2
    el iterador está en 4
    


```python
L=[1,2,3,4]
for i in L:
    print("el iterador está en", i)
else:
    print("el iterdaor salió de la lista")
```

    el iterador está en 1
    el iterador está en 2
    el iterador está en 3
    el iterador está en 4
    el iterdaor salió de la lista
    

# 10.3 Más ejemplos


```python
#Diferenciar vocales de consonantes en el alfabeto:
for letra in "abcdefghijklmnñopqrstuvwxyz":
    print(letra,end=" es una ")
    if letra in "aeiou":
        print("vocal")
    else:
        print("consonante")
```

    a es una vocal
    b es una consonante
    c es una consonante
    d es una consonante
    e es una vocal
    f es una consonante
    g es una consonante
    h es una consonante
    i es una vocal
    j es una consonante
    k es una consonante
    l es una consonante
    m es una consonante
    n es una consonante
    ñ es una consonante
    o es una vocal
    p es una consonante
    q es una consonante
    r es una consonante
    s es una consonante
    t es una consonante
    u es una vocal
    v es una consonante
    w es una consonante
    x es una consonante
    y es una consonante
    z es una consonante
    


```python
#Diferenciar números pares de impares
N=[1,2,3,4]
for i in N:
        if i%2 == 0:
            print(i, " es par ")
        else:
            print(i,  " es impar ")
```

    1  es impar 
    2  es par 
    3  es impar 
    4  es par 
    

# 11 Función Range
La función range sirve para entregar secuencias de números enteros.
La función de evoca de tres maneras:

1) range("fin")
2) range("inicio","fin")
3) range("inicio","fin","paso")
# 11.1 Range y primera forma


```python
range(10)
```




    range(0, 10)




```python
list(range(10))
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
for i in range(10):
    print(i,end=" ")
```

    0 1 2 3 4 5 6 7 8 9 

# 11.2 Range y segunda forma

Podemos definir un inicio y un fin


```python
range(1,10)
```




    range(1, 10)




```python
list(range(1,10))
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
list(range(-3,4))
```




    [-3, -2, -1, 0, 1, 2, 3]



# 11.3 Range y tercera forma

Podemos definir un inicio, un fin, y todavía saltar números. Aqui el nuevo parametro son los pasos.


```python
list(range(0,9,2))
```




    [0, 2, 4, 6, 8]




```python
list(range(2,11,3))
```




    [2, 5, 8]




```python
list(range(5,0,-1))
```




    [5, 4, 3, 2, 1]



# 11.4 Casos de Range + for
Tomar los numeros pares de 2 hasta 10

```python
for i in range(0,11,2):
    print(i,"es par")
```

    0 es par
    2 es par
    4 es par
    6 es par
    8 es par
    10 es par
    
Tomar los numeros multiplos de 3 en 3 hasta 21

```python
for i in range(3,22,3):
    print(i, "es multiplo de 3")
```

    3 es multiplo de 3
    6 es multiplo de 3
    9 es multiplo de 3
    12 es multiplo de 3
    15 es multiplo de 3
    18 es multiplo de 3
    21 es multiplo de 3
    

# 12 Programas genericos usando input


```python
#Ejemplo:

nombre, edad = "Joan", 19
print(nombre, " tiene ", edad, " años")
#Apesar de que el código funciona, no es generico, porque si cambiamos de lugar nombre y edad tenemos que cambiar el programa.
```

    Joan  tiene  19  años
    

# 12.1 Función input

input (que significa entrada) será la función responsable por la entrada de informción en nuestro programa.


```python
#Ejemplos:
input()
```

    hola
    




    'hola'




```python
input()
```

    66
    




    '66'


Notamos que la función input nos devuelve siempre un String
# 12.1 Pasando para variables


```python
x=input()
y=input()
print("entrada en x:",x)
print("entrada en y:",y)
```

    1
    2
    entrada en x: 1
    entrada en y: 2
    


```python
x,y = input(), input()
print("entrada en x:",x)
print("entrada en y:",y)
```

    1
    2
    entrada en x: 1
    entrada en y: 2
    

# 12.2 Convirtiendo tipos

Como vimos, input convierte la entrada para str.
Pero no siempre queremos trabajar con strings, asi que recorremos a los comandos int y float.


```python
n=int(input())
n
```

    61
    




    61



# 12.3 Resolviendo el problema inicial sobre programas genericos


```python
nombre, edad= input(),int(input())
print(nombre, "tiene", edad, "años")
```

    Joan
    19
    Joan tiene 19 años
    

#  13 Introducción a funciones

Las funciones son partes de un código que pueden ser ejecutados en cualquier parte de un programa. Sus principales utilidades son las de: 1) Permiten reutilizar un codigo 2) Dejan el codigo más legible y 3) facilitan la busqueda de errores en un programa (depuración).

# 13.1 Funciones sin parametros

Para crear funciones usamos la siguiente estructura: def "nombre_de_la_fución"(parametro 1,...): código


```python
def mensaje():
    print("Hola humano")
```


```python
#tenemos que invocar a la funcion por su nombre
mensaje()
```

    Hola humano
    

# 13.2 Funciones con parametros


```python
def nombre_de_usuario(nombre):
    print("nombre de usuario:", nombre)
```


```python
nombre_de_usuario("Joan")
nombre_de_usuario(36)
```

    nombre de usuario: Joan
    nombre de usuario: 36
    

# 13.3 Funciones con return

La mayoria de la funciones tienen una entrada (parametro) y una salida (return). Return es el resultado de la función.


```python
#Función suma:
def suma(B, C):
    return B + C
```


```python
suma(2, 2)
```




    4




```python
suma("ho", "la")
```




    'hola'


NOTA: La función será interrumpida despues de return, o sea, no es ejecutado todo lo que este por debajo de return dentro de la función

```python
def f():
    for i in range(0,10):
        if i>3:
            return
        print("a")
```


```python
f()
#Esto muestra que apartir de i>3, entre en return y se dejó de ejecutar el print
```

    a
    a
    a
    a
    

# 14 Trabajar con fechas y horas

Usaremos "import", el cual sirve para invocar modulos o submodulos, por ejemplo "time" o "datetime" de fecha y horas.
Tambien le daremos uso al comando str(f o p)(), donde "strf()" sirve para sacar una parte de la información de una variable y "strp()" sirve para pasar de strings a numeros y vice-versa

# 14.1 datetime


```python
#Ejemplo: Leer el mes
import datetime
mifecha=datetime.datetime.now()
print(mifecha.strftime("%B"))
```

    April
    


```python
import datetime
ahora=datetime.datetime.now()
#Podemos separar mes, dia, hora, mintuo, etc...
print(ahora)
print(ahora.minute)
print(ahora.hour)
print(ahora.day)
print(ahora.month)
```

    2020-04-22 12:22:18.741977
    22
    12
    22
    4
    

# 14.2 Date


```python
#Ejemplo: 
#1) Leer mes, dia y fecha
import time
print(time.strftime("%d/%m/%Y"))
#2) Leer horas:
#2.1) Formato 24h:
print(time.strftime("2.1)%H:%M:%S"))
#2.2 Formato 12h:
print(time.strftime("2.2)%I:%M:%S"))
```

    22/04/2020
    2.1)13:53:07
    2.2)01:53:07
    

# 14.3 Almacenar la variable tiempo


```python
import time
tiempo= time.strftime("%H:%M:%S")
tiempo
```




    '12:01:08'




```python
import time
fecha=time.strftime("%d/%m/%Y")
fecha
```




    '22/04/2020'



# 14.4 Uso del strp

Situaciones en que tenemos la fecha en formato string y queremos pasarla a formato de fecha


```python
import datetime
fecha="20/07/2001"
fecha= datetime.datetime.strptime(fecha,"%d/%m/%Y")
print(fecha)
```

    2001-07-20 00:00:00
    


```python
import datetime
fecha = "20 August 2016"
#Para pasar la fecha de arriba a un formato de fecha recorremos a strp:
y = datetime.datetime.strptime(fecha,"%d %B %Y")
print(y)
```

    2016-08-20 00:00:00
    
NOTA: cuidado con el orden de las variables y en como las hace corresponder strptime!
      note que "20 August 2016" está exactamente "alineado" con "%d %B %Y". Si hubieramos escrito "20 August- 2016" tendriamos
      que reescribir "%d %B- %Y"
#  14.5 Operaciones sobre fechas
Ahora, ademas de trabajar con el modulo "import" usaremos el "from" que se usa para reticar un submodulo en especifico mediante la siguiente formula:

import datetime
from datetime import date    O sea, usar las fechas (año, mes, dia) de datetime

NOTA: Cuando date es invocado, debemos respetar su orden (%Y(años) %m (mes) %d(dia))

```python
#Ejemplo: Calcular mi edad
from datetime import time
def calcular_edad(fecha_nac):
    diferencia_fechas= date.today() - fecha_nac
    diferencia_fechas_dias= diferencia_fechas.days
    edad_numerica= diferencia_fechas_dias/365.2425
    edad= int(edad_numerica)
    return edad
fecha_nac= date(2001 ,7 , 20)
print(calcular_edad(fecha_nac))
```

    18
    
