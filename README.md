# Diagramas-Clases
# Primer diagrama
Fish <|--  Animal : Extends

    Cat <|-- Animal : Extends

    Spider <|-- Animal : Extends

    Pet <|.. Cat : implements
    Pet <|.. Fish : implements

    class Pet{

      <<interface>>

    +getName() String
    +setName(n : String) void
    +play()
    }

    class Animal{

    <<abstract>>

      -legs : int

      +Animal(legs : int) 
      +walk() void
      +eat() void
    }

    class Spider{
    }

    class Cat{
     +name : String
    }

    class Fish{
     +name : String
    }
 <p align ="center">
 <image src="/imgDiagrama/1.png"></image>
 </p>  

  
   
   # Segundo diagrama
   
   Encyclopedia <|--  Readingitem : Extends
    
    Customer "buy" -- "1..*" Readingitem

    Magazine <|-- Readingitem : Extends

    Book <|-- Readingitem : Extends

    GST_Chargeable <|.. Magazine : implements
    GST_Chargeable <|.. Encyclopedia : implements

    class GST_Chargeable{

      <<interface>>

    RATE=0.06 : double
    +getGST_Chargeable()double
    }

    class Readingitem{

    <<abstract>>

      -title : String
      -price : double

      +Readingitem(double, String) void
      +getName()void
      +getPrice()double
      +abtract calculatePrice()double
      +abtract displayinto()void

    }

    class Customer{
    -customerName : String
    -totalPay : double
    -item : Readingitem
    +Customer(String)void
    +buy(Readingitem)void
    +getTotalPay()double
    +toString():String

    }

    class Book{
    -author : String
    -year : int
    +Book(String, double, String, int) void
    }

    class Magazine{
    
    -Monthssue : int
    -year : int
    +Magazine(int, int, double, String) void
    }

    class Encyclopedia{
    -Year : int
    +Encyclopedia(String, double, int)void
    }
    
 <p align ="center">
 <image src="/imgDiagrama/2.png"></image>
 </p>  

