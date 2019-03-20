# Functions

```scala
// def funcName (param1:dataType, param2:dataType) : returnType = {
//    function body
//    return valueToReturn
// }
 
// You can give parameters default values
def getSum( num1:Int = 1, num2:Int = 1) : Int = {
  return num1 + num2
}
 
println("5 + 4 = " + getSum(5,4))
 
// you can use named arguments
println("5 + 4 = " + getSum(num2=5, num1=4))
 
// A function that returns nothing (Procedure)
def sayHi() : Unit = {
  println("Hi how are you doing")
}
 
sayHi
 
// Receive variable number of arguments
def getSum2(args: Int*) : Int = {
  var sum : Int = 0
  for(num <- args){
    sum += num
  }
  sum
}
 
println("getSum2: " + getSum2(1,2,3,4,5))
 
// Recursion example calculating factorials
def factorial(num : BigInt) : BigInt = {
  if (num <= 1)
    1
  else
    num * factorial(num - 1)
}
 
// 1st: num = 4 * factorial(3) = 4 * 6 = 24
// 2nd: num = 3 * factorial(2) = 3 * 2 = 6
// 3rd: num = 2 * factorial(1) = 2 * 1 = 2
 
println("Factorial of 4 = " + factorial(4))
```

## Higher Order Functions

```scala
// Functions can be passed like any other variable
// You need the _ after the function to state you meant the function
val log10Func = log10 _
 
println(log10Func(1000))
 
// You can apply a function to all items of a list with map
List(1000.0,10000.0).map(log10Func).foreach(println)
 
// You can use an anonymous function with map as well
// Receives an Int x and multiplies every x by 50
List(1,2,3,4,5).map((x : Int) => x * 50).foreach(println)
 
// Filter will pass only those values that meet a condition
List(1,2,3,4,5,6).filter(_ % 2 == 0).foreach(println)
 
// Pass different functions to a function
def times3(num : Int) = num * 3
def times4(num : Int) = num * 4
 
// Define the function parameter type and return type
def multIt(func : (Int) => Double, num : Int ) = {
  func(num)
}
 
printf("3 * 100 = %.1f)\n", multIt(times3, 100))
 
// A closure is a function that depends on a variable declared outside
// of the function
val divisorVal = 5
val divisor5 = (num : Double) => num / divisorVal
println("5 / 5 = " + divisor5(5.0))
```
