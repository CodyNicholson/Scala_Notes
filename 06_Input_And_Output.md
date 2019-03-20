# Input & Output

```scala
var numberGuess = 0
 
do{
  print("Guess a number : ")
 
  // You can also use readInt, readDouble, readByte, readShort, readLong,
  //
  numberGuess = readLine.toInt
 
  } while(numberGuess != 15)
 
  printf("You guessed the secret number %d\n", 15)
 
  // You can use string interpolation
  val name = "Derek"
  val age = 39
  val weight = 175.5
  println(s"Hello $name")
 
  println(f"I am ${age + 1} and weigh $weight%.2f")
 
  // printf Style Format Specifiers
  // %c : Characters
  // %d : Integers
  // %f : Floating Point Numbers
  // %s : Strings
  printf("'%5d'\n",5) // Right justify
 
  printf("'%-5d Hi'\n",5) // Left justify
 
  printf("'%05d'\n",5) // Zero Fill
 
  printf("'%.5f'\n",3.14) // 5 decimal minimum & maximum
 
  printf("'%-5s'\n", "Hi") // Left Justify String
 
  // Special Characters : \n, \b, \\, \a
```
