**Day 21: Generics**

**Task**

Write  a single generic function named printArray; this function must taken an array of generic elements as a parameter (the exception to this is C++, which takes a vector). The locked Solution class in your editor tests your function.

**Note**: You must use generics to solve this challenge. Do not write overload functions.

**Input Format**

The locked Solutions class in your editor will pass different types of arrays to your printArray function.

**Constraints**

You must have exactly **1** function named printArray.

**Output Format**

Your printArray function should print each element if its generic array parameter on a new line.

**Code**

```
import java.util.*;

class Printer <T> {

/**
    *    Method Name: printArray
    *    Print each element of the generic array on a new line. Do not return anything.
    *    @param A generic array
    **/
    
    // Write your code 
    public static<E> void printArray(E[] array){

       for(E element : array){
           System.out.println(element);
       }
    }

}

public class Generics {
    
    public static void main(String args[]){
        Scanner scanner = new Scanner(System.in);
        int n = scanner.nextInt();
        Integer[] intArray = new Integer[n];
        for (int i = 0; i < n; i++) {
            intArray[i] = scanner.nextInt();
        }

        n = scanner.nextInt();
        String[] stringArray = new String[n];
        for (int i = 0; i < n; i++) {
            stringArray[i] = scanner.next();
        }
        
        Printer<Integer> intPrinter = new Printer<Integer>();
        Printer<String> stringPrinter = new Printer<String>();
        intPrinter.printArray( intArray  );
        stringPrinter.printArray( stringArray );
        if(Printer.class.getDeclaredMethods().length > 1){
            System.out.println("The Printer class should only have 1 method named printArray.");
        }
    } 
}
```

