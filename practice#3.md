#Exercice 3

// Practice 3, analyse the following code with your own words

def listEvens(list:List[Int]): String ={
    for(n <- list){
        if(n%2==0){
            println(s"$n is even")
        }else{
            println(s"$n is odd")
        }
    }
    return "Done"
}
//In this first code, we see that it helps us to obtain through a list the even and odd numbers within the list
/ * We first create the list called listEvens and indicate the type of list, in this case they will be pure integers and indicate a string, in case they enter a number in the list
double bone with decimal point will mark error, then we create a for loop that will help us to read all the content of the list and within the same for we have
another loop called if-else that its only function is to tell the user what number is odd or even, and finally a string called done will be returned */

val l = List(1,2,3,4,5,6,7,8)
val l2 = List(4,3,22,55,7,8)
/*here we give the values that will be inside the list that we previously created but that will be stored in an equally created variable*/ 
listEvens(l)
listEvens(l2)
/*Here we only extract from the listEvens list and from the variable created the content of the list and we will see which numbers are ar or odd * /

//3 7 afortunado

def afortunado(list:List[Int]): Int={
    var res=0
    for(n <- list){
        if(n==7){
            res = res + 14
        }else{
            res = res + n
        }
    }
    return res
}
/*In this code as in the previous one we will create a list called lucky of integer type and then we will create a variable called res
with a value of 0, using a for loop we will make an if-else loop with which if n is equal to 7 the variable res will be equal to the sum of the same variable
plus 14 and we will return the variable res, otherwise it will be added whatever is worth n*/ 

val af= List(1,7,7)
println(afortunado(af))
/*We create the variable af where the values that we indicate will be deposited in the previously created list val af = List (1,7,7)
and later the variable af will be printed with the sum of the list List (1,7,7)*/ 

def balance(list:List[Int]): Boolean={
    var primera = 0
    var segunda = 0

    segunda = list.sum

    for(i <- Range(0,list.length)){
        primera = primera + list(i)
        segunda = segunda - list(i)

        if(primera == segunda){
            return true
        }
    }
    return false 
}
/*in this code we create a list called balance of integer type we initialize two variables called
first and second with an initial value of 0 and we will equalize the second variable to the sum function of list
and we will create a for loop where we will make a lup using the range of the list starting with 0,
and in turn we will indicate that the first and second variables will be equal to themselves but the value of i list (i) will be added to the first variable
which is obtained from the range of the list and the second variable is subtracted the same value from i list (i)
later using an if-else loop we will ask if the variables are identical, if they are, a true will be returned
otherwise it will return a false*/

val bl = List(3,2,1)
val bl2 = List(2,3,3,2)
val bl3 = List(10,30,90)
/*we create variables called bl, bl2, bl3 which will store the values of the balance list*/

balance(bl)
balance(bl2)
balance(bl3)
/*here we call the balance list with the value obtained that is inside the variable created before
bl, bl2 bl3 and we will see if the balance is true or false*/

def palindromo(palabra:String):Boolean ={
    return (palabra == palabra.reverse)
}
/*we create a function called palindrome, and initialize a variable called word of type string
and we will return the variable word and if it is true and false*/

val palabra = "OSO"
val palabra2 = "ANNA"
val palabra3 = "JUAN"
/*we create variables called word that contain a value of type string, which are word palindromes and others that
we will check if palindromes or not*/

println(palindromo(palabra))
println(palindromo(palabra2))
println(palindromo(palabra3))
/*here we are only going to print the variable created before and if it is true or false*/
