# Conditionals

```scala
// if statements are like Java except they return a value like the
// ternary operator
 
// Conditional Operators : ==, !=, >, <, >=, <=
// Logical Operators : &&, ||, !
 
var age = 18
 
val canVote = if (age >= 18) "yes" else "no"
 
// You have to use { } in the REPL, but not otherwise
if ((age >= 5) && (age <= 6)) {
  println("Go to Kindergarten")
} else if ((age > 6) && (age <= 7)) {
  println("Go to Grade 1")
} else {
  println("Go to Grade " + (age - 5))
}
 
true || false
!(true)
```
