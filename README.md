# Java-basic-Bit2Byte

```java
class Main {
    public static void main(String[] args) {
        float f = 1.19F;
        double d = 1.19; 
        int test = 15;
        // i = f; // compile time error.
        test = (int)f; // ok
        
        // expression vs statement 
        // num = 5 --> expression 
        // num = 5; --> statement 
        
        int count; // declaration 
        count = 0; // assignment 
        int check = 5; // initialization 
        
        // double > float > long > int
        double b1 = 100;
        long b2 = 10L;
        double b3 = b1 + b2; 
        
        // byte data type 
        // -128 to 127 range 
        byte b11 = 5; 
        
        // n Java, when you perform arithmetic operations (+, -, *, /, etc.) with byte, short, or char, the operands are automatically promoted to int before the operation.
        
        byte b4 = 10;
        // byte b10 = b1 + b2; // error 
        byte b5 = 5 + 10; // OK 
        
        // not using unary operator 
        byte b6 = 5; 
        byte b7 = 6;
        b6 = b7; 
        
        // using unary operator 
        byte b8 = +5;
        byte b9 = 7;
        b8 = b9; // ok 
        // b8 = +b9 // error 
        
        //increment and decrement 
        
        // increment then assign 
        int k = 5;
       int postIncr = ++k;
       System.out.println("Post Increment: " + postIncr);
       System.out.println("k after post increment: " + k);
       
       // assign then increment 
       k = 5; 
       int preIncr = k++;
       System.out.println("Pre Increment: " + preIncr);
       System.out.println("k after pre increment: " + k);
       
       // In Java, the Integer class maintains a cache of Integer objects for values in the range -128 to 127 (inclusive).
       Integer num1 = 100;
       Integer num2 = 100;
       System.out.println(num1==num2); // true
       
       Integer num3 = 10000;
       Integer num4 = 10000;
       System.out.println(num3==num4); // false
       
       // boolean-expression ? true-expression : false-expression
       int a = 5;
       int b = 55;
       int mx = a>b ? a : b;
       
       // same 
       if (a > b) {
         mx = a;
       } 
       else {
       mx = b;
      }
      
      
      /*************/
      // block statement
      
      {
          int blockTest = 100;
          System.out.println("Inside of block: " + blockTest);
      }
      // error
      // variable not recognize
      // System.out.println("Outside of block: " + blockTest);
      
      // switch same as c
      int day = 2; 
      switch(day){
          case 1:
              System.out.println("Saturday");
              break;
          case 2:
              System.out.println("Sunday");
              break;
          default:
             System.out.println("Invalid Day");
      }
      
      // for loop same as c 
      for(int i=0;i<=5;i++){
          System.out.println(i);
      }
      
      // while loop same as c
      int m = 0;
      while(m<=5){
          System.out.println(m);
          m++;
      }
      
      // for-each loop
      int[] arr= {10,20,30};
      for(int num:arr){
          System.out.println(num);
      }
      
      
      
      // last topic 
        int i = 24;
        int j = 48;
        k = 57;
        
        count = 0;
        boolean outputFromLogical = (i<48) || (j == 48 ) || (++count < 1000); //--------(a)
        System.out.println(outputFromLogical + " -> " + count); // true -> 0 
        
        
        boolean outputFromShortCircuit = (i<48) | (j == 48 ) | (++count < 1000); //-----(b)
        System.out.println(outputFromShortCircuit + " -> " + count); // true -> 1
        
        boolean outputAnd = (i == j) && (i++ ==k); //--------(c)
        System.out.println(outputAnd+" "+i); // false 24
        
        boolean outputShortAnd = (i == j) & (i++ ==k); //----(d)
        System.out.println(outputShortAnd+" "+i); // false 25
              
       
    }
}

```
