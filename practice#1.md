#Practice 1
**Exercise 1**

//Develop a scala algorithm that calculates the radius of a circle
var pi=3.1416
var p=14.2563
var radio=(p/(2*pi))
////////////////////////////////////////////////
**Exercise 2**

//Develop an algorithm in scala that tells me if a number is prime
def isPrime2(i :Int) : Boolean = {
|     if (i <= 1)
|       false
|     else if (i == 2)
|       true
|     else
|       !(2 to (i-1)).exists(x => i % x == 0)
|   }
// isPrime2: (i: Int)Boolean
(1 to 10).foreach(i => if (isPrime2(i)) println("%d is prime.".format(i)))
////////////////////////////////////////////////
**Exercise 3**

//Given the variable bird = "tweet", use string interpolation to
// print "I'm writing a tweet"
var bird = "tweet"
string conexion "Estoy escribiendo un Twwet"
println("Estoy escribiendo un %s",bird)
///////////////////////////////////////////////

**Exercise 4**

/*Given the variable message = "Hello Luke, I am your father!" uses slilce to extract the
 sequence "Luke" */
var mensaje = "Hola Luke soy tu padre!"
mensaje.slice(5,9)
//////////////////////////////////////////////

**Exercise 5**

//What is the difference between value and a variable in scala?
//value (val) se le asigna un valor definido y no puede ser cambiado en cambio una variable (var) puede ser cambiada en cualquier momento.
//////////////////////////////////////////////

**Exercise 6**

//Given the tuple (2,4,5,1,2,3,3.1416,23) returns the number 3.1416
var x = (2,4,5,1,2,3,3.1416,23)

println(x._7)
