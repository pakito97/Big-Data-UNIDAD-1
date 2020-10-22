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
  practice#2
  <a href="https://github.com/pakito97/Big-Data-UNIDAD-1/blob/Development/practice%232.md">
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
  practice#5 git flow
  <a href="https://github.com/pakito97/Big-Data-UNIDAD-1/blob/Development/practica%20git%20flow.md">
  <img align="left" alt=" Github" width="22px" src="https://cdn.jsdelivr.net/npm/simple-icons@v3/icons/github.svg" />
</a>
  </br>


Practice 4

**Excercice 1**

def  funcion(n: Int): Int =  
{  
// If the number entered in the function is less than 2, the number entered will be returned
if (n<2)  
{  
return n  
}  
// In any case, the function will do a series of sums, and returns the result
else  
{  
return funcion(n-1) + funcion(n-2)  
}  
}  
funcion(9)  

///////////////////////////////////////////////////////////////////////////////////////////

**Excercice 2**

def  funcion1(n: Double): Double =  
{  
// If the number entered in the function is less than 2, the number entered will be returned
if (n<2)  
{
**return n  
}  
// 
In any case, the following will be done
else  
{  
// The mathematical formula is more extensive, but I decided to do it in small parts
// and then join it in the variable (j)
var p = ((1+(Math.sqrt(5)))/2)  
var a = Math.pow(p,n)  
var b = Math.pow((1-p),n)  
var c = Math.sqrt(5)  
var j = ((a-(b)))/(c)  
// The result of (j) will be the result of returning (return)
return(j)  
}  
  
}  
funcion1(9)  

////////////////////////////////////////////////////////////////////////////////////////

**Excercice 3**

// In this third algorithm a function was added that after having performed
// the corresponding operations the function will give us a result (return)
// this must be an integer value (Int)
def  funcion2(n: Int): Int =  
{  
var a = 0  
var b = 1  
var c = 0  

// A cycle (for) is started where k = 1, it will begin to cycle until it becomes (n)
// (n) represents the value to be entered in the function
for (k <- 1 to n)  
{  
// Depending on the cycle (for) the variables (c, a, b) will start to change
your result
// until the loop is finished (for)
c = b + a  
a = b  
b = c  
}  
// The result will be returned with (return)
return(a)  
}  
funcion2(9) 

//////////////////////////////////////////////////////////////////////////////////////////////////////////

**Excercice 4**

def  funcion3(n: Int): Int =  
{  
var a = 0  
var b = 1  
// A cycle (for) is started where k = 1, it will begin to cycle until it becomes (n)
// (n) represents the value to be entered in the function
for(k <- 1 to n)  
{  
b = b + a  
a = b - a  
// Depending on the (for) loop, the variables (b, a) will begin to change their result
// until the loop is finished (for)
}  
// The result will be returned with (return)
return(a)  
}  
funcion3(9

/////////////////////////////////////////////////////////////////////////////////////////////////////////////

**Excercice 5**

def  funcion4(n: Int): Double =  
{  
// An array is created starting from 0 to (n + 1)
val vector = Array.range(0,n+1)  
// If the variable (n) is less than 2, the same variable is returned as a result
if (n < 2)  
{  
return (n)  
}  
// Otherwise the vector with space (0) will have a value of zero (0)
// and the vector with space (1) will have a value of one (1) 
else  
{  
vector(0) = 0  
vector(1) = 1  
// It begins to cycle with a for the vector
for (k <- 2 to n)  
{  
vector(k) = vector(k-1) + vector(k-2)  
}  
// 
The result will be the variable (n) based on the established vector
return vector(n)  
}  
}  
funcion4(9) 
