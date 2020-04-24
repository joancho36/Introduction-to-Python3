# Ejercicios

2. Lea el año de nacimiento de un utilizador y diga cuantos años tiene


```python
#Colocar siempre la fecha de nacimiento (fecha_nac) como date(fecha_nac) con el orden Año,mes,día
from datetime import date
from datetime import time
def cal_edad(fecha_nac):
    diferencia_fech= date.today() - fecha_nac
    diferencia_fech_dias= diferencia_fech.days
    edad_numerica= diferencia_fech_dias/365
    edad= int(edad_numerica)
    return edad
fecha_nac=date(2001 ,7 ,20)
print(cal_edad(fecha_nac))

```

    18
    

3.Lea una palabra y transformela a su inversa, que se lea de atras para al frente 


```python
def inverse_word(word):
    a=word[::-1]
    return print(a)
inverse_word("joan dos santos")
```

    sotnas sod naoj
    

4.Lea un número y diga si es entero. O real. Positivo, negativo o cero. Diga si es impar o es Par, en caso de ser decimal diga "numero invalido".


```python
#Para numeros enteros
def tipo_numero(n):
    a=n
    if type(a)==int:
        print("n es entero")
    else:
        print("n no es entero")
    return
tipo_numero(2.2)
tipo_numero(2)
```

    n no es entero
    n es entero
    


```python
#Para numeros reales
def tipo_numero_R(s):
    if type(s)==complex:
        print("s no es real")
    else:
        print("s es real")
    return
tipo_numero_R(2)
tipo_numero_R(1j)
```

    s es real
    s no es real
    


```python
#Si es par o ímpar
def par_impar(t):
    if t%2==0:
        print("t es par")
    elif t%3==0:
        print("t es ímpar")
    else:
        print("Número invalido, coloque un número entero")
    return
par_impar(2)
par_impar(3)
par_impar(2.2)
```

    t es par
    t es ímpar
    Número invalido, coloque un número entero
    

5. Lea el nombre de un usuario, y si el nombre contiene espacio diga "invalido"


```python
import re
def name_user(u):
    s=u
    checar=re.findall(r" ",s)
    i=len(checar)
    if i==0:
        print("Válido")
    else:
        print("invalido")
    return
name_user("joan")
```

    Válido
    
