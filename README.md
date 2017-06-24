It will contain the list of all the Questions from Anything to anything ....

Core Java  ---

{
          Basics like Static,Abstract and other Stuff , Collections, Generics, Multi Threading , Concurrency , Exception Handling ,      Serialization, I/O Streams, Data structures, Garbage Collectors, Collections, Reflections, Synchronization .

     Thinks About How those Data structure Gets implemented .. Means LinkedList is not there then how to implement.

     You should be capable to code your own custom ArrayList or LinkedList it does not exist.

      Focus on Core java First

     Ref: http://javarevisited.blogspot.in/

}
Advanced Java
{
          JDBC , Servlets, JSP , EJB --How we will be connecting to Database(Oracle or MySQL , MongoDB) .. How to run the Query (Interact).. How to works with Stored Procedure , Callable Interface   , Storing the files and images , How to return Multiple Cursors using Java Program...(Hands on Experience) .....

Servlet and JSP will come for the web application ...Our Core Web Technology ... in Java -- Before Going to Spring or Struts.

EJB is also Required .. Application Server and Remote Method Invocation.


}

Frameworks
{

          Any One of the Framework is required .. MVC Framework should be known ... Spring and JSF are two most Used now days. We will go with  the Spring Framework

}

Design Patterns
{
          Design Patterns -- solution Provided for Common Problems that we have in Java ..Total 26 Design Patterns are there  ---                    Singleton ,Abstract, Factory , and Other Design Pattern we should have hands on Experience..

          Spring ---Internally it has Design Pattern in it .. Framework also has in-built Design Pattern  ...

}

Web Services
{

     Expose your functionality as a service ... Difference between RestFul and RestLess .. Inter-portabaility between 2 different Operating System .

SOAP -- based on the Rest Protocol XML based

REST -- based on JSON , XML both  -- Restful

}

ORM Frameworks
{

          Object Relation Mapping  --- < Hibernate  --- To Map the Java Object with SQL Table ... Java(Objects) ----> SQL (Table)

          ORM will be independent of Database ... Automatically our Java Application will be compatible with SQL .. just by mapping Object into Table of SQL.

Hibernate is there and iBatis is also there

}
Unit Testing Frameworks
{
     Junit ---> basically used for test driven Development . We need to write cases in Junit .. Whatever the code we write

     TestNG --- for Integeration Testing and Full Application Testing

     Mockito --->Behaviour , Design and Development .. Business Layer is developed but DAO layer is still not developed  ... Mockito can help us by providing Dummy Object  which will help n Behaviour Driven Development

     Logging Framework ---->  Logs Mechanism ---Informative  ----Logs of our application for our better Debugging .(System.out.print is a bad Practice in Logging Mechanism because for that it need to have one round trip to the server and then print the data in the console  ---> Network calls will be done which is bad practice) --like log4j or sl4j --Leverage your log levels based on the server it will print the logs ...

}

Source Control Management
{

          VSS , Perforce , SVN , GIT

          I am quite Aware with the GIT and SVN

}
Build tools
{
          Ant, Gradle and Maven ---Proper Dependency Management
          Configuration Files ---pom.xml  --- or for Gradle  --gradle.build
          Dependency for our application --> all the jar files management --- compiling , testing  and other making war files  --     simplify Process

}
Application Server
{

One of the Application Server like how to deploy the war files in the server ...Whenever you deploy the war --Transaction Management .. By Default how to manage them at Application -- how you can do the settings at application level ,, How to initialize log4j with the server , handling the transaction , connection pooling --We should know all the settings we can do at the server level ..like getting connection from JNDI

}

Databases {

     Like Writing Stored Procedure , Cursor  and writing Queries and function ... and advance concepts

     Industry is practising with MongoDB -- open Database

}

Operating Systems{
     Linux, Windows --Like at the Application Server Level

}
Other Things are
{

     Web Technologies  -- Javascript , AngularJS , NodeJS, AngularJS , HTML5,CSS3  ,Jquery
       XML Technologies -- XML Parser , (DOM ,SAX, SPATH) , JSON

     AJAX

}
SDLC or Agile Process {

          RAD -- Rapid Application Development
          Standard SDLC Process
          Agile

}

J2EE

Hibernate

Spring MVC

Servlets

JSP

Beans

...We shall links of projects here only.....

Lets take up the 3 day challenge and finish it off before 3 days

What are access Specifiers in Java ?

public , private , protected and default are 4 Access Specifiers in Java

Access Specifiers are used only in Class level means from one class to other class  --->

public is something which u can use at every place ---> Sub Class --> Sub Class in Same Package ----> Sub Class in Different Package ---> In Other parts of the world (Other Package Not Subclass)

private is only limited to Class level ---> You cant access them outside the class

protected and default are left ----->

Protected ----> You cant use them in other world(Other Package)  . But you can use them in the ---> same Class -- > Subclass Same Package -->subclass Different Package .

Default ---> you cant use them in other world and subclass with Different Package ----But you can use them in ----->same Class --->sub Class with same Package

            | Class | Package | Subclass | Subclass | World
            |      |        |(same pkg)|(diff pkg)|
————————————+———————+—————————+——————————+——————————+————————
public      |  +  |    +    |    +    |    +    |  +   
————————————+———————+—————————+——————————+——————————+————————
protected  |  +  |    +    |    +    |    +    |       
————————————+———————+—————————+——————————+——————————+————————
no modifier |  +  |    +    |    +    |          |   
————————————+———————+—————————+——————————+——————————+————————
private    |  +  |        |          |          |   

+ : accessible
blank : not accessible

Package Private(Default)

Can only be seen and used by the package in which it was declared. This is the default in Java (which some see as a mistake).

Protected

Package Private + can be seen by subclasses or package member(Subclass of Different Package).

Static keyword in Java

Java has other modifiers like static, final and abstract.  But these are not Access Modifiers they are just Modifiers

Lets Take Static  ----->

You can't define a static keyword variable inside function ---> Why ?  Because being static variable it must get memory at the time of class loading, which is not possible to provide memory to local variable at the time of class loading because that static variable is inside the function ..So there is no need

Because being static variable it must get memory at the time of class loading, which is not possible to provide memory to local variable at the time of class loading

Ref: http://www.instanceofjava.com/2015/07/core-java-interview-questions-on-static.html

Best Explanation would be from this link :

Other people have explained how to deal with this at the coding level. Allow me to explain the logical and philosophical reasons why static within a method makes no sense. You have to ask the question "How long do you want the variable to last?".

- normal member variables last as long as the instance they are part of;
- variables declared within a method last until the method is exited;
- static class variables last for the lifetime of the class (i.e. forever for most purposes)

So how long do you want your 'static within a method' variable to last? If it's until the end of the method, then you can just use it without static. If it's for the lifetime of the class, then you can declare it as a static member variable. What other options are there?

C++ allows statics within a method, but they end up behaving just like a static class variable, but with reduced scope. Even in C++ they are rarely used. They also end up being stored exactly like static member variables.

The Java designers decided that the small amount of benefit wasn't worth the additional complexity of the language.

Ref :  https://stackoverflow.com/questions/24269308/why-cant-we-declare-static-variables-inside-a-function-body-even-the-function-is

Non-static Variable cannot be referenced from a static context --->  Why because static level variables (Class level variables are created during class loading that is when class files are loaded into memory or class is loaded into memory) and instance level variables are created when you create a instance of that class ...Which is created after .....so here static variable is trying to access non-static(Which is created only when you create an instance of it..for which you have not created up-till now) ..So you are trying to access a variable that does not exist in memory ...That's y java restricts the non-static variables cannot be referenced from a static context...

Ref :http://javarevisited.blogspot.in/2012/02/why-non-static-variable-cannot-be.html

Static Block in Java --

- Static blocks are the blocks which will have braces and with static keyword.
- These static blocks will be called when JVM loads the class.
- Static blocks are the blocks with static keyword.
- Static blocks wont have any name in its prototype.
- Static blocks are class level.
- Static block will be executed only once.
- No return statements.
- No arguments.
- No this or super keywords supported.

Final Keyword with static

So lets suppose this Program ...

 import java.io.*;
import java.util.*;
class staticKey{

final static int b[]=new int[3];

public static void main(String args[]){
b=new int[4];
b[0]=22;
b[0]=23;
}

If you see Closely in this ...array  i have defined final but i am able to change the values inside the array .....But according to final if we declare something as final .. Its value cant be changed once initialised  .....

The final statement is true that its values cannot be changed ..but the contents inside the array can be changed ..but the array cant be changed means

final int b[]=new int[4];

b[1]=23;
b[1]=43; //allowed

But b=new int[5]; //not allowed because u are trying to change the array here

Same thing applies to object

Declaring method and class as final

Method  ----

final ChessPlayer getFirstPlayer() {
        return ChessPlayer.WHITE;
    }
Here we want to specify that method that method cannot be overriden by its subclass.Why we want to do that is because we have an implementation that you dont want it change and it should be consistent accross every implementation of it.

Class -----

If we declare a class as final then we want to specify that class and its all parameters like methods and variables cannot be overriden and class cannot be inherited that is no subclass can be made for that. This is particularly popular with String class where you cant override it and have your own implementation.

Method parameters as final  ---

Consider this example
private void processScores(final TableLayout scoreTable,
      XmlResourceParser scores) throws IOException, XmlPullParserException{

Here if you see parameters of the function are marked as final  .... This is basically because of two reasons ..

Inner class  Use Case and when you don't want its value to be changed

Lets take the Inner Class Use case --

Consider the example

public int checkFinalParams( int a){
int b; //cant be used inside Inner Class unless declared as final
b=a;
//a=2;//not allowed
class A{   //Inner Class
public int B(){
return a; // Not Allowed to use parameter variable here ...Local Variable is not allowed to use in the Inner Class unless it is              // declared as final.
}
}
return b;
}
}

But why the local variable can't be used inside the inner class unless it is declared as final because actually inner class maintains its own copy of variable and its scope ..IF you change something inside the inner class(Value of that variable) then its value will not be persistent outside the class. means its value will not be the changed value . So in order to avoid this java made strict rules that variables inside the function cant be used inside the inner class .. unless declared as final

Ref: http://blog.brendanlacanette.com/2015/08/variable-is-accessed-within-inner-class.html

Second Use Case is we don't some one to change the value of the parameter variable that we are passing so we mark it as final .. It helps to avoid any bugs that might try to change the value of that variable

" final is to prevent yourself from accidentally overwriting them. If you really don't want to change the arguments, then perhaps you should mark them final so that if you actually do, you'll get the error at compile-time rather than finding out at runtime that your code has a bug."

Ref :https://stackoverflow.com/questions/4930114/why-declare-a-function-argument-to-be-final

What is final static variable in Java ?

final keyword says that variable once initialised cannot be changed  ....  so  there can be two types of final ...

static final and final
static means things are assigned at class level and only one value will exist across all instances of that variable.

A static variable stays in the memory. A non-static var is being initialized each time you call the constructor. I think it's better to use

private static final int NUMBER = 10;

Another Better Example to understand this Difference is

For final, it can be assigned different values at runtime when initialized. For example

Class Test{
  public final int a;
}

Test t1  = new Test();
t1.a = 10;
Test t2  = new Test();
t2.a = 20; //fixed

Thus each instance has different value of field a.

For static final, all instances share the same value, and can't be altered after first initialized.

Class TestStatic{
      public static final int a;
}

Test t1  = new Test();
t1.a = 10;
Test t2  = new Test();
t1.a = 20;  // ERROR, CAN'T BE ALTERED AFTER THE FIRST INITIALIZATION.

We should also remember that

There is no reason to have a declaration such as

private final int NUMBER = 10;

If it cannot change, there is no point having one copy per instance.

Simple reason is that if we cannot change the value .. there is no need to maintain different value for every instance ...but it all depends on the requirement of the program and scenario.

What is  private final variable in Java ?

Why we cannot override static methods in Java ?

final methods can't be overriden, because that's what final is designed to do: it's a sign saying "do not override this".

static methods can't be overriden, because they are never called in a polymorphic way: when you call SomeClass.foo() it will always be the foo method of SomeClass, no matter if there is another ExtendedSomeClass that has a much groovier foo method.

final is used to avoid overriding. And a static method is not associated with any instance of a class so the concept is not applicable.


Why Polymorphism ?

One of the best cases one can make for using polymorphism is the ability to refer to interfaces rather than implementations.

Polymorphism is functions or constructors having same name but Different Implementation . In java terms we say that if an entity can be represented in more than one forms, that entity is said to exhibit polymorphism.

You can't overload variables. With your approach, you should give them different name, then overload the getMatrix method for different types.

Variable Overloading Possible or not  ?

I'm writing a class to represent a matrix. I want it to look something like this:

public class matrix {
    private int[][] matrix;
    private double[][] matrix;
    //And so on and so forth so that the user can enter any primitive type and
    //get a matrix of it
}

Is this legal code, or would I have to have different variable names based on the data types that their matrix holds?

Better Answer for that

A better approach is to use Java Generics:

public class Matrix<T> {
    private T[][] matrix;
    public T getMatrix() {return matrix;}
    ...
}

and then create objects of whatever types you want: Matrix<Integer>, Matrix<Double>, etc

Two Types of Polymorphism are there -- Compile time and Run time -- In compile time --compiler will get to know about which method signature to call at compile time .. means compile time only it will link that method with the caller(from where it is called).

In Runtime polymorphism .. (Basically done in Inheritance) ..the compiler will determine which function to call during run time .. because famous when a function is over-ride by another function with same name during run time.Runtime Polymorphism is called Dynamic method dispatch.So basically it states that when call to an over-ridden Method is resolved at run time it is called Run-time Polymorphism or dynamic Method Dispatch.

Ref : https://www.javatpoint.com/runtime-polymorphism-in-java

So Upcasting is when object of class are referenced by Parent Class then its called Runtime Polymorphism

- class A{}
- class B extends A{}

- A a=new B();//upcasting

Another Good Example to tell What is Runtime polymorphism and why it is needed .

- class Bank{
- float getRateOfInterest(){return 0;}
- }
- class SBI extends Bank{
- float getRateOfInterest(){return 8.4f;}
- }
- class ICICI extends Bank{
- float getRateOfInterest(){return 7.3f;}
- }
- class AXIS extends Bank{
- float getRateOfInterest(){return 9.7f;}
- }
- class TestPolymorphism{
- public static void main(String args[]){
- Bank b;
- b=new SBI();
- System.out.println("SBI Rate of Interest: "+b.getRateOfInterest());
- b=new ICICI();
- System.out.println("ICICI Rate of Interest: "+b.getRateOfInterest());
- b=new AXIS();
- System.out.println("AXIS Rate of Interest: "+b.getRateOfInterest());
- }
- }

If you see Bank Class reference is enough to store references of child class . Bank Class can used to call object to of any other Bank like Axis , SBI or ICICI etc .

Similarly Interface reference  can be used to point to any of its implementor

List a =new ArrayList();

List b =new LinkedList();

List c = new Vector();

It's run-time because the flow of program can't be known before execution i.e. only during run-time it can be decided that which form will be used.

The good reason for why Polymorphism is need in java is because the concept is extensively used in implementing inheritance.It plays an important role in allowing objects having different internal structures to share the same external interface.

Run Time Polymorphism is not possible with data members ..

Method is overridden not the datamembers, so runtime polymorphism can't be achieved by data members.

In the example given below, both the classes have a datamember speedlimit, we are accessing the datamember by the reference variable of Parent class which refers to the subclass object. Since we are accessing the datamember which is not overridden, hence it will access the datamember of Parent class always.

Rule: Runtime polymorphism can't be achieved by data members.

- class Bike{
-  int speedlimit=90;
- }
- class Honda3 extends Bike{
-  int speedlimit=150;
-
-  public static void main(String args[]){
-   Bike obj=new Honda3();
-   System.out.println(obj.speedlimit);//90
- }

Polymorphism helps us to actually implement the inheritance in much better way .. Lets suppose you have Class Car and then child Class Maruti ..Both have drive() .. thus both does the same thing .. we can store the reference of Base Class to hold Child Class Reference like

Car c = new Maruti ()

Similarly we can use Interface to do the same thing.

When reference variable of Parent class refers to the object of Child class, it is known as upcasting.

Ref : https://stackoverflow.com/questions/11064409/why-to-use-polymorphism

Why Interfaces ?

First thing to know is what is interface  ?

In the Java programming language, an interface is a reference type, similar to a class, that can contain only constants, method signatures, default methods, static methods, and nested types. ... Interfaces cannot be instantiated—they can only be implemented by classes or extended by other interfaces

Whats the purpose of one interface extending other interface ?

Ref : https://stackoverflow.com/questions/10227410/interface-extends-another-interface-but-implements-its-methods

The purpose of one interface extending, not implementing another, is to build a more specific interface. For example, SortedMap is an interface that extends Map. A client not interested in the sorting aspect can code against Map and handle all the instances of for example TreeMap, which implements SortedMap. At the same time, another client interested in the sorted aspect can use those same instances through the SortedMap interface.

In your example you are repeating the methods from the superInterface. While legal, it's unnecessary and doesn't change anything in the end result. The compiled code will be exactly the same whether these methods are there or not. Whatever Eclipse's hover says is irrelevant to the basic truth that an interface does not implement anything.

Interface and polymorphism are closely related --- Interface help to implement Polymorphism

An interface is a contract (or a protocol, or a common understanding) of what the classes can do. When a class implements a certain interface, it promises to provide implementation to all the abstract methods declared in the interface. Interface defines a set of common behaviours. The classes implement the interface agree to these behaviours and provide their own implementation to the behaviours. This allows you to program at the interface, instead of the actual implementation. One of the main usage of interface is provide a communication contract between two objects. If you know a class implements an interface, then you know that class contains concrete implementations of the methods declared in that interface, and you are guaranteed to be able to invoke these methods safely. In other words, two objects can communicate based on the contract defined in the interface, instead of their specific implementation.

Secondly, Java does not support multiple inheritance (whereas C++ does). Multiple inheritance permits you to derive a subclass from more than one direct superclass. This poses a problem if two direct superclasses have conflicting implementations. (Which one to follow in the subclass?). However, multiple inheritance does have its place. Java does this by permitting you to "implements" more than one interfaces (but you can only "extends" from a single superclass). Since interfaces contain only abstract methods without actual implementation, no conflict can arise among the multiple interfaces. (Interface can hold constants but is not recommended. If a subclass implements two interfaces with conflicting constants, the compiler will flag out a compilation error.)

By implementing a well known interface, you can have polymorphism, which enable you to write generic code that can act on any instance of a class that implements a given interface.

Example is of List and ArrayList,Vector and other classes

What are marker interfaces  ?

Marker interfaces in java are interfaces with no members declared in them. They are just an empty interfaces used to mark or identify a special operation.

Then What is the purpose of marker interface ..When they don't have any methods ?

Maker interface are also called tag interface. They have no fields or methods .

Example of it serializable, clonnable and remote interface.

Basic purpose of marker interface is that JVM sees this marker interface ..then it conveys to JVM that this class will some special operation. When JVM sees some marker interface it does some operation on it to support cloning or serializable etc.

Thus basically they are used for indication purpose to JVM ..but why for this indication can't we set some boolean value ..which can do the same ..Ofcourse we can set that but  advantage of it is that we can use polymorphism with that interface

.

Although i can use annotation in that instead of marker interface .

Why Abstract Class  ?

First of all we need to know what are abstract classes.

So What are abstract classes ?

Abstract classes are classes that contain one or more abstract methods. Anabstract method is a method that is declared, but contains no implementation.Abstract classes may not be instantiated, and require subclasses to provide implementations for the abstract methods.

You cant create an instance of abstract class but can extend it and in subclass you can implement those methods .

Basic use of abstract class is that abstract class create templates for future children class  and also add some added functionality that your child class can utilise later.

Abstract classes are useful over interface when you define implementation details of your class but don't want allow it be directly instantiated (Child class can implement that instead)

How Abstract Class are different from Interface ?

The question instead should be when you should prefer interface and when you should prefer abstract class

Abstract class will provide template of that class as well as the implementation of some methods which you can use directly but you can create instance of that abstract class.

On the other hand interface will just provide template .Interface will just provide contract for Objects to follow ..

In other cases Abstract Classes are much useful as interfaces  .

Abstract Class is that class that is declared Abstract . It may or may not contain abstract methods . But when class is declared as abstract it cannot be instantiated ..but they can be subclassed.

On the other hand Abstract methods are those that are just declared without any implementation.

Any Class that

Its necessary to implement all the methods of the interface.

Object Oriented Pillars in Java ?

Four pillars of OOPS are

- Inheritance
- Polymorphism
- Encapsulation
- Abstraction

Collection Framework in Java

Difference Between HashSet and HashMap in Java ---->HashSet does not Allows Duplicate values ..whereas hashMap Allow ....
Both uses HashTables for their Implementation ...

HashSet is designed on Set Interface -- mathematical Model of Set Interface

HashMap is designed on Map Interface --Map maps key to values

HashSet is a set, e.g. {1,2,3,4,5}

HashMap is a key -> value (key to value) map, e.g. {a -> 1, b -> 2, c -> 2, d -> 1}

Notice in my example above that in the HashMap there must not be duplicate keys, but it may have duplicate values.

In the HashSet, there must be no duplicate elements.

No Duplicate Values in HashSet but in HashMap it is allowed (Although keys cant be duplicate)

https://stackoverflow.com/questions/2773824/difference-between-hashset-and-hashmap