**Indications, to access the links choose the github symbol corresponding to the practice you want to view**

<br>
<a>
  practice#1
  <a href="https://github.com/pakito97/Big-Data-UNIDAD-1/blob/Development/practice%231.md">
  <img align="left" alt=" Github" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" />
</a>
</br>
<br>
<a>
  practice#3
  <a href="https://github.com/pakito97/Big-Data-UNIDAD-1/blob/Development/practice%233.md">
  <img align="left" alt=" Github" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" />
</a>
</br>
<br>
<a>
  practice#4
  <a href="https://github.com/pakito97/Big-Data-UNIDAD-1/blob/Development/practice%234.md">
  <img align="left" alt=" Github" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" />
</a>
  </br>
  <br>
<a>
  practice#5 git flow
  <a href="https://github.com/pakito97/Big-Data-UNIDAD-1/blob/Development/practica%20git%20flow.md">
  <img align="left" alt=" Github" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" />
</a>
  </br>


Practice 2

**Ecercise 1**

//Create a list called "list" with the elements "red", "white", "black"
import scala.collection.mutable.ListBuffer
var lista = collection.mutable.ListBuffer("rojo","blanco","negro")

/////////////////////////////////////////////////////////////////////////

**Ecercise 2**

//Add 5 more elements to "list" "green", "yellow", "blue", "orange", "pearl"
import scala.collection.mutable.ListBuffer
var lista = collection.mutable.ListBuffer("rojo","blanco","negro")

lista += "verde"
lista += "amarillo"
lista += "azul"
lista += "naranja"
lista += "perla"

/////////////////////////////////////////////////////////////////////////

**Ecercise 3**

//Get the elements of "list" "green", "yellow", "blue"
import scala.collection.mutable.ListBuffer
var lista = collection.mutable.ListBuffer("rojo","blanco","negro")

lista += "verde"
lista += "amarillo"
lista += "azul"
lista += "naranja"
lista += "perla"

lista slice (3,6)

/////////////////////////////////////////////////////////////////////////

**Ecercise 4**

//Create an array of numbers in the range 1-1000 in steps of 5 by 5
Array.range(1, 1000, 5)

////////////////////////////////////////////////////////////////////////

**Ecercise 5**

//What are the unique elements of the list List (1,3,3,4,6,7,3,7) use conversion to sets
import scala.collection.mutable.ListBuffer
var lista = collection.mutable.ListBuffer(1,3,3,4,6,7,3,7)

lista.toSet

////////////////////////////////////////////////////////////////////////

**Ecercise 6**

/*Create a mutable map named names that contains the following "Jose", 20, "Luis", 24, "Ana", 23, "Susana", "27"
6 a. Print all keys on the map 7 b. Add the following value to the map ("Miguel", 23) */
var mutmap = collection.mutable.Map(("Jose", 20), ("Luis", 24), ("Susana", 27))

//6a
println(mutmap)

//6b
mutmap += ("Miguel" -> 23)

