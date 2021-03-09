# 2-Scala
1. [Funciones](#schema1)
2. [Simplificación de funciones](#schema2)
3. [Funciones lambda](#schema3)
<hr>

<a name="schema1"></a>

# 1. Funciones
~~~scala
def obtenerCubo(x:Int): Int ={
    return x*x*x
}
val resultadoCubo = obtenerCubo(3)
println(s"El resultado del cubo es: ${resultadoCubo}")
~~~
![scala](./images/001.png)


<hr>

<a name="schema2"></a>

# 2.  Simplificación de funciones
1º No ponemos el tipo de retorno porque se infiere, en scala no se puede inferir los datos de entrada pero si los de salida
2º Se omite el bloque de código.

~~~scala
def obtenerCubo2(x:Int) =  x*x*x
val resultadoCubo2 = obtenerCubo2(3)
println(s"El resultado del cubo es: ${resultadoCubo2}")
~~~
![scala](./images/002.png)

<hr>

<a name="schema3"></a>


# 3. Funciones lambda
Una función lambda puede recibir como parámetro otra función y puede devolver otro función

~~~scala
def sumar(f:Int => Int)={
    f(3) //se puede poner el return o no.
}
sumar(obtenerCubo2)
~~~
![scala](./images/003.png)