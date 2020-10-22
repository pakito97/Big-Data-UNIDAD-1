#Excerce


def  funcion(n: Int): Int =  
{  
// Si el numero ingresado en la función es menor a 2, el numero ingresado será regresado  
if (n<2)  
{  
return n  
}  
// En todo caso, la funcion hara una serie de sumas, y regresa el resultado  
else  
{  
return funcion(n-1) + funcion(n-2)  
}  
}  
funcion(9)  
