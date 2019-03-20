# File I/O

```scala
// Use import java.io.PrintWriter to write to a file
val writer = new PrintWriter("test.txt")
writer.write("Just some random text\nSome more random text")
writer.close()
 
// Use import scala.io.Source to read from files
val textFromFile = Source.fromFile("test.txt", "UTF-8")
 
// Iterate through each line in the file and print
val lineIterator = textFromFile.getLines
for(line <- lineIterator){
  println(line)
}
textFromFile.close()
```
