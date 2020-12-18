# The Object Oriented Thought Process

by Matt Weisfield

## Chapter 1: Introduction to Object Oriented Concepts 
- Objects and OO programing emerged with the rise of "Internet as a business" and entertainment platform, objects work well over a network.

### Fundamental Concepts

- Object oriented languages are defined by the following: 
- Polymorphism
- Encapsulation
	- Inheritance
- Composition (supplementary to the terms listed above)
	- Matt also considers composition to be another central component in OO programing languages

### Objects and Legacy Systems

**What Are the fundamental concepts of OO Programing?**
**What is an Object Wrapper?**
**What is an Object**
**What is the difference between procedural programing and OO programing?**
**What is the difference between procedural programing and OO programing?**

	- OO programing and procedural (structured) programming are complementary to one another and should be used in conjunction with one another

#### What is an Object Wrapper?
	- An object wrapper is OO code that contains (wraps around) structured code like loops and if statements to make it look and function like OO code. 

#### What is an Object?
	- At it's most basic definition, an object has both data and behavior (attributes and methods).

#### What is the process of procedural programing?
	- Procedural programing ideally consist of individual / distinct functions or processes in which data is placed into them and outputs come out.

#### What is the difference between procedural programing and OO programing?
	- In OO design, the data and the methods live on the same object, conversely with procedural, or structured, design the attributes and functions / behaviors are separated.
	- What are some benefits to switching to / using an OO model as opposed to structured?
	- There is no such thing as global data in an OO model. Which means there is amost a guarantee of data integrity
	- It is important in OO programing that one object does not change the attributes of another object. 
	- A good rule of thumb is to build small objects that do one task well as opposed to a large object that does many task.

### Moving from Procedural to Object-Oriented Development
**What is procedural programing?**
**What is the primary benifit to OO programing?**
**How is the state of the object represented?**

#### Procedural Programing 
	- procedural programing is the method of programing in which the data and the processes to manipulate that data are separated.

#### OO Programing 
	- The primary benefit of OO programing is that the data and the methods and operations that can and should manipulate that data are encapsulated in the same object
	- An example of an object being sent over an network would be a webapp / page. Browsers does not know what the app will be before hand and relies on the object (HTML/Javascrip/CSS) to build and run itself

### What Exactly is an Object?
**What is a getter and setter?**
**What is UML (Unified Modeling Language)**

#### Object Data 
	- the data stored within an object represents the sate of the object. Also called the objects attributes.

#### Object Behaviors
	- The behavior of an object outlines what an object can do.
	- Getters and setters are methods on an object that regulate access to object attributes. 
		- They are also called accessor and manipulators, respectivly 
	- The unified modeling language is used to help visualize and manipulate class diagrams.

### What Exactly is a Class?
	- Classes are what are used to create objects, they can be thought of as templates for how an object looks and functions.

**What is the difference between public and private members of a class?**
**What is an object message**

#### Attributes
	- public members can be accessed by any function or other object, while private members (attributes or methods) can only be accessed by the object itself.
	
#### Messages
	- Messages are typically how two objects communicate, generally, through methods. Object A will call a method on Object B and that is Object A's way of communicating and the return value of the method is the way Object B will communicate with A

### Using Class Diagrams as a Visual Tool
	- UML (Universal Modeling Language) is just a simple way to describe classes and object and how they interact with each other without being buried under the syntax of a particular language.

### Encapsulation and Data Hiding
**How is incapulation defined?**
**What is an interface?**

	- Encapsulation can be defined as the idea that objects contain (encapsulate) both their attributes and their methods / functions. With the intent that only the minimal number of which should be exposed to other objects.

#### Interfaces
	- Interfaces are how objects interact with each other. Typically through methods. In good oo design, attributes should be private. Only the public attributes and methods are considered the interface.

#### Implementations 
- Example of interface implementation  
	- Toaster <--> Electrical Outlet <--> PowerPlant
	- Object  <--> Interface         <--> Object

	- Square of a number:

``` Java 
public class IntSquare {

	// private attrubute
	private int squareValue;

	// public interface
	public intgetSquare (int value) {

		SquareValue = calculateSquare(value);

		return squareValue;

	}

	// private implimentation
	private intcalculatSquare (int value) {
		
		retrn value * value;

	}
}
```

### Inheritance

**What is inheritance?**
**What is a superclass?**
**What is abstraction?**
	- Inheritance is the ability of on class to inherit the attributes and methods of another class. 

#### Superclasses and Subclasses
	- A super class is a class from which other classes inherit from, that usually contain attributes and methods that pertain to more than one subclass.

#### Inheritance Abstraction
	- Abstraction is a large inheritance tree (more or less)

#### Is-a Relationships
	- A square "is a" shape
	- A Circle "is a" shape
	- A Star "is a " shape
	- a BLANK "is a" type of BLANK

### Polymorphism

**What is Polymorphism?**
**What is a benefit of polymorphism? (when used togeether)**
	- Polymorphism can be described as a superclass having a public method available to interface with, but requires that a subclass define what the method does. For example, a shape superclass might have and abstract function for an interface called "getArea()" but the implementation of that function should be defined on the circle class, square class, or star class that inherits from the shape class.
	- one benefit to inheritance and polymorphisms is that two different objects could be added to the same the stack if they inherit from the same superclass. Imagine the below has circle, square and star objects. we can reliably call the getArea() method on each.

``` Java
while ( !stack.empty()) {
	Shape shape = (Shape) stack.pop();
	System.out.println ("Area = " + shape.getArea());
}
```

### Composition

**What is Composition?**
	- Composition is the idea that objects are built or made up of other objects. 

#### Composition Abstraction

**What is abstraction?**
	- an object is built up of many other objects.

#### Has-a Relationship
	- While inheritance is considered an is-a relationship, a composition relationship is termed a has-a relationship.



## Chapter 2: How to Think in Terms Of Objects 

### Knowing the Difference Between Interface and the Implementation
**What is the difference between interface and implementation?**
- An interface is what the user of your class or object can interact with while the implementation is the method and details by which which the class produces its returned value.
- The interface should consistently return what the user expects even if the implementation changes.
- Implementation details should be kept hidden from the user
- (user in this context is other designers and developers not necessarily end users)
- A change to the implementation should not require a change to the users code.
**What is object persistence?**
- Object persistence is the concept of saving the state of an object for later use.

### Using Abstract Thinking When Designing Interfaces
**What is one of the main advantages of using 00 programing?**
- One of the main advantages of using OO programing is that classes can be reused. 
**What is the difference between an abstract and concrete user inteface?**
- Abstract interfaces are generally more usefull than concrete interfaces. Abstract interfaces tend to be more flexable and reuseable 
	- think: asking a taxi to "take me to the airport" ( abstract ) vs. "turn left, turn right, turn left.... " ( concrete )
	- I as the pasanger do not care about how the taxi gets me to the airport, just that is does.

### Prividing the Absolute Minimal User Interface Possible
- Provide as few interfaces as possible.
- Its better to add interfaces later at requests rather than adding a bunch up front 
- It is important to design the interface while taking the perspective of the end user
- Do not try and design from the information systems stand point.

#### Determining the Users
- Special care must be taken to ensure that all users of a particular class will be able to use the class. an iteritive approach to object design will be required and that is okay.

#### Identifying the Public Interfaces
- A good analogy to help identify what interfaces should be public: 
	- If we have an interface called enterTaxi(), we certainly do not want enterTaxi() to have logic in it to pay the cabbie. If we do this, not only is the design somewhat illogical, but there is virtually no way that a user of the class can tell what has to be done to pay the cabbie.

#### Identifying the Implementation
- The implimentation is the meat and potatoes of the object, ie the interior of the method that corresponds to the interface. The interface is how our users see and interact with the object.

## Chapter 3: More Object-Oriented Concepts

### Constructors
**What are constructors?**
- Constructors are used when initalizing an object from a class. they outline the initalizing attribues of the resulting object using the parameters (if any) that are passed into the the call to the class.
- When a new object is created on the the first things that happens is that the constructor is called.
- The code inside the constructor should set the object to its inital/safe/stable state.

**What is the default constuctor and when is it called?**
- regardless of if you as the programmer explicitly define a constructor. A constuctor is always called when a new object is instantiated, however the constructer that is called is named the "default constructor". usually, this default constructor only calls the supperclass of what ever programing language framework you are in, and then creates the object itself. This way, the "Object" class will be the parent class.

```java
public Cabbie() {
	super();
}
```

**What is overloading a method?**
- Overloading a method is when you use the same method name more than once but the parameter list is different every time.

**What is a method signature?**
- A method signature is the name of the method along with the parameter list.

### Error Handling
**What are four proposed ways errors can be handled?**

- the four options are: 
	- Ignore the problem. (bad)
	- Check for potential problems and abort the program when one is found.
	- Check for potential problems, fix the mistake, and attempt to fix the problem.
	- Throw an exception.

**What is an exception?**
 
- An exception is a flag thrown by the program when an unexpected event occurred / error occurs. 
	- If your program throws an exception, and cleanly catches it. it can still proceed without blowing up

### The Importance of Scope
**How many types of attributes are their?**
- There are three types of attrubutes:
	- Local Attributes - these are owned by a specific method
	- Object Attributes - these are attribues that are decalred at the class level and unique for every object that is instantiated.
	- Class Attributes - these are attributes that are delacred as static at the class level and is shared across every instance of object created from it. 

### Operator Overloading
**What is operator Overloading**
- Operator Overloading is when you assign different functions to well know operators.
	- for example: with strings the "+" symbol means to concatinate two independant strings into one string.

### Multiple Inheritance
**What is multiple inheritance?**
- Multiple inheritance is when a class ingerits from more than one class.
- not all programing languages allow for multiple ingeritance 
	- For example: java, SWIFT and .NET do not allow for multiple inheritance and the designers decided the increased complexity outweighed the benifits.

### Object Operations
**What is the diffrence between a shallow copy / shallow compairison as it relates to Objects?**
- when making a shallow copy of an object, only the first level of the object and its references / pointers are coppied, not the additional objects that are pointed to / referenced by the inital object. siularly when compairing two objects you should take care to understand if the operation is compairing justs the surface level object and references or the entire object tree.

## Chapter 4: The Anatomy of a Class

### The Name of the Class
**What important functions do the class name serve?**
- The class name helps the user of the class determine its function as well as how it fits in the overall structure of the program.
- The class name is also used whenever the class is instantiated.

### Comments
- It is important to remember that comments come in different flavors depending on the language: Multi-line and Single-line.

### Attributes
- Attributes are said to store the state of the object because at any given moment the object attributes represent the information that the object holds (It's state).
- Remember, you should atempt to keep as many attributes private as possible.

### Constructors
- Not coding a constructor / default constructor and relying on the constructor provided by the system is bad practice.

### Accessors
**What are accessor methods?**
- Accessor methods, sometimes called getters and setters are public class methods that either change / update (set) or returns (gets) a classes attribute.
- These are perferable to allowing direct access to class attributes themselves. it also narrows the scope if it turns out that a bug is tracked down to an errant value for an attribute
- In short, getters and setters are used to ensure a level of data integerity and security.

**What is a static attrubute or method?**
- the keyword static indicates that memory a method or attribute is only allocated once across however many instances of an object are instanciated. ie if the an object is defined and has a static attribute, when making changes to that static attribute, all other objects that came from the same class will have that static attribute updated as well

### Public Interface Methods
- Methods that can be accessed or called by other classes/objects

### Private Implementation Methods
- Methods that can't be accessed or called by other classes/objects

## Chapter 5: Class Design Guidelines

### Modeling Real-World Systems

### Identifying the Public Interfaces

### Designing Robust Constructors (and Perhaps Destructors)

### Designing Error Handling into a Class

### Designing with Reuse in Mind

### Designing with Extensibility in Mind

### Designing with Maintainability in Mind

### Using Object Persistence

