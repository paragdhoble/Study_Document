# Study_Document

Java:-
1.	Primitive datatypes
2.	Difference between abstract class and interface
3.	Final class, final method and Final variable
4.	Difference between final, finally and finalize
5.	Virtual methods in java
6.	Abstract class in java
7.	Static class
8.	OOPs concept
9.	What are constructors in Java?
10.	What is Polymorphism?
11.	What is runtime polymorphism or dynamic method dispatch?
12.	What is method overloading and method overriding?
13.	Can weoverride a private or static method in Java?
14.	Can weoverload a finaland static method in Java?
15.	What is multiple inheritance? Is it supported by Java?
16.	Difference between String and String buffer
17.	Why string is immutable
18.	Can we create object of static and abstract class
19.	Checked and unchecked exception
20.	Difference between throw and throws
21.	What is the output if we print object
22.	Difference between == and equals 



Programs:-
1.	Reverse string
2.	Program – static block in parent
3.	Program - finalize block
4.	Custom Exception
5.	Count the occurrence of each character in String
6.	Bubble sort



Jenkins:-
	A)
	B)
	
































1.	Primitive datatypes
Every variable has a type declared in the source code. There are two kinds of types: reference types and primitive types. Reference types are references to objects. Primitive types directly contain values. 
There are 8 primitive types:

DataType	Size	Default Value
byte	8 bit	0
short	16 bit	0
int	32 bit	0
long	64 bit	0L
float	32 bit	0.0f
double	64 bit	0.0d
boolean	1 bit	FALSE
char	16 bit	\u0000'


2. Difference between abstract class and interface

Abstract class	Interface
1) Abstract class can have abstract and non-abstract methods.	Interface can have only abstract methods. Since Java 8, it can have default and static methods also.
2) Abstract class doesn't support multiple inheritance.	Interface supports multiple inheritance.
3) Abstract class can have final, non-final, static and non-static variables.	Interface has only static and final variables.
4) The abstract keyword is used to declare abstract class.	The interface keyword is used to declare interface.
5) An abstract classcan extend another Java class and implement multiple Java interfaces.	An interface can extend another Java interface only.
6) An abstract classcan be extended using keyword 'extends'	An interface classcan be implemented using keyword 'implements'
7) A Javaabstract classcan have class members like private, protected, etc.	Members of a Java interface are public by default.
8)Example:	Example:
public abstract class Shape{	public interface Drawable{
public abstract void draw();	void draw();
}	}



3) Final class, final method and Final variable

 


	Final Class:-

A final class is simply a class that can't be extended.
Example:-
final class Show{
	public void show1(){
		System.out.println("Hello world.");
	}
}

class show2 extends Show{
	public void show3() {
		System.out.println("Hello world.2");
	}
}

** This program will not compile as we cannot extend final class

Final method:-
Final method indicates that the method cannot be overridden by subclasses

Final variable:-
The only difference between a normal variable and a final variable is that we can re-assign value to a normal variable but we cannot change the value of a final variable once assigned. Hence final variables must be used only for the values that we want to remain constant throughout the execution of program.


4. Difference between final, finally and finalize

final	finally	finalize
Final is used to apply restrictions on class, method and variable. Final class can't be inherited, final method can't be overridden and final variable value can't be changed.	Finally is used to place important code, it will be executed whether exception is handled or not.	Finalize is used to perform clean up processing just before object is garbage collected.
Final is a keyword.	Finally is a block.	Finalize is a method.


5. Virtual methods in java

In Java, all non-static methods are by default "virtual functions." Only methods marked with the keyword final, which cannot be overridden, along with private methods, which are not inherited, are non-virtual.
Static or final methods are non-virtual.


6. Abstract class in java

Abstract class is a way of implementing 0 to 100% abstraction. A class declared with abstract keyword is known as an abstract class. An abstract class may or may not contain abstract method. Abstract classes cannot be instantiated.


7.	Static class

Outer classes cannot be static, but nested/inner classes can be. That basically helps you to use the nested/inner class without creating an instance of the outer class. 
classStaticClass {
	public static class StaticInnerClass{
		public void show() {
			System.out.println("Inner class as static class");
		}
	}
}

public class StaticClassExample {
	public static void main(String args[]) {
		StaticClass obj1=new StaticClass();
		StaticClass.StaticInnerClass obj2= new StaticClass.StaticInnerClass();
		//obj1.show(); is not allowed
		obj2.show();
	}
}



8.	OOPS Concept

Core OOPS concepts are
1) Class
The class is a group of similar entities. It is only a logical component and not the physical entity. For example, if you had a class called “Expensive Cars” it could have objects like Mercedes, BMW, Toyota, etc. Its properties (data) can be price or speed of these cars. While the methods may be performed with these cars are driving, reverse, braking etc.

2) Object

An object can be defined as an instance of a class, and there can be multiple instances of an object in a program. An Object contains both the data and the function, which operates on the data. For example - chair, bike, marker, pen, table, car, etc.

3) Inheritance

Inheritance is an OOPS concept in which one object acquires the properties and behaviors of the parent object. It’s creating a parent-child relationship between two classes. It offers robust and natural mechanism for organizing and structure of any software.

4) Polymorphism

Polymorphism refers to the ability of a variable, object or function to take on multiple forms. For example, in English, the verb “run” has a different meaning if you use it with “a laptop,” “a foot race, and ”business.&rdquo Here, we understand the meaning of “run” based on the other words used along with it.The same also applied to Polymorphism.

5) Abstraction

An abstraction is an act of representing essential features without including background details. It is a technique of creating a new data type that is suited for a specific application. For example, while driving a car, you do not have to be concerned with its internal working. Here you just need to concern about parts like steering wheel, Gears, accelerator, etc.

6) Encapsulation

Encapsulation is an OOP technique of wrapping the data and code. In this OOPS concept, the variables of a class are always hidden from other classes. It can only be accessed using the methods of their current class. For example - in school, a student cannot exist without a class.

7) Association

Association is a relationship between two objects. It defines the diversity between objects. In this OOP concept, all object have their separate lifecycle, and there is no owner. For example, many students can associate with one teacher while one student can also associate with multiple teachers.

8) Aggregation

In this technique, all objects have their separate lifecycle. However, there is ownership such that child object can’t belong to another parent object. For example consider class/objects department and teacher. Here, a single teacher can’t belong to multiple departments, but even if we delete the department, the teacher object will never be destroyed.

9) Composition

A composition is a specialized form of Aggregation. It is also called "death" relationship. Child objects do not have their lifecycle so when parent object deletes all child object will also delete automatically. For that, let’s take an example of House and rooms. Any house can have several rooms. One room can’t become part of two different houses. So, if you delete the house room will also be deleted.


9.	What are constructors in Java?
In Java, constructor refers to a block of code which is used to initialize an object. It must have the same name as that of the class. Also, it has no return type and it is automatically called when an object is created.
There are two types of constructors:
1.	Default constructor
2.	Parameterized constructor


10.	What is Polymorphism?
 
 
Polymorphism is briefly described as “one interface, many implementations”. Polymorphism is a characteristic of being able to assign a different meaning or usage to something in different contexts – specifically, to allow an entity such as a variable, a function, or an object to have more than one form. There are two types of polymorphism:
1.	Compile time polymorphism
2.	Run time polymorphism
 
Compile time polymorphism is method overloading whereas Runtime time polymorphism is done using inheritance and interface.



11.	What is runtime polymorphism or dynamic method dispatch?
In Java, runtime polymorphism or dynamic method dispatch is a process in which a call to an overridden method is resolved at runtime rather than at compile-time. In this process, an overridden method is called through the reference variable of a superclass. Let’s take a look at the example below to understand it better.
classSuperClass {
	void show() {
		System.out.println("Show of super class");
	}
}

classchildClassextendsSuperClass {
	void show() {
		System.out.println("Show of child class");
	}
}

publicclassTestSuperClass {

	publicstaticvoid main(String args[]) {
		SuperClasssc = newSuperClass();
		childClasscs = newchildClass();

		SuperClasssc2 = newchildClass();
		
sc.show();
		cs.show();
		sc2.show();
	}
}
Output:-
Show of super class
Show of child class
Show of child class


12.	What is method overloading and method overriding?
Method Overloading :
•	In Method Overloading, Methods of the same class shares the same name but each method must have different number of parameters or parameters having different types and order.
•	Method Overloading is to “add” or “extend” more to method’s behavior.
•	It is a compile time polymorphism.
•	The methods must have different signature.
•	It may or may not need inheritance in Method Overloading.
Let’s take a look at the example below to understand it better.
class Adder {
	staticint add(inta, intb) {
		returna + b;
	}

	staticdouble add(doublea, doubleb) {
		returna + b;
	}

	publicstaticvoid main(String args[]) {
		System.out.println(Adder.add(11, 11));
		System.out.println(Adder.add(12.3, 12.6));
	}
}
Method Overriding:  
•	In Method Overriding, sub class have the same method with same name and exactly the same number and type of parameters and same return type as a super class.
•	Method Overriding is to “Change” existing behavior of method.
•	It is a run time polymorphism.
•	The methods must have same signature.
•	It always requires inheritance in Method Overriding.
Let’s take a look at the example below to understand it better.
class Car {
	void run() {
		System.out.println("car is running");
	}

class Audi extends Car{
void run()
{
System.out.println("Audi is running safely with 100km");
}
publicstaticvoidmain(String args[]) {
		Car b = newAudi();
		b.run();
	}
}


13.	Can we override a private or static method in Java?
Wecannot override a private or static method in Java. If you create a similar method with same return type and same method arguments in child class then it will hide the super class method; this is known as method hiding. Similarly, you cannot override a private method in sub class because it’s not accessible there. What you can do is create another private method with the same name in the child class. Let’s take a look at the example below to understand it better.
class Base {
	privatestaticvoid display() {
		System.out.println("Static or class method from Base");
	}

	publicvoid print() {
		System.out.println("Non-static or instance method from Base");
	}

	class Derived extends Base {
		privatestaticvoiddisplay() {
			System.out.println("Static or class method from Derived");
		}

		publicvoid print() {
			System.out.println("Non-static or instance method from Derived");
		}

publicclass test {
	publicstaticvoidmain(String args[])
		{
			Base obj= newDerived();
			obj1.display();
			obj1.print();
		}
	}


14.	Can weoverload a finaland static method in Java?
Yes. We can overload final and static method.


15.	What is multiple inheritance? Is it supported by Java?
 If a child class inherits the property from multiple classes is known as multiple inheritance. Java does not allow to extend multiple classes.
The problem with multiple inheritance is that if multiple parent classes have a same method name, then at runtime it becomes difficult for the compiler to decide which method to execute from the child class.
Therefore, Java doesn’t support multiple inheritance. The problem is commonly referred as Diamond Problem.


16.	Difference between String and String buffer

Basis for comparison	String	StringBuffer
Basic	The length of the String object is fixed.	The length of the StringBuffer can be increased.
Modification	String object is immutable.	StringBuffer object is mutable.
Performance	It is slower during concatenation.	It is faster during concatenation.
Memory	Consumes more memory.	Consumes less memory.
Storage	String constant pool.	Heap Memory.


17.	Why string is immutable
String objects are immutable in Java because they provide no methods that modify the state of an existing String object. They only provide methods that create new String objects based on the content of existing ones.

String str = "Hello World";
str = "Hi World!";
By seeing this code you would say that the value of str has changed so how can it be immutable? Let me explain this:
In first statement an object is created using string literal “Hello World”, in second statement when we assigned the new string literal “Hi World!” to str, the object itself didn’t change instead a new object got created in memory using string literal “Hi World!” and the reference to it is assigned to str. So basically both the objects “Hello World” and “Hi World!” exists in memory having different references(locations).

18.	Can we create object of static and abstract class??
No. We cannot create object of static and abstract class


19.	Checked and unchecked Exceptions
In Java exceptions under Error and RuntimeException classes are unchecked exceptions, everything else under throwableclass is checked.
 

There are two types of exceptions: checked exception and unchecked exception. The main difference between checked and unchecked exception is that the checked exceptions are checked at compile-time while unchecked exceptions are checked at runtime.

A)	What are checked exceptions?
Checked exceptions are checked at compile-time. It means if a method is throwing a checked exception then it should handle the exception using try-catch block or it should declare the exception using throws keyword, otherwise the program will give a compilation error.
In this example, we are reading the file myfile.txt and displaying its content on the screen. In this program there are three places where a checked exception is thrown as mentioned in the comments below. FileInputStream which is used for specifying the file path and name, throws FileNotFoundException. The read() method which reads the file content throws IOException and the close() method which closes the file input stream also throws IOException.
 
Output:-
 

Here are the few other Checked Exceptions –
a)	SQLException
b)	IOException
c)	ClassNotFoundException
d)	InvocationTargetException

How to resolve the error (checked exceptions)? 
Method 1: Declare the exception using throws keyword.
Method 2: Handle them using try-catch blocks.

B)	What are unchecked exceptions?
Unchecked exceptions are not checked at compile time. It means if your program is throwing an unchecked exception and even if you didn’t handle/declare that exception, the program won’t give a compilation error. Most of the times these exception occurs due to the bad data provided by user during the user-program interaction. It is up to the programmer to judge the conditions in advance, that can cause such exceptions and handle them appropriately. All Unchecked exceptions are direct sub classes of RuntimeException class.

Unchecked Exception Example
 
If you compile this code, it would compile successfully however when you will run it, it would throw ArithmeticException. That clearly shows that unchecked exceptions are not checked at compile-time, they occurs at runtime.

Here are the few unchecked exception classes:
a)	NullPointerException
b)	ArrayIndexOutOfBoundsException
c)	ArithmeticException
d)	IllegalArgumentException
e)	NumberFormatException


20.	Difference between throw and throws

Throw	Throws
Java throw keyword is used to explicitly throw an exception.	Java throws keyword is used to declare an exception.
Checked exception cannot be propagated using throw only.	Checked exception can be propagated with throws.
Throw is followed by an instance.	Throws is followed by class.
Throw is used within the method.	Throws is used with the method signature.
You cannot throw multiple exceptions.	You can declare multiple exceptions e.g. public void method()throws IOException,SQLException.


21.	What is the output if we print object
System.out.println("Value of object of class="+ objectOfClass);
It's will print the default implementation of Object class toString() method.
Returns a string representation of the object. In general, the toString method returns a string that "textually represents" this object. The result should be a concise but informative representation that is easy for a person to read. It is recommended that all subclasses override this method.

The toString method for class Object returns a string consisting of the name of the class of which the object is an instance, the at-sign character `@', and the unsigned hexadecimal representation of the hash code of the object. In other words, this method returns a string equal to the value of: getClass().getName() + '@' + Integer.toHexString(hashCode())
Default Implementation:-
public String  toString() {
returngetClass().getName() + "@" + Integer.toHexString(hashCode());
     }
output:-PackageName.classname@HASHCODE


22.	Difference between == and equals
1. Main difference between .equals() method and == operator is that one is method and other is operator.
2. We can use == operators for reference comparison (address comparison) and .equals() method for content comparison. 
In simple words, == checks if both objects point to the same memory location whereas .equals() evaluates to the comparison of values in the objects.




***** Programs *****
1.	Reverse the string
String str="thisismytest";
	char reverse[]=str.toCharArray();
		
	for (inti=0,j=reverse.length-1;i<reverse.length/2;i++,j--) {
		char temp=reverse[i];
		reverse[i]=reverse[j];
		reverse[j]=temp;
	}
		
	System.out.println("Result="+ String.copyValueOf(reverse));
	System.out.println("Result 2="+ Arrays.toString(reverse));


2.	Program – static block in parent
 
Output:-
 

3.	Custom exception
 

Output:-
 

4.	Test

5.	Count the occurrence of each character in String
 

Output:-
 

6.	Bubble Sort

 
Output:-
 



Jenkins:- 
1) What is Jenkins?
2) What is continuous integration?
3) What is the requirement for using Jenkins?
4) What are the advantages of Jenkins?
5) Explain how you can move or copy Jenkins from one server to another?
6) What are the commands you can use to start Jenkins manually?
7) Some of the useful plugins in Jenkin?
8) Explain how you can deploy a custom build of a core plugin?
9) Explain how can create a backup and copy files in Jenkins?
10) Explain how you can clone a Git repository via Jenkins?
11) Explain how you can set up Jenkins job?
12) What are the two components Jenkins is mainly integrated with?
13) What is master and slave??

1) What is Jenkins?
Jenkins is an open source tool with plugin built for continuous integration purpose. Theprinciple functionality of Jenkins is to keep a track of version control system and to initiate andmonitor a build system if changes occur. It monitors the whole process and provides reports andnotifications to alert.

2) What is continuous integration?
Continuous Integration is a development practice in which the developers are required to commit changes to the source code in a shared repository several times a day or more frequently. Every commit made in the repository is then built. This allows the teams to detect the problems early.

3) What is the requirement for using Jenkins?
To use Jenkins you require
	a) A source code repository which is accessible, for instance, a Git repository
	b) A working build script, e.g., a Maven script, checked into the repository

4) Mention what are the advantages of Jenkins?
Advantage of Jenkins includes
1.	At integration stage, build failures are cached
2.	For each code commit changes an automatic build report notification generates
3.	To notify developers about build report success or failure, it is integrated with LDAP mailserver
4.	Achieves continuous integration agile development and test driven development
5.	With simple steps, maven release project is automated
6.	Easy tracking of bugs at early stage in development environment than production

5) Explain how you can move or copy Jenkins from one server to another?
	a) Slide a job from one installation of Jenkins to another by copying the related jobdirectory
	b) Make a copy of an already existing job by making clone of a job directory by a differentname
	c) Renaming an existing job by renaming a directory.

6) Mention what are the commands you can use to start Jenkins manually?
To start Jenkins manually, you can use either of the following
•	(Jenkins_url)/restart: Forces a restart without waiting for builds to complete
•	(Jenkin_url)/safeRestart: Allows all running builds to complete

7) Mention some of the useful plugins in Jenkin?
Some of the important plugins in Jenkin includes
•	Maven 2 project
•	Amazon EC2
•	HTML publisher
•	Copy artifact
•	Join
•	Green Balls

8) Explain how you can deploy a custom build of a core plugin?
To deploy a custom field of a core plugin, you have to do following things
•	Stop Jenkins
•	Copy the custom HPI to $Jenkins_Home/plugins
•	Delete the previously expanded plugin directory
•	Make an empty file called .hpi.pinned
•	Start Jenkins

9) Explain how can create a backup and copy files in Jenkins?
Jenkins saves all the setting, build artifacts and logs in its home directory, to create a back-up of your Jenkins setup, just copy this directory. You can also copy a job directory to clone orreplicate a job or rename the directory.

10) Explain how you can clone a Git repository via Jenkins?
To clone a Git repository via Jenkins, you have to enter the e-mail and user name for yourJenkins system. For that, you have to switch into your job directory and execute the “gitconfig”command.

11) Explain how you can set up Jenkins job?
To create a project that is handled via jobs in Jenkins. Select New item from the menu, oncethis done enter a name for the job and select free-style job. Then click OK to create new job inJenkins. The next page enables you to configure your job.

12) Mention what are the two components Jenkins is mainly integrated with?
Jenkin is mainly integrated with two components
•	Version Control system like GIT, SVN
•	And build tools like Apache Maven.

13) What is master and slave??
Jenkins Distributed Architecture
Jenkins uses a Master-Slave architecture to manage distributed builds. In this architecture, Master and Slave communicate through TCP/IP protocol.
Jenkins Master
Your main Jenkins server is the Master. The Master’s job is to handle:
•	Scheduling build jobs.
•	Dispatching builds to the slaves for the actual execution.
•	Monitor the slaves (possibly taking them online and offline as required).
•	Recording and presenting the build results.
•	A Master instance of Jenkins can also execute build jobs directly.

Jenkins Slave
A Slave is a Java executable that runs on a remote machine. Following are the characteristics of Jenkins Slaves:
•	It hears requests from the Jenkins Master instance.
•	Slaves can run on a variety of operating systems.
•	The job of a Slave is to do as they are told to, which involves executing build jobs dispatched by the Master.
•	You can configure a project to always run on a particular Slave machine, or a particular type of Slave machine, or simply let Jenkins pick the next available Slave.
The diagram below is self-explanatory. It consists of a Jenkins Master which is managing three Jenkins Slave.
 
Now let us look at an example in which Jenkins is used for testing in different environments like: Ubuntu, MAC, Windows etc.
The diagram below represents the same:
 
The following functions are performed in the above image:
•	Jenkins checks the Git repository at periodic intervals for any changes made in the source code.
•	Each builds requires a different testing environment which is not possible for a single Jenkins server. In order to perform testing in different environments Jenkins uses various Slaves as shown in the diagram.
•	Jenkins Master requests these Slaves to perform testing and to generate test reports.


14) pipeline


Q. Why Java is platform independent?
Platform independent practically means “write once run anywhere”. Java is called so because of its byte codes which can run on any system irrespective of its underlying operating system.


Q. Why java is not 100% Object-oriented?
Java is not 100% Object-oriented because it makes use of eight primitive datatypes such as boolean, byte, char, int, float, double, long, short which are not objects.



Q. Explain JVM, JRE and JDK?
JVM (Java Virtual Machine): It is an abstract machine. It is a specification that provides run-time environment in which java bytecode can be executed. It follows three notations:
•	Specification: It is a document that describes the implementation of the Java virtual machine. It is provided by Sun and other companies.
•	Implementation: It is a program that meets the requirements of JVM specification.
•	Runtime Instance: An instance of JVM is created whenever you write a java command on the command prompt and run the class.
JRE (Java Runtime Environment): JRE refers to a runtime environment in which java bytecode can be executed. It implements the JVM (Java Virtual Machine) and provides all the class libraries and other support files that JVM uses at runtime. So JRE is a software package that contains what is required to run a Java program. Basically, it’s an implementation of the JVM which physically exists. 
JDK(Java Development Kit) : It is the tool necessary to compile, document and package Java programs. The JDK completely includes JRE which contains tools for Java programmers. The Java Development Kit is provided free of charge. Along with JRE, it includes an interpreter/loader, a compiler (javac), an archiver (jar), a documentation generator (javadoc) and other tools needed in Java development. In short, it contains JRE + development tools.
Refer to this below image and understand how exactly these components reside:
 


Q. Explain public static void main(String args[]).
public : Public is an access modifier, which is used to specify who can access this method. Public means that this Method will be accessible by any Class.
static : It is a keyword in java which identifies it is class based i.e it can be accessed without creating the instance of a Class.
void : It is the return type of the method. Void defines the method which will not return any value.
main: It is the name of the method which is searched by JVM as a starting point for an application with a particular signature only. It is the method where the main execution occurs.
String args[] : It is the parameter passed to the main method.





Q. What are wrapper classes?
Wrapper classes converts the java primitives into the reference types (objects). Every primitive data type has a class dedicated to it. These are known as wrapper classes because they “wrap” the primitive data type into an object of that class. Refer to the below image which displays different primitive type, wrapper class and constructor argument. 
 


Q

Q. What is singleton class and how can we make a class singleton?
Singleton class is a class whose only one instance can be created at any given time, in one JVM. A class can be made singleton by making its constructor private.












Q. What is the difference between Array list and vector?
Array List	Vector
Array List is not synchronized.	Vector is synchronized.
Array List is fast as it’s non-synchronized.	Vector is slow as it is thread safe.
If an element is inserted into the Array List, it increases its Array size by 50%.	Vector defaults to doubling size of its array.
Array List does not define the increment size.	Vector defines the increment size.
Array List can only use Iterator for traversing an Array List.	Except Hashtable, Vector is the only other class which uses both Enumeration and Iterator.


Q. What is the difference between equals() and == ?
Equals() method is defined in Object class in Java and used for checking equality of two objects defined by business logic.
“==” or equality operator in Java is a binary operator provided by Java programming language and used to compare primitives and objects. publicboolean equals(Object o) is the method provided by the Object class. The default implementation uses == operator to compare two objects. For example: method can be overridden like String class. equals() method is used to compare the values of two objects.

public static void main(String[] args) {
	String str1 = new String("ABCD");
	String str2 = new String("ABCD");
	if (str1 == str2) {
		System.out.println("String 1 == String 2 is true");
	} else {
		System.out.println("String 1 == String 2 is false");
		String Str3 = str2;
		if (str2 == Str3) {
			System.out.println("String 2 == String 3 is true");
		} else {
			System.out.println("String 2 == String 3 is false");
		}
		if (str1.equals(str2)) {
			System.out.println("String 1 equals string 2 is true");
		} else {
			System.out.println("String 1 equals string 2 is false");
		}
	}
}


Q10. What are the differences between Heap and Stack Memory?
The major difference between Heap and Stack memory are:
Features	Stack	Heap
Memory	Stack memory is used only by one thread of execution.	Heap memory is used by all the parts of the application.
Access	Stack memory can’t be accessed by other threads.	Objects stored in the heap are globally accessible.
Memory Management	Follows LIFO manner to free memory.	Memory management is based on generation associated to each object.
Lifetime	Exists until the end of execution of the thread.	Heap memory lives from the start till the end of application execution.
Usage	Stack memory only contains local primitive and reference variables to objects in heap space.	Whenever an object is created, it’s always stored in the Heap space.



Q3. What is the difference between abstract classes and interfaces?
Abstract Class	Interfaces
An abstract class can provide complete, default code and/or just the details that have to be overridden.	An interface cannot provide any code at all,just the signature.
In case of abstract class, a class may extend only one abstract class.	A Class may implement several interfaces.
An abstract class can have non-abstract methods.	All methods of an Interface are abstract.
An abstract class can have instance variables.	An Interface cannot have instance variables
An abstract class can have any visibility: public, private, protected.	An Interface visibility must be public (or) none.
If we add a new method to an abstract class then we have the option of providing default implementation and therefore all the existing code might work properly	If we add a new method to an Interface then we have to track down all the implementations of the interface and define implementation for the new method
An abstract class can contain constructors	An Interface cannot contain constructors
Abstract classes are fast	Interfaces are slow as it requires extra indirection to find corresponding method in the actual class

 
Q7. What is association?
Association is a relationship where all object have their own lifecycle and there is no owner. Let’s take an example of Teacher and Student. Multiple students can associate with a single teacher and a single student can associate with multiple teachers but there is no ownership between the objects and both have their own lifecycle. These relationship can be one to one, One to many, many to one and many to many.

Q8. What do you mean by aggregation?
Aggregation is a specialized form of Association where all object have their own lifecycle but there is ownership and child object cannot belongs to another parent object. Let’s take an example of Department and teacher. A single teacher cannot belongs to multiple departments, but if we delete the department teacher object will not destroy. 

Q9. What is composition in Java?
Composition is again specialized form of Aggregation and we can call this as a “death” relationship. It is a strong type of Aggregation. Child object does not have their lifecycle and if parent object deletes all child object will also be deleted. Let’s take again an example of relationship between House and rooms. House can contain multiple rooms there is no independent life of room and any room cannot belongs to two different house if we delete the house room will automatically delete.


1) What is difference between JDK,JRE and JVM?
JVM
JVM is an acronym for Java Virtual Machine, it is an abstract machine which provides the runtime environment in which java bytecode can be executed. It is a specification.
JVMs are available for many hardware and software platforms (so JVM is platform dependent).
JRE
JRE stands for Java Runtime Environment. It is the implementation of JVM.
JDK
JDK is an acronym for Java Development Kit. It physically exists. It contains JRE + development tools.

________________________________________
2) How many types of memory areas are allocated by JVM?
Many types:
1.	Class(Method) Area
2.	Heap
3.	Stack
4.	Program Counter Register
5.	Native Method Stack

________________________________________
3) What is JIT compiler?
Just-In-Time(JIT) compiler:It is used to improve the performance. JIT compiles parts of the byte code that have similar functionality at the same time, and hence reduces the amount of time needed for compilation.Here the term “compiler” refers to a translator from the instruction set of a Java virtual machine (JVM) to the instruction set of a specific CPU.
________________________________________
4) What is platform?
A platform is basically the hardware or software environment in which a program runs. There are two types of platforms software-based and hardware-based. Java provides software-based platform.
________________________________________
5) What is the main difference between Java platform and other platforms?
The Java platform differs from most other platforms in the sense that it's a software-based platform that runs on top of other hardware-based platforms.It has two components:
1.	Runtime Environment
2.	API(Application Programming Interface)
________________________________________
6) What gives Java its 'write once and run anywhere' nature?
The bytecode. Java is compiled to be a byte code which is the intermediate language between source code and machine code. This byte code is not platform specific and hence can be fed to any platform.
________________________________________
7) What is classloader?
The classloader is a subsystem of JVM that is used to load classes and interfaces.There are many types of classloaders e.g. Bootstrap classloader, Extension classloader, System classloader, Plugin classloader etc.
________________________________________
8) Is Empty .java file name a valid source file name?
Yes, save your java file by .java only, compile it by javac .java and run by java yourclassname Let's take a simple example:
//save by .java only  
class A {
	publicstaticvoid main(String args[]) {
		System.out.println("Hello java");
	}
}
// compile by javac .java
// run by java A________________________________________
9) Is delete,next,main,exit or null keyword in java?
No.
________________________________________
10) If I don't provide any arguments on the command line, then the String array of Main method will be empty or null?
It is empty. But not null.
________________________________________
11) What if I write static public void instead of public static void?
Program compiles and runs properly.
________________________________________
12) What is the default value of the local variables?
The local variables are not initialized to any default value, neither primitives nor object references.
________________________________________
13) What is difference between object oriented programming language and object based programming language?
Object based programming languages follow all the features of OOPs except Inheritance. Examples of object based programming languages are JavaScript, VBScript etc.
14) What will be the initial value of an object reference which is defined as an instance variable?
The object references are all initialized to null in Java.
________________________________________
15) What is constructor?
o	Constructor is just like a method that is used to initialize the state of an object. It is invoked at the time of object creation.

________________________________________
16) What is the purpose of default constructor?
o	The default constructor provides the default values to the objects. The java compiler creates a default constructor only if there is no constructor in the class.
________________________________________
17) Does constructor return any value?
Ans: yes, that is current instance (You cannot use return type yet it returns a value).
________________________________________
18) Is constructor inherited?
No, constructor is not inherited.
________________________________________
19) Can you make a constructor final?
No, constructor can't be final.
________________________________________
20) What is static variable?
o	static variable is used to refer the common property of all objects (that is not unique for each object) e.g. company name of employees,college name of students etc.
o	static variable gets memory only once in class area at the time of class loading.

________________________________________
21) What is static method?
o	A static method belongs to the class rather than object of a class.
o	A static method can be invoked without the need for creating an instance of a class.
o	static method can access static data member and can change the value of it.

________________________________________
22) Why main method is static?
because object is not required to call static method if It were non-static method,jvmcreats object first then call main() method that will lead to the problem of extra memory allocation.
________________________________________
23) What is static block?
o	Is used to initialize the static data member.
o	It is excuted before main method at the time of classloading.

________________________________________
24) Can we execute a program without main() method?
Ans) Yes, one of the way is static block.
________________________________________

25) What if the static modifier is removed from the signature of the main method?
Program compiles. But at runtime throws an error "NoSuchMethodError".
________________________________________
26) What is difference between static (class) method and instance method?
static or class method	instance method
1)A method i.e. declared as static is known as static method.	A method i.e. not declared as static is known as instance method.
2)Object is not required to call static method.	Object is required to call instance methods.
3)Non-static (instance) members cannot be accessed in static context (static method, static block and static nested class) directly.	static and non-static variables both can be accessed in instance methods.
4)For example: public static int cube(int n){ return n*n*n;}	For example: public void msg(){...}.
________________________________________
27) What is this in java?
It is a keyword that that refers to the current object.
________________________________________
28) What is Inheritance?
Inheritance is a mechanism in which one object acquires all the properties and behavior of another object of another class. It represents IS-A relationship. It is used for Code Reusability and Method Overriding.

________________________________________
29) Which class is the superclass for every class?
Object class.
________________________________________
30) Why multiple inheritance is not supported in java?
o	To reduce the complexity and simplify the language, multiple inheritance is not supported in java in case of class.
________________________________________
31) What is composition?
Holding the reference of the other class within some other class is known as composition.
________________________________________
32) What is difference between aggregation and composition?
Aggregation represents weak relationship whereas composition represents strong relationship. For example: bike has an indicator (aggregation) but bike has an engine (compostion).
33) Why Java does not support pointers?
Pointer is a variable that refers to the memory address. They are not used in java because they are unsafe(unsecured) and complex to understand.
________________________________________
34) What is super in java?
It is a keyword that refers to the immediate parent class object.
________________________________________
35) Can you use this() and super() both in a constructor?
No. Because super() or this() must be the first statement.
________________________________________
36) What is object cloning?
The object cloning is used to create the exact copy of an object. 
________________________________________
37) What is method overloading?
If a class have multiple methods by same name but different parameters, it is known as Method Overloading. It increases the readability of the program.
________________________________________
38) Why method overloading is not possible by changing the return type in java?
Because of ambiguity.
________________________________________
39) Can we overload main() method?
Yes, You can have many main() methods in a class by overloading the main method.
40) What is method overriding:
If a subclass provides a specific implementation of a method that is already provided by its parent class, it is known as Method Overriding. It is used for runtime polymorphism and to provide the specific implementation of the method.
________________________________________
41) Can we override static method?
No, you can't override the static method because they are the part of class not object.
________________________________________
42) Why we cannot override static method?
It is because the static method is the part of class and it is bound with class whereas instance method is bound with object and static gets memory in class area and instance gets memory in heap.
________________________________________
43) Can we override the overloaded method?
Yes.
________________________________________
44) Difference between method Overloading and Overriding.
Method Overloading	Method Overriding
1) Method overloading increases the readability of the program.	Method overriding provides the specific implementation of the method that is already provided by its super class.
2) methodoverlaoding is occurs within the class.	Method overriding occurs in two classes that have IS-A relationship.
3) In this case, parameter must be different.	In this case, parameter must be same.
45) Can you have virtual functions in Java?
Yes, all functions in Java are virtual by default.
________________________________________

46) What is covariant return type?
Now, since java5, it is possible to override any method by changing the return type if the return type of the subclass overriding method is subclass type. It is known as covariant return type. 
________________________________________
47) What is final variable?
If you make any variable as final, you cannot change the value of final variable(It will be constant).
________________________________________
48) What is final method?
Final methods can't be overriden.
________________________________________
49) What is final class?
Final class can't be inherited. 
________________________________________
50) What is blank final variable?
A final variable, not initalized at the time of declaration, is known as blank final variable.
________________________________________
51) Can we intialize blank final variable?
Yes, only in constructor if it is non-static. If it is static blank final variable, it can be initialized only in the static block.
________________________________________
52) Can you declare the main method as final?
Yes, such as, public static final void main(String[] args){}.

53) What is Runtime Polymorphism?
Runtime polymorphism or dynamic method dispatch is a process in which a call to an overridden method is resolved at runtime rather than at compile-time.
In this process, an overridden method is called through the reference variable of a super class. The determination of the method to be called is based on the object being referred to by the reference variable.
________________________________________
54) Can you achieve Runtime Polymorphism by data members?
No.
________________________________________
55) What is the difference between static binding and dynamic binding?
In case of static binding type of object is determined at compile time whereas in dynamic binding type of object is determined at runtime.
________________________________________
56) What is abstraction?
Abstraction is a process of hiding the implementation details and showing only functionality to the user.
Abstraction lets you focus on what the object does instead of how it does it.
________________________________________
57) What is the difference between abstraction and encapsulation?
Abstraction hides the implementation details whereas encapsulation wraps code and data into a single unit.
________________________________________
58) What is abstract class?
A class that is declared as abstract is known as abstract class. It needs to be extended and its method implemented. It cannot be instantiated.
________________________________________
59) Can there be any abstract method without abstract class?
No, if there is any abstract method in a class, that class must be abstract.
________________________________________
60) Can you use abstract and final both with a method?
No, because abstract method needs to be overridden whereas you can't override final method.
________________________________________
61) Is it possible to instantiate the abstract class?
No, abstract class can never be instantiated.
________________________________________
62) What is interface?
Interface is a blueprint of a class that have static constants and abstract methods.It can be used to achieve fully abstraction and multiple inheritance.
________________________________________
63) Can you declare an interface method static?
No, because methods of an interface is abstract by default, and static and abstract keywords can't be used together.
________________________________________
64) Can an Interface be final?
No, because its implementation is provided by another class.
________________________________________
65) What is marker interface?
An interface that have no data member and method is known as a marker interface.For example Serializable, Cloneable etc.
________________________________________
66) What is difference between abstract class and interface?
Abstract class	Interface
1)An abstract class can have method body (non-abstract methods).	Interface have only abstract methods.
2)An abstract class can have instance variables.	An interface cannot have instance variables.
3)An abstract class can have constructor.	Interface cannot have constructor.
4)An abstract class can have static methods.	Interface cannot have static methods.
5)You can extends one abstract class.	You can implement multiple interfaces.
67) Can we define private and protected modifiers for variables in interfaces?
No, they are implicitly public.
________________________________________
68) When can an object reference be cast to an interface reference?
An object reference can be cast to an interface reference when the object implements the referenced interface.
________________________________________
69) What is package?
A package is a group of similar type of classes interfaces and sub-packages. It provides access protection and removes naming collision.
________________________________________
70) Do I need to import java.lang package any time? Why ?
No. It is by default loaded internally by the JVM.
________________________________________
71) Can I import same package/class twice? Will the JVM load the package twice at runtime?
One can import the same package or same class multiple times. Neither compiler nor JVM complains about it.But the JVM will internally load the class only once no matter how many times you import the same class.
________________________________________
72) What is static import ?
By static import, we can access the static members of a class directly, there is no to qualify it with the class name.


73) What is Exception Handling?
Exception Handling is a mechanism to handle runtime errors.It is mainly used to handle checked exceptions.
________________________________________

74) What is difference between Checked Exception and Unchecked Exception?
1)Checked Exception
The classes that extend Throwable class except RuntimeException and Error are known as checked exceptions e.g.IOException,SQLException etc. Checked exceptions are checked at compile-time.
2)Unchecked Exception
The classes that extend RuntimeException are known as unchecked exceptions e.g. ArithmeticException,NullPointerException etc. Unchecked exceptions are not checked at compile-time.
________________________________________
75) What is the base class for Error and Exception?
Throwable.
________________________________________
76) Is it necessary that each try block must be followed by a catch block?
It is not necessary that each try block must be followed by a catch block. It should be followed by either a catch block OR a finally block. And whatever exceptions are likely to be thrown should be declared in the throws clause of the method.
________________________________________
77) What is finally block?
o	finally block is a block that is always executed. 
________________________________________
78) Can finally block be used without catch?
o	Yes, by try block. finally must be followed by either try or catch. 
________________________________________
79) Is there any case when finally will not be executed?
finally block will not be executed if program exits(either by calling System.exit() or by causing a fatal error that causes the process to abort). 
________________________________________



80) What is difference between throw and throws?
throw keyword	throws keyword
1)throw is used to explicitly throw an exception.	throws is used to declare an exception.
2)checked exceptions can not be propagated with throw only.	checked exception can be propagated with throws.
3)throw is followed by an instance.	throws is followed by class.
4)throw is used within the method.	throws is used with the method signature.
5)You cannot throw multiple exception	You can declare multiple exception e.g. public void method()throws IOException,SQLException.
________________________________________
81) Can an exception be rethrown?
Yes.
________________________________________
82) Can subclass overriding method declare an exception if parent class method doesn't throw an exception ?
Yes but only unchecked exception not checked.
________________________________________
83) What is exception propagation ?
Forwarding the exception object to the invoking method is known as exception propagation.
________________________________________
84) What is the meaning of immutable in terms of String?
The simple meaning of immutable is unmodifiable or unchangeable. Once string object has been created, its value can't be changed.
________________________________________


85) Why string objects are immutable in java?
Because java uses the concept of string literal. Suppose there are 5 reference variables,allreferes to one object "sachin".If one reference variable changes the value of the object, it will be affected to all the reference variables. That is why string objects are immutable in java.
________________________________________
86) How many ways we can create the string object?
There are two ways to create the string object, by string literal and by new keyword.
________________________________________
87) How many objects will be created in the following code?
String s1="Welcome";  
String s2="Welcome";  
String s3="Welcome";  
Only one object.
________________________________________
88) Why java uses the concept of string literal?
To make Java more memory efficient (because no new objects are created if it exists already in string constant pool).
________________________________________
89) How many objects will be created in the following code?
String s = new String("Welcome");  
Two objects, one in string constant pool and other in non-pool(heap).
________________________________________
90) What is the basic difference between string and stringbuffer object?
String is an immutable object. StringBuffer is a mutable object.
________________________________________
91) What is the difference between StringBuffer and StringBuilder ?
StringBuffer is synchronized whereas StringBuilder is not synchronized.
________________________________________
92) How can we create immutable class in java ?
We can create immutable class as the String class by defining final class and
________________________________________
93) What is the purpose of toString() method in java ?
The toString() method returns the string representation of any object. If you print any object, java compiler internally invokes the toString() method on the object. So overriding the toString() method, returns the desired output, it can be the state of an object etc. depends on your implementation.
________________________________________
94) What is nested class?
A class which is declared inside another class is known as nested class. There are 4 types of nested class member inner class, local inner class, anonymous inner class and static nested class.
________________________________________
95) Is there any difference between nested classes and inner classes?
Yes, inner classes are non-static nested classes i.e. inner classes are the part of nested classes.
________________________________________
96) Can we access the non-final local variable, inside the local inner class?
No, local variable must be constant if you want to access it in local inner class.
________________________________________
97) What is nested interface?
Any interface i.e. declared inside the interface or class, is known as nested interface. It is static by default.
________________________________________
98) Can a class have an interface?
Yes, it is known as nested interface.
________________________________________
99) Can an Interface have a class?
Yes, they are static implicitly.



117) what is Garbage Collection?
Garbage collection is a process of reclaiming the runtime unused objects.It is performed for memory management.
118) What is gc()?
gc() is a daemon thread.gc() method is defined in System class that is used to send request to JVM to perform garbage collection.
119) What is the purpose of finalize() method?
finalize() method is invoked just before the object is garbage collected.It is used to perform cleanup processing.
120) Can an unrefrenced objects be refrenced again?
Yes.
121)What kind of thread is the Garbage collector thread?
Daemon thread.
122)What is difference between final, finally and finalize?
final: final is a keyword, final can be variable, method or class.You, can't change the value of final variable, can't override final method, can't inherit final class.
finally: finally block is used in exception handling. finally block is always executed.
finalize():finalize() method is used in garbage collection.finalize() method is invoked just before the object is garbage collected.The finalize() method can be used to perform any cleanup processing.
________________________________________
123) What is the purpose of the Runtime class?
The purpose of the Runtime class is to provide access to the Java runtime system.
124) How will you invoke any external process in Java?
By Runtime.getRuntime().exec(?) method.
________________________________________


125) What is the difference between the Reader/Writer class hierarchy and the InputStream/OutputStream class hierarchy?
The Reader/Writer class hierarchy is character-oriented, and the InputStream/OutputStream class hierarchy is byte-oriented.
126)Whatan I/O filter?
An I/O filter is an object that reads from one stream and writes to another, usually altering the data in some way as it is passed from one stream to another.
________________________________________
127) What is serialization?
Serialization is a process of writing the state of an object into a byte stream.It is mainly used to travel object's state on the network.
128) What is Deserialization?
Deserialization is the process of reconstructing the object from the serialized state.It is the reverse operation of serialization.
129) What is transient keyword?
If you define any data member as transient,it will not be serialized. 
130)What is Externalizable?
Externalizable interface is used to write the state of an object into a byte stream in compressed format.It is not a marker interface.
131)What is the difference between Serializalble and Externalizable interface?
Serializable is a marker interface but Externalizable is not a marker interface.When you use Serializable interface, your class is serialized automatically by default. But you can override writeObject() and readObject() two methods to control more complex object serailization process. When you use Externalizable interface, you have a complete control over your class's serialization process.
________________________________________

132)How do I convert a numeric IP address like 192.18.97.39 into a hostname like java.sun.com?
By InetAddress.getByName("192.18.97.39").getHostName() where 192.18.97.39 is the IP address.
________________________________________
133) What is reflection?
Reflection is the process of examining or modifying the runtime behaviour of a class at runtime.It is used in:
o	IDE (Integreted Development Environment) e.g. Eclipse, MyEclipse, NetBeans.
o	Debugger
o	Test Tools etc.
134) Can you access the private method from outside the class?
Yes, by changing the runtime behaviour of a class if the class is not secured.


148) What are wrapper classes?
Wrapper classes are classes that allow primitive types to be accessed as objects.
149) What is a native method?
A native method is a method that is implemented in a language other than Java.
150) What is the purpose of the System class?
The purpose of the System class is to provide access to system resources.
151) What comes to mind when someone mentions a shallow copy in Java?
Object cloning.
152) What is singleton class?
Singleton class means that any given time only one instance of the class is present, in one JVM.
________________________________________
153) Which containers use a border layout as their default layout?
The Window, Frame and Dialog classes use a border layout as their default layout.
154) Which containers use a FlowLayout as their default layout?
The Panel and Applet classes use the FlowLayout as their default layout.
155) What are peerless components?
The peerless components are called light weight components.
156) is the difference between a Scrollbar and a ScrollPane?
A Scrollbar is a Component, but not a Container. A ScrollPane is a Container. A ScrollPane handles its own events and performs its own scrolling.
157) What is a lightweight component?
Lightweight components are the one which doesn?t go with the native call to obtain the graphical units. They share their parent component graphical units to render them. For example, Swing components.
158) What is a heavyweight component?
For every paint call, there will be a native call to get the graphical units.For Example, AWT.
159) What is an applet?
An applet is a small java program that runs inside the browser and generates dynamic contents.
160) Can you write a Java class that could be used both as an applet as well as an application?
Yes. Add a main() method to the applet.
________________________________________
161) What is Locale?
A Locale object represents a specific geographical, political, or cultural region.
162) How will you load a specific locale?
By ResourceBundle.getBundle(?) method.
________________________________________
163) What is a JavaBean?
are reusable software components written in the Java programming language, designed to be manipulated visually by a software development environment, like JBuilder or VisualAge for Java.
________________________________________
164) Can RMI and Corba based applications interact?
Yes they can. RMI is available with IIOP as the transport protocol instead of JRMP.


Java Multithreading Interview Questions

1) What is multithreading?
Multithreading is a process of executing multiple threads simultaneously. Its main advantage is:
o	Threads share the same address space.
o	Thread is lightweight.
o	Cost of communication between process is low.
________________________________________
2) What is thread?
A thread is a lightweight subprocess.It is a separate path of execution.It is called separate path of execution because each thread runs in a separate stack frame.
________________________________________
3) What is the difference between preemptive scheduling and time slicing?
Under preemptive scheduling, the highest priority task executes until it enters the waiting or dead states or a higher priority task comes into existence. Under time slicing, a task executes for a predefined slice of time and then reenters the pool of ready tasks. The scheduler then determines which task should execute next, based on priority and other factors.
________________________________________

4) What does join() method?
The join() method waits for a thread to die. In other words, it causes the currently running threads to stop executing until the thread it joins with completes its task.
________________________________________




5) What is difference between wait() and sleep() method?
wait()	sleep()
1) The wait() method is defined in Object class.	The sleep() method is defined in Thread class.
2) wait() method releases the lock.	The sleep() method doesn't releases the lock.
________________________________________
6) Is it possible to start a thread twice?
No, there is no possibility to start a thread twice. If we does, it throws an exception.
________________________________________
7) Can we call the run() method instead of start()?
yes, but it will not work as a thread rather it will work as a normal object so there will not be context-switching between the threads.
________________________________________
8) What about the daemon threads?
The daemon threads are basically the low priority threads that provides the background support to the user threads. It provides services to the user threads.
________________________________________
9) Can we make the user thread as daemon thread if thread is started?
No, if you do so, it will throw IllegalThreadStateException
________________________________________
10) What is shutdown hook?
The shutdown hook is basically a thread i.e. invoked implicitely before JVM shuts down. So we can use it perform clean up resource.
________________________________________
11) When should we interrupt a thread?
We should interrupt a thread if we want to break out the sleep or wait state of a thread.
________________________________________

12) What is synchronization?
Synchronization is the capabilility of control the access of multiple threads to any shared resource.It is used:
1.	To prevent thread interference.
2.	To prevent consistency problem.
________________________________________
13) What is the purpose of Synchronized block?
o	Synchronized block is used to lock an object for any shared resource.
o	Scope of synchronized block is smaller than the method.
________________________________________
14) Can Java object be locked down for exclusive use by a given thread?
Yes. You can lock an object by putting it in a "synchronized" block. The locked object is inaccessible to any thread other than the one that explicitly claimed it.
________________________________________
15) What is static synchronization?
If you make any static method as synchronized, the lock will be on the class not on object.  
________________________________________

16) What is the difference between notify() and notifyAll()?
The notify() is used to unblock one waiting thread whereas notifyAll() method is used to unblock all the threads in waiting state.
________________________________________
17)What is deadlock?
Deadlock is a situation when two threads are waiting on each other to release a resource. Each thread waiting for a resource which is held by the other waiting thread.





JDBC Interview Questions
1) What is JDBC?
JDBC is a Java API that is used to connect and execute query to the database. JDBC API uses jdbc drivers to connect to the database.
________________________________________
2) What is JDBC Driver?
JDBC Driver is a software component that enables java application to interact with the database. There are 4 types of JDBC drivers:
1.	JDBC-ODBC bridge driver
2.	Native-API driver (partially java driver)
3.	Network Protocol driver (fully java driver)
4.	Thin driver (fully java driver)
________________________________________
3) What are the steps to connect to the database in java?
o	Registering the driver class
o	Creating connection
o	Creating statement
o	Executing queries
o	Closing connection
________________________________________
4) What are the JDBC API components?
The java.sql package contains interfaces and classes for JDBC API.
Interfaces:
o	Connection
o	Statement
o	PreparedStatement
o	ResultSet
o	ResultSetMetaData
o	DatabaseMetaData
o	CallableStatement etc.
Classes:
o	DriverManager
o	Blob
o	Clob
o	Types
o	SQLException etc.
________________________________________
5) What are the JDBC statements?
There are 3 JDBC statements.
1.	Statement
2.	PreparedStatement
3.	CallableStatement
________________________________________
6) What is the difference between Statement and PreparedStatement interface?
In case of Statement, query is complied each time whereas in case of PreparedStatement, query is complied only once. So performance of PreparedStatement is better than Statement.

________________________________________
7) How can we execute stored procedures and functions?
By using Callable statement interface, we can execute procedures and functions.
________________________________________
8) What is the role of JDBC DriverManager class?
The DriverManager class manages the registered drivers. It can be used to register and unregister drivers. It provides factory method that returns the instance of Connection.

________________________________________
9) What does the JDBC Connection interface?
The Connection interface maintains a session with the database. It can be used for transaction management. It provides factory methods that returns the instance of Statement, PreparedStatement, CallableStatement and DatabaseMetaData.

________________________________________
10) What does the JDBC ResultSet interface?
The ResultSet object represents a row of a table. It can be used to change the cursor pointer and get the information from the database.

________________________________________
11) What does the JDBC ResultSetMetaData interface?
The ResultSetMetaData interface returns the information of table such as total number of columns, column name, column type etc.

________________________________________
12) What does the JDBC DatabaseMetaData interface?
The DatabaseMetaData interface returns the information of the database such as username, driver name, driver version, number of tables, number of views etc.

________________________________________
13) Which interface is responsible for transaction management in JDBC?
The Connection interface provides methods for transaction management such as commit(), rollback() etc.

________________________________________
14) What is batch processing and how to perform batch processing in JDBC?
By using batch processing technique in JDBC, we can execute multiple queries. It makes the performance fast.

________________________________________
15) How can we store and retrieve images from the database?
By using PreparedStatement interface, we can store and retrieve images.




Java Collections Interview Questions
1) What is the difference between ArrayList and Vector?
No.	ArrayList	Vector
1)	ArrayList is not synchronized.	Vector is synchronized.
2)	ArrayList is not a legacy class.	Vector is a legacy class.
3)	ArrayList increases its size by 50% of the array size.	Vector increases its size by doubling the array size.
________________________________________
2) What is the difference between ArrayList and LinkedList?
No.	ArrayList	LinkedList
1)	ArrayList uses a dynamic array.	LinkedList uses doubly linked list.
2)	ArrayList is not efficient for manipulation because a lot of shifting is required.	LinkedList is efficient for manipulation.
3)	ArrayList is better to store and fetch data.	LinkedList is better to manipulate data.
________________________________________
3) What is the difference between Iterator and ListIterator?
Iterator traverses the elements in forward direction only whereas ListIterator traverses the elements in forward and backward direction.
No.	Iterator	ListIterator
1)	Iterator traverses the elements in forward direction only.	ListIterator traverses the elements in backward and forward directions both.
2)	Iterator can be used in List, Set and Queue.	ListIterator can be used in List only.
________________________________________
4) What is the difference between Iterator and Enumeration?
No.	Iterator	Enumeration
1)	Iterator can traverse legacy and non-legacy elements.	Enumeration can traverse only legacy elements.
2)	Iterator is fail-fast.	Enumeration is not fail-fast.
3)	Iterator is slower than Enumeration.	Enumeration is faster than Iterator.
________________________________________
5) What is the difference between List and Set?
List can contain duplicate elements whereas Set contains only unique elements.
________________________________________
6) What is the difference between HashSet and TreeSet?
HashSet maintains no order whereas TreeSet maintains ascending order.
________________________________________
7) What is the difference between Set and Map?
Set contains values only whereas Map contains key and values both.
________________________________________
8) What is the difference between HashSet and HashMap?
HashSet contains only values whereas HashMap contains entry(key,value). HashSet can be iterated but HashMap need to convert into Set to be iterated.
________________________________________
9) What is the difference between HashMap and TreeMap?
HashMap maintains no order but TreeMap maintains ascending order.
________________________________________



10) What is the difference between HashMap and Hashtable?
No.	HashMap	Hashtable
1)	HashMap is not synchronized.	Hashtable is synchronized.
2)	HashMap can contain one null key and multiple null values.	Hashtable cannot contain any null key or null value.
________________________________________
11) What is the difference between Collection and Collections?
Collection is an interface whereas Collections is a class. Collection interface provides normal functionality of data structure to List, Set and Queue. But, Collections class is to sort and synchronize collection elements.
________________________________________
12) What is the difference between Comparable and Comparator?
No.	Comparable	Comparator
1)	Comparable provides only one sort of sequence.	Comparator provides multiple sort of sequences.
2)	It provides one method named compareTo().	It provides one method named compare().
3)	It is found in java.lang package.	it is found in java.util package.
4)	If we implement Comparable interface, actual class is modified.	Actual class is not modified.
________________________________________
13) What is the advantage of Properties file?
If you change the value in properties file, you don't need to recompile the java class. So, it makes the application easy to manage.
________________________________________



14) What does the hashCode() method?
The hashCode() method returns a hash code value (an integer number).
The hashCode() method returns the same integer number, if two keys (by calling equals() method) are same.
But, it is possible that two hash code numbers can have different or same keys.
________________________________________
15) Why we override equals() method?
The equals method is used to check whether two objects are same or not. It needs to be overridden if we want to check the objects based on property.
For example, Employee is a class that has 3 data members: id, name and salary. But, we want to check the equality of employee object on the basis of salary. Then, we need to override the equals() method.
________________________________________
16) How to synchronize List, Set and Map elements?
Yes, Collections class provides methods to make List, Set or Map elements as synchronized:
public static List synchronizedList(List l){}
public static Set synchronizedSet(Set s){}
public static SortedSetsynchronizedSortedSet(SortedSet s){}
public static Map synchronizedMap(Map m){}
public static SortedMapsynchronizedSortedMap(SortedMap m){}
________________________________________
17) What is the advantage of generic collection?
If we use generic class, we don't need typecasting. It is typesafe and checked at compile time.
________________________________________
18) What is hash-collision in Hashtable and how it is handled in Java?
Two different keys with the same hash value is known as hash-collision. Two different entries will be kept in a single hash bucket to avoid the collision.
________________________________________
19) What is the Dictionary class?
The Dictionary class provides the capability to store key-value pairs.
________________________________________
20) What is the default size of load factor in hashing based collection?
The default size of load factor is 0.75. The default capacity is computed as initial capacity * load factor. For example, 16 * 0.75 = 12. So, 12 is the default capacity of Map.


21) What is the difference between Array and ArrayList?

Array is a fixed length data structure whereas ArrayList is a variable length Collection class. We cannot change length of array once created in Java but ArrayList can be changed.
We cannot store primitives in ArrayList, it can only store objects. But array can contain both primitives and objects in Java. Since Java 5, primitives are automatically converted in objects which is known as auto-boxing.
importjava.util.*;

publicclassListExample {
	publicstaticvoid main(String[] args) {
		List<Integer>list = newArrayList<>();
		list.add(Integer.valueOf(10));// storing Integer object
		list.add(20);// Now compiler converts it into Integer.valueOf(20) which is object
		list.add(30);

		System.out.println("Traversing List...");
		for (Integer i : list) {
			System.out.println(i);
		}
	}
}


22) What is the difference between length of Array and size of ArrayList?
ArrayList doesn't have length() method, the size() method of ArrayList provides the number of objects available in the collection.
Array has length property which provides the length or capacity of the Array. It is the total space allocated during the intialization of the array.
importjava.util.ArrayList;

publicclassLengthVsSize {
	publicstaticvoid main(String[] args) {
		// creating array of 10 elements
		intarr[] = newint[10];
		// storing 2 elements
		arr[0] = 10;
		arr[1] = 12;
		// printing length of array
		System.out.println(arr.length);// 10

		// Creating ArrayList
		ArrayList<String>list = newArrayList<String>();
		// storing 2 elements
		list.add("ankit");
		list.add("nippun");
		// printing size of ArrayList
		System.out.println(list.size());// 2
	}
}


23) How to convert ArrayList to Array and Array to ArrayList?

publicclassLengthVsSizeArrayList {
	publicstaticvoid main(String[] args) {
		// creating Arraylist
		List<String>fruitList = newArrayList<>();
		// adding String Objects to fruitsListArrayList
		fruitList.add("Mango");
		fruitList.add("Banana");
		fruitList.add("Apple");
		fruitList.add("Strawberry");
		fruitList.add("Pineapple");
		System.out.println("Converting ArrayList to Array");
		String[] item = fruitList.toArray(new String[fruitList.size()]);
		for (String s : item) {
			System.out.println(s);
		}
		System.out.println("Converting Array to ArrayList");
		List<String>l2 = newArrayList<>();
		l2 = Arrays.asList(item);
		System.out.println(l2);
	}
}


24) How to make Java ArrayList Read-Only?
publicclassUnmodifiableArrayList {
	publicstaticvoid main(String[] args) {
		List<String>fruitList = newArrayList<String>();

		fruitList.add("Mango");
		fruitList.add("Banana");
		fruitList.add("Apple");
		fruitList.add("Strawberry");
		fruitList.add("Pineapple");

		List<String>unmodifiableList = Collections.unmodifiableList(fruitList);
		unmodifiableList.add("INDIA");
		System.out.println(fruitList);
	}
}


25) How to remove duplicates from ArrayList?
To remove dupliates from ArrayList, we can convert it into Set. Since Set doesn't contain duplicate elements, it will have only unique elements.

publicclassRemoveDuplicateArrayList {
	publicstaticvoid main(String[] args) {
		List<String>l = newArrayList<String>();
		l.add("Mango");
		l.add("Banana");
		l.add("Mango");
		l.add("Apple");
		System.out.println(l.toString());
		Set<String>s = newLinkedHashSet<String>(l);
		System.out.println(s);
	}
}


26) How to reverse ArrayList?
The reverse method of Collections class can be used to reverse any collection. It is a static method. Let's see the signature of reverse method:
public static void reverse(Collection c)  

Let's see a simple example to reverse ArrayList in Java:
publicclassReverseArrayList {
	publicstaticvoid main(String[] args) {
		List<String>l = newArrayList<String>();
		l.add("Mango");
		l.add("Banana");
		l.add("Mango");
		l.add("Apple");
		System.out.println("Before Reversing");
		System.out.println(l.toString());

		Collections.reverse(l);
		System.out.println("After Reversing");
		System.out.println(l);
	}
}


27) How to sort ArrayList in descending order?
By using Collections.reverseOrder(Comparator<T>cmp) method, we can sort the collection in reverse order. The reverseOrder() method does the reversing on the basis of given Comparator. In case of null, it will reverse collection in natural ordering.

SmartPhone.java
importjava.util.Comparator;

publicclassSmartPhone {
	String brand;
	String model;intprice;intrating;

	SmartPhone(String brand,Stringmodel,intprice,intrating){  
this.brand = brand;  
this.model = model;  
this.price = price;  
this.rating = rating;

    }

	public String getBrand() {  
returnbrand;  
    }

	publicvoidsetBrand(String brand) {
		this.brand = brand;
	}

	public String getModel() {  
returnmodel;  
    }

	publicvoidsetModel(String model) {
		this.model = model;
	}

	publicintgetPrice() {  
returnprice;  
    }

	publicvoidsetPrice(intprice) {  
this.price = price;  
    }

	publicintgetRating() {  
returnrating;  
    }

	publicvoidsetRating(intrating) {  
this.rating = rating;  
    }

	public String toString() {
		return"SmartPhone [brand=" + brand + ", model=" + model + ", price=" + price + ", rating=" + rating + "]";
	}

	publicintcompareTo(SmartPhonesp) {  
returnthis.price-sp.price;  

    }
}

classRatingComparatorimplements Comparator<SmartPhone> {
	@Override
	publicint compare(SmartPhoneobj1, SmartPhoneobj2) {
		return (obj1.rating<obj2.rating) ? -1 : (obj1.rating>obj2.rating) ? 1 : 0;
	}
}

ArrayListLearning.java
publicclassArrayListLearning {
	@SuppressWarnings("unchecked")
	publicstaticvoid main(String[] args) {

		List<SmartPhone>phoneList = newArrayList<>();
		SmartPhoneph1 = newSmartPhone("Apple", "6s", 50000, 10);
		SmartPhoneph2 = newSmartPhone("lg", "pro2", 40000, 9);
		SmartPhoneph3 = newSmartPhone("MI", "3s", 10000, 6);
		SmartPhoneph4 = newSmartPhone("Letv", "le2", 12000, 7);

		phoneList.add(ph1);
		phoneList.add(ph2);
		phoneList.add(ph3);
		phoneList.add(ph4);
		System.out.println("Actual List");
		System.out.println(phoneList);
		System.out.println("Sorting the list as comparator");
		Collections.sort(phoneList, newRatingComparator());

		System.out.println(phoneList);
		System.out.println("Reversing the Comparator sorting");
		Comparator<SmartPhone>cmp = Collections.reverseOrder(newRatingComparator());

		Collections.sort(phoneList, cmp);
		System.out.println("Printing the reverse list");
		System.out.println(phoneList);
	}

}


28) How to synchronize ArrayList?
We can use Collections.synchronizedList(List<T>) method to synchronize collections in java. The synchronizedList(List<T>) method is used to return a synchronized (thread-safe) list backed by the specified list.

importjava.util.*;  
publicclassSyncronizeArrayList {  
publicstaticvoid main(String args[]) {  
// Non Synchronized ArrayList
        List<String>fruitList = newArrayList<String>();  

fruitList.add("Mango");  
fruitList.add("Banana");  
fruitList.add("Apple");  
fruitList.add("Strawberry");  
fruitList.add("Pineapple");  

// Synchronizing ArrayList in Java  
furitList = Collections.synchronizedList(fruitList);  

// we must use synchronize block to avoid non-deterministic behavior  
synchronized (fruitList) {  
            Iterator<String>itr = fruitList.iterator();  
while (itr.hasNext()) {  
System.out.println(itr.next());  
            }  
        }  
    }  
}


29) When to use ArrayList and LinkedList?
ArrayList provides constant time for search operation, so it is better to use ArrayList if searching is more frequent operation than add and remove operation. The LinkedList provides constant time for add and remove operations. So it is better to use LinkedList for manipulation.
ArrayList has O(1) time complexity to access elements via the get and set methods.
LinkedList has O(n/2) time complexity to access the elements.
LinkedLinked class implements Deque interface also, so you can get the functionality of double ended queue in LinkedList. The ArrayList class doesn't implement Deque interface.
In sort, ArrayList is better to access data whereaseLinkedList is better to manipulate data. Both classes implements List interface.
ArrayList Example
importjava.util.*;

publicclassListExample {
	publicstaticvoid main(String[] args) {
		// ArrayList is better to store and view data
		List<String>list = newArrayList<>();
		list.add("ankit");
		list.add("peter");
		list.add("mayank");

		System.out.println("Traversing ArrayList...");
		for (String s : list) {
			System.out.println(s);
		}
	}
}

LinkedList Example
importjava.util.*;

publicclassListExample2 {
	publicstaticvoid main(String[] args) {
		// LinkedList is better to manipulate data
		List<String>list = newLinkedList<>();
		list.add("ankit");
		list.add("peter");
		list.add("mayank");
		System.out.println("After adding: " + list);
		list.remove("peter");
		System.out.println("After removing: " + list);
		list.set(1, "vivek");
		System.out.println("After changing: " + list);
	}
}

