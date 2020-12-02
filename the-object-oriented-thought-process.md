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

### Determining the Users

### Identifying the Public Interfaces

### Identifying the Implementation
