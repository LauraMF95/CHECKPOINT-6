# WHY DO WE USE CLASSES IN PYTHON?

Python, as an object-oriented programming language, employs objects to accomplish data operations. 
Python classes are responsible for the creation of such valuable items.

Python is a programming language that relies on object-oriented programming. Object-oriented 
programming (OOP) is a high-level programming language that uses objects, classes, and functions to 
create useful programmes.

## Python Classes Explained

In Python, a class is similar to a blueprint from which objects are constructed. Let’s use an 
automobile as an example to better understand the word. 

An automobile is a collection of various elements, such as an engine, wheels, and so on, rather than a 
single entity. The term “vehicle” refers to a “class,” while the terms “engine” and “wheels” refer to 
objects. 

A **class instance** is sometimes known as an object, and the process of producing this object is known 
as instantiation. Each class has objects with numerous arguments that can be used to conduct actions on 
data.

When creating a class, the following guidelines should be followed:

- **Single Responsibility Principle (SRP)**: According to the Single Responsibility Principle (SRP), a 
class should only have one purpose.

- **Open Closed Responsibility (OCP)**: The Open Closed Responsibility (OCP) states that the class is 
open to extension but not to source code modifications.

- **Liskov Substitution Responsibility (LSR)**: The Liskov Substitution Responsibility (LSR) asserts that objects created in the superclass can be replaced with objects created in the subclass.

- **Dependency Inversion Principle (DIP)**: The Dependency Inversion Principle (DIP) asserts that the upper class should be based on the lower class’s abstraction rather than its details.

- **Interface Segregation Principle (ISP)**: The Interface Segregation Principle (ISP) asserts that no 
section of the code should be dependent on a function that isn’t in use.

## Creating Classes in Python

Classes are sort of like templates in which objects are created. The syntax of a class is as follows:

```python
class class_name:
```

Here:

- ***class*** is the keyword for defining class.

- The **class_name** refers to the class name.

All of a class’s attributes are declared in a new local namespace, and the attributes can be any type 
of data or function.

A new class object with the same name as the class is established when it is formed. This class object 
is used to access the class’s different attributes and build new objects for it. 

Let’s look at the following example to understand this more clearly:

```python
class Student(object):
    def __init__(self, name, age, gender, level, grades=None):
        self.name = name
        self.age = age
        self.gender = gender
        self.level = level
        self.grades = grades or {}

    def setGrade(self, course, grade):
        self.grades[course] = grade

    def getGrade(self, course):
        return self.grades[course]

    def getGPA(self):
        return sum(self.grades.values())/len(self.grades)

john = Student("Silver", 12, "male", 6, {"math":3.3})
jane = Student("Amanda", 12, "female", 6, {"math":3.5})

print(Silver.getGPA())
print(Amanda.getGPA())
```

## Attributes and Methods in Class

Some functionalities are defined by specifying attributes in a class, which act as reservoirs for data 
and functions linked to those attributes. Methods are the names for the functions.

### Attributes

A class attribute refers to a Python variable that belongs to a class rather than a specific object. 
The class can be assigned to a variable. Object instantiation is the term for this. Using the dot 
operator, you’ll be able to access the characteristics included within the class.

### Methods

A method is a function that is “associated” with an object.

*In Python, a method is similar to a function, except that it is coupled with objects or classes*. 
Except for two important variations, methods and functions in Python are quite similar.

- The method is applied implicitly to the object for which it is invoked.

- Data included within the class is accessible to the procedure.

```python
class ClassName:
   def method_name():
   
      # Method_body
```

## Types of Classes in Python

In Python, there are different varieties of classes in which some are as follows.

### Python Abstract Class

An abstract method is a unique method that has a declaration but does not have a need for execution. A 
class with more than one abstract method is called an abstract class. 

Python does not have an abstract class by default, unlike most high-level languages. Instead, this 
language provides a module named ABC, which allows the creation of the abstract base class.  

Example:

```python
# Python program invoking a
# method using super()
 
import abc
from abc import ABC, abstractmethod
 
class R(ABC):
    def rk(self):
        print("Abstract Base Class")
 
class K(R):
    def rk(self):
        super().rk()
        print("Subclass ")
 
# Driver code
r = K()
r.rk()
```

### Python Concrete Class

Concrete classes only have concrete methods, but abstract classes can have both concrete and abstract 
methods. Although the concrete class implements abstract methods, the abstract base class can also do 
so by invoking the methods via superclass.

### Python Partial Class

A partial class can be used to create a new function that only applies a subset of the statements and 
keywords you supply it. You can use partial to create a new object by freezing a portion of your 
function’s statements and keywords. To implement this class, we can use the Functools package.

## The ***__init__()*** Function

Special functions are class functions that begin with the double underscore and are known as the init 
() function. The ***__init__()*** function is a specific function that is called whenever a new 
instance of a class is created.

The ***__init__*** method is the Python equivalent of the C++ constructor in an object-oriented 
approach. When an object is generated from a class, the ***__init__()*** function is invoked. The 
__init__ method is only used by the class to initialise the object’s attributes. It’s solely utilised 
in the classroom.

The ***__init__*** method, commonly known as constructors in Object-Oriented Programming (OOP), is used 
to initialise all variables.

The ***__init__*** method is reserved in Python classes and automatically called when an object is 
created using a class. It is used to initialise the class’s variables. It is equivalent to a 
constructor.

- Like every other method, the init method begins with the keyword **“def.”**

- The first parameter of this method, like any other method, is **“self,”** but in the case of init,    
**“self”** refers to a newly generated object. In contrast, in different methods, **“self”** refers to 
the current object or instance associated with that method.

- It is possible to add more parameters.

Example:

```python
# A Sample class with init method  
class Person:  
      
    # init method or constructor   
    def __init__(self, name):  
        self.name = name  
      
    # Sample Method   
    def say_hi(self):  
        print('Hello, my name is', self.name)  
      
p = Person('Josh')  
p.say_hi()
```

## Python Inheritance and Its Types

In Python, there are different inheritance forms depending on the inheritance pattern between a derived 
class and a base class. The following are some of the inheritance types available in Python:

- **Single inheritance**: Single inheritance is the sort of inheritance in which a class inherits only 
one base class.

- **Multiple inheritances**: Many inheritances refers to a situation in which a class inherits from 
multiple base classes. Python, unlike other languages, ultimately enables multiple inheritances. All of 
the base classes are listed as a comma-separated list inside brackets. 

- **Multilevel inheritance**: Multilevel inheritance is when a class inherits a base class, and then 
another class inherits this previously derived class, resulting in a parent-child relationship class 
structure. 

- **Hierarchical inheritance**: Hierarchical inheritance occurs when several derived classes inherit a 
single base class.

- **Hybrid inheritance**: Hybrid inheritance occurs when one or more of the inheritances mentioned 
above types are combined.

Example:

```python
class polygon:
  def __init__(self, length, breadth):
    self.length = length
    self.breadth = breadth
  def area(self):
    return self.length * self.breadth
  
class square(polygon):
   def __init__(self, side):
      polygon.__init__(self, side, side)
    
MySquare = square(3)
print(MySquare.area())
```

## Polymorphism in Python

Polymorphism is the terminology for having several forms. Polymorphism allows for the use of a single 
interface with several Python data types, classes, and inputs.
There are two types:

### Run-time Polymorphism

The process of resolving a call to an overridden method at run-time is known as run-time polymorphism. 
Method overriding is how run-time polymorphism is implemented in Python.

Method overriding enables us to change the implementation of a method declared in the parent class in 
the child class.

### Compile-time Polymorphism

The technique by which the call to the method is resolved at the time of compilation is known as 
compile-time polymorphism. Method overloading is used to implement compile-time polymorphism.

Using method overloading, one can implement the same functionality of the class with different 
parameters. However, Compile-time polymorphism is not supported in Python.

## Advantages of Using Classes in Python

- Using classes, It is much easier to maintain the data members and methods together and structured in 
one place.

- Grouping related functions and putting them in one location provides a ***clear structure*** to the 
entire code and improves readability. 

- Classes can also be used to ***override any standard operator***. 

- The usage of classes allows the ***code to be reused***, making the application more efficient.

## Conclusion

Classes are crucial for writing more comprehensive code that is not only efficient but also 
comprehensible.  Classes are usually used in beginner-level and advanced-level programs and reduce 
frequent errors.

# WHICH METHOD IS AUTOMATICALLY EXECUTED WHEN A CLASS IS INSTANTIATED?

Object instantiation is a fundamental concept in object-oriented programming that refers to the process 
of creating new objects from a class. This process involves using constructors, which are special 
methods that define how new objects are initialized. This article describes how to instantiate an 
object in Python and provides examples of how to create and use these objects in your code.

## Exploring Python's Class Constructors

A class constructor in Python is a special method that is executed when an object of a class is 
instantiated. It is used to initialize the attributes of the class. The constructor method in Python is 
called ***__init__()*** and it is defined within the class.

### How to Instantiate a Python Class

In order to accomplish this, we must perform class instantiation in Python by creating an instance of 
the class that invokes its constructor method. Here's an example of a simple class and how to 
instantiate an object of that class.

```python
class Recipe:
    def __init__(self, name, ingredients):
        self.name = name
        self.ingredients = ingredients

# Instantiate a Recipe object
my_recipe = Recipe("Spaghetti Bolognese", ["spaghetti", "tomato sauce", "ground beef"])

# Access the object's attributes
print("Recipe Name:", my_recipe.name)
print("Ingredients:", my_recipe.ingredients)
```

In the above example, the **Recipe** class has a constructor that sets the attributes **name** and 
**ingredients** for each new object that is instantiated. The **my_recipe** object is instantiated with 
the name "Spaghetti Bolognese" and a list of ingredients. The print statements will output **Recipe Name: Spaghetti Bolognese** and **Ingredients: ['spaghetti', 'tomato sauce', 'ground beef']**.

## Inheritance and Constructors in Python

In Python, constructors play a crucial role in class inheritance, allowing child classes to inherit and 
extend attributes and behaviors from parent classes.

### Constructor Inheritance Basics

Child classes inherit the constructor of their parent class, enabling them to reuse the initialization 
logic from the parent. For example:

```python
class Vehicle:
    def __init__(self, make, model):
        self.make = make
        self.model = model

class Car(Vehicle):
    def __init__(self, make, model, year):
        super().__init__(make, model)
        self.year = year
```

In this example, the Car class inherits from Vehicle and extends its attributes.

### Constructor Overriding

Child classes can also override the parent class's constructor to customize initialization:

```python
class Bike(Vehicle):
    def __init__(self, make, model, wheel_count):
        super().__init__(make, model)
        self.wheel_count = wheel_count
```

### Abstract Base Classes

Abstract base classes allow you to enforce initialization patterns across a class hierarchy. 

## Delving into Python's Process of Instantiating Objects

Instantiating an object, in Python, means creating an instance of a class. When you create an instance 
of a class, you instantiate the object. In Python, the process of instantiating objects involves 
creating and initializing objects.

To instantiate a Python class, you need to use the constructor method, which is the ***__init__()*** 
method. The constructor method initializes the attributes or properties of an object.

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

person1 = Person("John", 25)
print(person1.name)
print(person1.age)
```

In this example, we defined a class called **Person** with two attributes, **name** and **age**. We 
instantiated an object **person1** and passed two arguments to the constructor method. Finally, we 
printed the values of the name and age attributes.

In Python, instantiating objects is a powerful and flexible way to create objects with specific 
behaviors and attributes.

## Initializing Objects Using the __init__() Method

The ***__init__()*** method is used in Python classes to initialize newly-created objects. It is 
automatically called when an object is created using the class constructor.

Here's an example of a class with an ***__init__()*** method: 

```python
class Person:
    def __init__(self, name, age):
        self.name = name
        self.age = age

p1 = Person("Alice", 25)
print(p1.name)  ### Output Alice

print(p1.age)  ### Output 25
```

In this example, the **Person** class has an **init** method that takes two arguments: **name** and 
**age**. When you create a new **Person** object, you pass in values for these arguments, and the 
***__init__()*** method sets the corresponding instance variables.
You can also have optional or default arguments in the ***__init__()*** method.

## Customizing Python's Object Initialization

In Python, the ***__init__()*** method is called when an object of a class is created. It is used to 
initialize the attributes of the object. However, sometimes we may need to customize object 
initialization by specifying our own parameters. This can be achieved using the following methods:

### Creating Python Class without __init__()

One way to customize object initialization is to define a custom method that initializes the 
attributes. This method can take parameters which are used to set the values of the attributes. Here is 
an example:

```python
class Car:
    def set_values(self, make, model, year):
        self.make = make
        self.model = model
        self.year = year

my_car = Car()
my_car.set_values('Toyota', 'Camry', 2022)
print(my_car.make)  # Output: Toyota
```

In this example, we defined a custom method **set_values()** to initialize the attributes **make**, 
**model**, and **year**. We then called this method on an object of the **Car** class to set the 
attribute values.

### Creating Class with __init__()

Another way to customize object initialization is to use class-level attributes. These attributes can 
be set in the class definition and used to initialize the attributes of the object. Here is an example:

```python
class Car:
    make = ''
    model = ''
    year = 0

    def __init__(self):
        self.make = Car.make
        self.model = Car.model
        self.year = Car.year

my_car = Car()
my_car.make = 'Toyota'
my_car.model = 'Camry'
my_car.year = 2022
print(my_car.make)  # Output: Toyota
```

In this example, we defined **make, model, and year** as class-level attributes and set their default 
values to an empty string and 0. We then used these attributes to initialize the object's attributes in 
the ***__init__()*** method. We can later modify the attribute values of the object as in the previous 
example.

## Creating Python Class Object with Flexible Initializers

Object-oriented programming allows us to create objects with different properties. We can initialize an 
object with fixed properties or flexible properties by passing different arguments to the constructor. 
In Python, we can use the ***__init__()*** method to initialize an object with flexible properties.

```python
class Rectangle:
    def __init__(self, width, height):
        self.width = width
        self.height = height

rect = Rectangle(5, 10)
print(rect.width)   # Output: 5
print(rect.height)  # Output: 10
```

In the above example, we initialized the **Rectangle** object with fixed properties **width** and 
**height**. The object returned by the constructor will always have the same properties.

# WHICH ARE THE THREE API VERBS?

In the realm of REST API (Representational State Transfer Application Programming Interface), the 
utilization of HTTP verbs plays a fundamental role in determining how clients interact with resources. 
These HTTP methods, often referred to as HTTP verbs, are at the core of RESTful services.

## What Are HTTP Verbs?

HTTP verbs are a set of standardized HTTP methods used to specify the desired action to be performed on 
a resource. In REST API, these verbs are the means by which clients communicate their intentions to the 
server. The most commonly used HTTP verbs in REST API are:

1. **GET**: The GET method is used to request data from the server. It is a safe and idempotent 
operation, meaning it should not have any side effects on the server, and multiple identical GET 
requests should produce the same result.

2. **POST**: POST is employed to create a new resource on the server. When a client sends a POST 
request, it typically includes data in the request body that the server uses to create a new resource.

3. **PUT**: The PUT method is used to update an existing resource on the server. It requires the client 
to send the entire representation of the resource, even if only a small part of it is being modified.

4. **DELETE**: DELETE is used to remove a resource from the server. When a client sends a DELETE request, it instructs the server to eliminate the specified resource.

## The Role of HTTP Verbs in Resource Manipulation

HTTP verbs play a vital role in how resources are managed within a REST API. By mapping these verbs to 
specific actions, you can perform various operations on resources:

1. Retrieval: GET is used to retrieve data from a resource, allowing clients to access information.

2. Creation: POST is utilized to create new resources, whether they are new user accounts, products, or 
any other data entity.

3. Update: PUT is employed to update existing resources, ensuring that the server-side resource is 
entirely replaced with the provided representation.

4. Deletion : DELETE facilitates the removal of resources, keeping the API clean and well-organized.

## Idempotency and Safety

Two important concepts related to HTTP verbs in REST API are idempotency and safety.

1. **Idempotency**: An operation is idempotent if performing it multiple times has the same effect as 
performing it once. GET is inherently idempotent, while PUT and DELETE can be idempotent if designed 
properly. POST, on the other hand, is not idempotent, as creating a new resource each time will have a 
different effect.

2. **Safety**: A safe operation is one that does not modify the state of the server. GET is considered 
a safe operation, as it does not change anything on the server. However, POST, PUT, and DELETE are not 
safe, as they can alter server state.

## Conclusion

HTTP verbs are the building blocks of REST API interactions. They define the actions that clients can 
perform on resources and play a crucial role in ensuring proper resource management. Understanding the 
semantics of these verbs, as well as their idempotent and safe characteristics, is fundamental in 
designing effective and predictable RESTful APIs.

# IS MONGODB A SQL OR A NOSQL DATABASE?

**MongoDB** is an open source **NoSQL** database management program. NoSQL (Not only SQL) is used as an 
alternative to traditional relational databases. NoSQL databases are quite useful for working with 
large sets of distributed data. MongoDB is a tool that can manage document-oriented information, store 
or retrieve information.

MongoDB is used for high-volume data storage, helping organizations store large amounts of data while 
still performing rapidly. Organizations also use MongoDB for its ad-hoc queries, indexing, load 
balancing, aggregation, server-side JavaScript execution and other features.

Structured Query Language (SQL) is a standardized programming language that is used to manage 
relational databases. SQL normalizes data as schemas and tables, and every table has a fixed structure.

Instead of using tables and rows as in relational databases, as a NoSQL database, the MongoDB 
architecture is made up of collections and documents. Documents are made up of Key-value pairs -- 
MongoDB's basic unit of data. Collections, the equivalent of SQL tables, contain document sets. MongoDB 
offers support for many programming languages, such as C, C++, C#, Go, Java, Python, Ruby and Swift.

## How does MongoDB work?

MongoDB environments provide users with a server to create databases with MongoDB. MongoDB stores data 
as records that are made up of collections and documents.

Documents contain the data the user wants to store in the MongoDB database. Documents are composed of 
field and value pairs. They are the basic unit of data in MongoDB. The documents are similar to 
JavaScript Object Notation (JSON) but use a variant called Binary JSON (BSON). The benefit of using 
BSON is that it accommodates more data types. The fields in these documents are like the columns in a 
relational database. Values contained can be a variety of data types, including other documents, arrays 
and arrays of documents, according to the MongoDB user manual. Documents will also incorporate a 
primary key as a unique identifier. A document's structure is changed by adding or deleting new or 
existing fields.

Sets of documents are called collections, which function as the equivalent of relational database 
tables. Collections can contain any type of data, but the restriction is the data in a collection 
cannot be spread across different databases. Users of MongoDB can create multiple databases with 
multiple collections.

The mongo shell is a standard component of the open-source distributions of MongoDB. Once MongoDB is 
installed, users connect the mongo shell to their running MongoDB instances. The mongo shell acts as an 
interactive JavaScript interface to MongoDB, which allows users to query or update data and conduct 
administrative operations.

A binary representation of JSON-like documents is provided by the BSON document storage and data 
interchange format. Automatic sharding is another key feature that enables data in a MongoDB collection 
to be distributed across multiple systems for horizontal scalability, as data volumes and throughput 
requirements increase.

The NoSQL DBMS uses a single master architecture for data consistency, with secondary databases that 
maintain copies of the primary database. Operations are automatically replicated to those secondary 
databases for automatic failover.

## Why is MongoDB used?

An organization might want to use MongoDB for the following:

- **Storage**: MongoDB can store large structured and unstructured data volumes and is scalable 
vertically and horizontally. Indexes are used to improve search performance. Searches are also done by 
field, range and expression queries.

- **Data integration**: This integrates data for applications, including for hybrid and multi-cloud 
applications.

- **Complex data structures descriptions**: Document databases enable the embedding of documents to 
describe nested structures (a structure within a structure) and can tolerate variations in data.

- **Load balancing**: MongoDB can be used to run over multiple servers.

## Features of MongoDB

- **Replication**: A replica set is two or more MongoDB instances used to provide high availability. 
Replica sets are made of primary and secondary servers. The primary MongoDB server performs all the 
read and write operations, while the secondary replica keeps a copy of the data. If a primary replica 
fails, the secondary replica is then used.

- **Scalability**: MongoDB supports vertical and horizontal scaling. Vertical scaling works by adding 
more power to an existing machine, while horizontal scaling works by adding more machines to a user's 
resources.

- **Load balancing**: MongoDB handles load balancing without the need for a separate, dedicated load 
balancer, through either vertical or horizontal scaling.


- **Schema-less**: MongoDB is a schema-less database, which means the database can manage data without 
the need for a blueprint.

- **Document**: Data in MongoDB is stored in documents with key-value pairs instead of rows and 
columns, which makes the data more flexible when compared to SQL databases.
 
## Advantages of MongoDB

- **Schema-less**: Like other NoSQL databases, MongoDB doesn't require predefined schemas. It stores 
any type of data. This gives users the flexibility to create any number of fields in a document, making 
it easier to scale MongoDB databases compared to relational databases.

- **Document-oriented**: One of the advantages of using documents is that these objects map to native 
data types in several programming languages., Having embedded documents also reduces the need for 
database joins, which can lower costs.

- **Scalability**: A core function of MongoDB is its horizontal scalability, which makes it a useful 
database for companies running big data applications. In addition, sharding lets the database 
distribute data across a cluster of machines. MongoDB also supports the creation of zones of data based 
on a shard key.

- **Third-party support**: MongoDB supports several storage engines and provides pluggable storage 
engine APIs that let third parties develop their own storage engines for MongoDB.

- **Aggregation**: The DBMS also has built-in aggregation capabilities, which lets users run MapReduce 
code directly on the database rather than running MapReduce on Hadoop. MongoDB also includes its own 
file system called GridFS, akin to the Hadoop Distributed File System. The use of the file system is 
primarily for storing files larger than BSON's size limit of 16 MB per document. These similarities let 
MongoDB be used instead of Hadoop, though the database software does integrate with Hadoop, Spark and 
other data processing frameworks.

## Disadvantages of MongoDB

- **Continuity**: With its automatic failover strategy, a user sets up just one master node in a 
MongoDB cluster. If the master fails, another node will automatically convert to the new master. This 
switch promises continuity, but it isn't instantaneous -- it can take up to a minute. By comparison, 
the Cassandra NoSQL database supports multiple master nodes. If one master goes down, another is 
standing by, creating a highly available database infrastructure.

- **Write limits**: MongoDB's single master node also limits how fast data can be written to the 
database. Data writes must be recorded on the master, and writing new information to the database is 
limited by the capacity of that master node.

- **Data consistency**: MongoDB doesn't provide full referential integrity through the use of 
foreign-key constraints, which could affect data consistency.

-  **Security**: In addition, user authentication isn't enabled by default in MongoDB databases. 
However, malicious hackers have targeted large numbers of unsecured MongoDB systems in attacks, which 
led to the addition of a default setting that blocks networked connections to databases if they haven't 
been configured by a database administrator.

## MongoDB vs. RDBMS: What are the differences?

A relational database management system (RDBMS) is a collection of programs and capabilities that let 
IT teams and others create, update, administer and otherwise interact with a relational database. 
RDBMSes store data in the form of tables and rows. Although it is not necessary, RDBMS most commonly 
uses SQL.

One of the main differences between MongoDB and RDBMS is that RDBMS is a relational database while 
MongoDB is nonrelational. Likewise, while most RDBMS systems use SQL to manage stored data, MongoDB 
uses BSON for data storage -- a type of NoSQL database.

While RDBMS uses tables and rows, MongoDB uses documents and collections. In RDBMS a table -- the 
equivalent to a MongoDB collection -- stores data as columns and rows. Likewise, a row in RDBMS is the 
equivalent of a MongoDB document but stores data as structured data items in a table. A column denotes 
sets of data values, which is the equivalent to a field in MongoDB.

MongoDB is also better suited for hierarchical storage.

## MongoDB platforms

MongoDB is available in community and commercial versions through vendor MongoDB Inc. MongoDB Community 
Edition is the open source release, while MongoDB Enterprise Server brings added security features, an 
in-memory storage engine, administration and authentication features, and monitoring capabilities 
through Ops Manager.

A graphical user interface (GUI) named MongoDB Compass gives users a way to work with document 
structure, conduct queries, index data and more. The MongoDB Connector for BI lets users connect the 
NoSQL database to their business intelligence tools to visualize data and create reports using SQL 
queries.

Following in the footsteps of other NoSQL database providers, MongoDB Inc. launched a cloud database as 
a service named MongoDB Atlas in 2016. Atlas runs on AWS, Microsoft Azure and Google Cloud Platform. 
Later, MongoDB released a platform named Stitch for application development on MongoDB Atlas, with 
plans to extend it to on-premises databases.

The company also added support for multi-document atomicity, consistency, isolation, and durability 
(ACID) transactions as part of MongoDB 4.0 in 2018. Complying with the ACID properties across multiple 
documents expands the types of transactional workloads that MongoDB can handle with guaranteed accuracy 
and reliability.

# WHAT IS AN API?

An **application programming interface (API)** is a way for two or more computer programs or components 
to communicate with each other. It is a type of software interface, offering a service to other pieces 
of software. A document or standard that describes how to build or use such a connection or interface 
is called an API specification. A computer system that meets this standard is said to implement or 
expose an API. The term API may refer either to the specification or to the implementation. Whereas a 
system's user interface dictates how its end-users interact with the system in question, its API 
dictates how to write code that takes advantage of that system's capabilities.

In contrast to a user interface, which connects a computer to a person, an application programming 
interface connects computers or pieces of software to each other. It is not intended to be used 
directly by a person (the end user) other than a computer programmer who is incorporating it into the 
software. An API is often made up of different parts which act as tools or services that are available 
to the programmer. A program or a programmer that uses one of these parts is said to call that portion 
of the API. The calls that make up the API are also known as subroutines, methods, requests, or 
endpoints. An API specification defines these calls, meaning that it explains how to use or implement 
them.

One purpose of APIs is to hide the internal details of how a system works, exposing only those parts 
that a programmer will find useful, and keeping them consistent even if the internal details change 
later. An API may be custom-built for a particular pair of systems, or it may be a shared standard 
allowing interoperability among many systems.

There are APIs for programming languages, software libraries, computer operating systems, and computer 
hardware. APIs originated in the 1940s, though the term did not emerge until the 1960s and 1970s. 
Contemporary usage of the term API often refers to web APIs, which allow communication between 
computers that are joined by the internet. Recent developments in APIs have led to the rise in 
popularity of microservices, which are loosely coupled services accessed through public APIs.

## Purpose

In building applications, an API simplifies programming by abstracting the underlying implementation 
and only exposing objects or actions the developer needs. While a graphical interface for an email 
client might provide a user with a button that performs all the steps for fetching and highlighting new 
emails, an API for file input/output might give the developer a function that copies a file from one 
location to another without requiring that the developer understand the file system operations 
occurring behind the scenes.

## History of the term

The term API initially described an interface only for end-user-facing programs, known as application 
programs. This origin is still reflected in the name "application programming interface." Today, the 
term is broader, including also utility software and even hardware interfaces.

### 1940s and 50s

The idea of the API is much older than the term itself. British computer scientists Maurice Wilkes and 
David Wheeler worked on a modular software library in the 1940s for EDSAC, an early computer. The 
subroutines in this library were stored on punched paper tape organized in a filing cabinet. This 
cabinet also contained what Wilkes and Wheeler called a "library catalog" of notes about each 
subroutine and how to incorporate it into a program. Today, such a catalog would be called an API (or 
an API specification or API documentation) because it instructs a programmer on how to use (or "call") 
each subroutine that the programmer needs.

Wilkes and Wheeler's 1951 book The Preparation of Programs for an Electronic Digital Computer contains 
the first published API specification. Joshua Bloch considers that Wilkes and Wheeler "latently 
invented" the API because it is more of a concept that is discovered than invented.

### 1960s and 70s

The term "application program interface" (without an ‑ing suffix) is first recorded in a paper called 
Data structures and techniques for remote computer graphics presented at an AFIPS conference in 1968. 
The authors of this paper use the term to describe the interaction of an application—a graphics program 
in this case—with the rest of the computer system. A consistent application interface (consisting of 
Fortran subroutine calls) was intended to free the programmer from dealing with idiosyncrasies of the 
graphics display device, and to provide hardware independence if the computer or the display were 
replaced.

The term was introduced to the field of databases by C. J. Date in a 1974 paper called The Relational 
and Network Approaches: Comparison of the Application Programming Interface. An API became a part of 
the ANSI/SPARC framework for database management systems. This framework treated the application 
programming interface separately from other interfaces, such as the query interface. Database 
professionals in the 1970s observed these different interfaces could be combined; a sufficiently rich 
application interface could support the other interfaces as well.

This observation led to APIs that supported all types of programming, not just application programming.

### 1990s

By 1990, the API was defined simply as "a set of services available to a programmer for performing 
certain tasks" by technologist Carl Malamud.

The idea of the API was expanded again with the dawn of remote procedure calls and web APIs. As 
computer networks became common in the 1970s and 1980s, programmers wanted to call libraries located 
not only on their local computers but on computers located elsewhere. These remote procedure calls were 
well supported by the Java language in particular. In the 1990s, with the spread of the internet, 
standards like CORBA, COM, and DCOM competed to become the most common way to expose API services.

### 2000s

Roy Fielding's dissertation Architectural Styles and the Design of Network-based Software Architectures 
at UC Irvine in 2000 outlined Representational state transfer (REST) and described the idea of a 
"network-based Application Programming Interface" that Fielding contrasted with traditional 
"library-based" APIs. XML and JSON web APIs saw widespread commercial adoption beginning in 2000 and 
continuing as of 2022. The web API is now the most common meaning of the term API.

The Semantic Web proposed by Tim Berners-Lee in 2001 included "semantic APIs" that recasts the API as 
an open, distributed data interface rather than a software behavior interface. Proprietary interfaces 
and agents became more widespread than open ones, but the idea of the API as a data interface took 
hold. Because web APIs are widely used to exchange data of all kinds online, API has become a broad 
term describing much of the communication on the internet. When used in this way, the term API has 
overlap in meaning with the term communication protocol.

## Usage

### Libraries and frameworks

The interface to a software library is one type of API. The API describes and prescribes the "expected behavior" (a specification) while the library is an "actual implementation" of this set of rules.

A single API can have multiple implementations (or none, being abstract) in the form of different libraries that share the same programming interface.

The separation of the API from its implementation can allow programs written in one language to use a 
library written in another. For example, because Scala and Java compile to compatible bytecode, Scala 
developers can take advantage of any Java API.

API use can vary depending on the type of programming language involved. An API for a procedural 
language such as Lua could consist primarily of basic routines to execute code, manipulate data or 
handle errors while an API for an object-oriented language, such as Java, would provide a specification 
of classes and its class methods. Hyrum's law states that "With a sufficient number of users of an API, 
it does not matter what you promise in the contract: all observable behaviors of your system will be 
depended on by somebody." Meanwhile, several studies show that most applications that use an API tend 
to use a small part of the API.

Language bindings are also APIs. By mapping the features and capabilities of one language to an 
interface implemented in another language, a language binding allows a library or service written in 
one language to be used when developing in another language.

Tools such as SWIG and F2PY, a Fortran-to-Python interface generator, facilitate the creation of such 
interfaces.

An API can also be related to a software framework: a framework can be based on several libraries 
implementing several APIs, but unlike the normal use of an API, the access to the behavior built into 
the framework is mediated by extending its content with new classes plugged into the framework itself.

Moreover, the overall program flow of control can be out of the control of the caller and in the 
framework's hands by inversion of control or a similar mechanism.

### Operating systems

An API can specify the interface between an application and the operating system. POSIX, for example, 
provides a set of common API specifications that aim to enable an application written for a POSIX 
conformant operating system to be compiled for another POSIX conformant operating system.

Linux and Berkeley Software Distribution are examples of operating systems that implement the POSIX APIs.

Microsoft has shown a strong commitment to a backward-compatible API, particularly within its Windows 
API (Win32) library, so older applications may run on newer versions of Windows using an 
executable-specific setting called "Compatibility Mode".

An API differs from an application binary interface (ABI) in that an API is source code based while an 
ABI is binary based. For instance, POSIX provides APIs while the Linux Standard Base provides an ABI.

### Remote APIs

Remote APIs allow developers to manipulate remote resources through protocols, specific standards for 
communication that allow different technologies to work together, regardless of language or platform. 
For example, the Java Database Connectivity API allows developers to query many different types of 
databases with the same set of functions, while the Java remote method invocation API uses the Java 
Remote Method Protocol to allow invocation of functions that operate remotely but appear local to the 
developer.

Therefore, remote APIs are useful in maintaining the object abstraction in object-oriented programming; 
a method call, executed locally on a proxy object, invokes the corresponding method on the remote 
object, using the remoting protocol, and acquires the result to be used locally as a return value.

A modification of the proxy object will also result in a corresponding modification of the remote 
object. 

### Web APIs

Web APIs are a service accessed from client devices (mobile phones, laptops, etc.) to a web server 
using the Hypertext Transfer Protocol (HTTP). Client devices send a request in the form of an HTTP 
request, and are met with a response message usually in JavaScript Object Notation (JSON) or Extensible 
Markup Language (XML) format. Developers typically use Web APIs to query a server for a specific set of 
data from that server.

An example might be a shipping company API that can be added to an eCommerce-focused website to 
facilitate ordering shipping services and automatically include current shipping rates, without the 
site developer having to enter the shipper's rate table into a web database. While "web API" 
historically has been virtually synonymous with web service, the recent trend (so-called Web 2.0) has 
been moving away from Simple Object Access Protocol (SOAP) based web services and service-oriented 
architecture (SOA) towards more direct representational state transfer (REST) style web resources and 
resource-oriented architecture (ROA). Part of this trend is related to the Semantic Web movement toward 
Resource Description Framework (RDF), a concept to promote web-based ontology engineering technologies. 
Web APIs allow the combination of multiple APIs into new applications known as mashups.

In the social media space, web APIs have allowed web communities to facilitate sharing content and data 
between communities and applications. In this way, content that is created in one place dynamically can 
be posted and updated to multiple locations on the web. For example, Twitter's REST API allows 
developers to access core Twitter data and the Search API provides methods for developers to interact 
with Twitter Search and trends data.

## Design

The design of an API has a significant impact on its usage. First of all, the design of programming 
interfaces represents an important part of software architecture, the organization of a complex piece 
of software. The principle of information hiding describes the role of programming interfaces as 
enabling modular programming by hiding the implementation details of the modules so that users of 
modules need not understand the complexities inside the modules. Aside from the previous underlying 
principle, other metrics for measuring the usability of an API may include properties such as 
functional efficiency, overall correctness, and learnability for novices. One straightforward and 
commonly adopted way of designing APIs is to follow Nielsen's heuristic evaluation guidelines. The 
Factory method pattern is also typical in designing APIs due to their reusable nature. Thus, the design 
of an API attempts to provide only the tools a user would expect.

### Synchronous versus asynchronous

An application programming interface can be synchronous or asynchronous. A synchronous API call is a 
design pattern where the call site is blocked while waiting for the called code to finish. With an 
asynchronous API call, however, the call site is not blocked while waiting for the called code to 
finish, and instead the calling thread is notified when the reply arrives.

## Security

API security is very critical when developing a public facing API. Common threats include SQL 
injection, Denial-of-service attack (DoS), broken authentication, and exposing sensitive data. Without 
ensuring proper security practices, bad actors can get access to information they should not have or 
even gain privileges to make changes to your server. Some common security practices include proper 
connection security using HTTPS, content security to mitigate data injection attacks, and requiring an 
API key to use your service. Many public facing API services require you to use an assigned API key, 
and will refuse to serve data without sending the key with your request.

## Release policies

APIs are one of the more common ways technology companies integrate. Those that provide and use APIs 
are considered as being members of a business ecosystem.

The main policies for releasing an API are:

- **Private**: The API is for internal company use only.

- **Partner**: Only specific business partners can use the API. For example, vehicle for hire companies 
such as Uber and Lyft allow approved third-party developers to directly order rides from within their 
apps. This allows the companies to exercise quality control by curating which apps have access to the 
API and provides them with an additional revenue stream.
 
- **Public**: The API is available for use by the public. For example, Microsoft makes the Windows API 
public, and Apple releases its API Cocoa so that software can be written for their platforms. Not all 
public APIs are generally accessible by everybody. For example, Internet service providers like 
Cloudflare or Voxility, use RESTful APIs to allow customers and resellers access to their 
infrastructure information, DDoS stats, network performance, or dashboard controls. Access to such APIs 
is granted either by "API tokens", or customer status validations.

## Public API implications

An important factor when an API becomes public is its "interface stability". Changes to the API—for 
example adding new parameters to a function call—could break compatibility with the clients that depend 
on that API.

When parts of a publicly presented API are subject to change and thus not stable, such parts of a 
particular API should be documented explicitly as "unstable". For example, in the Google Guava library, 
the parts that are considered unstable, and that might change soon, are marked with the Java annotation 
@Beta.

A public API can sometimes declare parts of itself as deprecated or rescinded. This usually means that 
part of the API should be considered a candidate for being removed, or modified in a backward 
incompatible way. Therefore, these changes allow developers to transition away from parts of the API 
that will be removed or not supported in the future.

On February 19, 2020, Akamai published their annual "State of the Internet" report, showcasing the 
growing trend of cybercriminals targeting public API platforms at financial services worldwide. From 
December 2017 through November 2019, Akamai witnessed 85.42 billion credential violation attacks. About 
20%, or 16.55 billion, were against hostnames defined as API endpoints. Of these, 473.5 million have 
targeted financial services sector organizations.

## Documentation

API documentation describes the services an API offers and how to use those services, aiming to cover 
everything a client would need to know for practical purposes.

Documentation is crucial for the development and maintenance of applications using the API.[52] API 
documentation is traditionally found in documentation files but can also be found in social media such 
as blogs, forums, and Q&A websites.

Traditional documentation files are often presented via a documentation system, such as Javadoc or 
Pydoc, that has a consistent appearance and structure. However, the types of content included in the 
documentation differ from API to API.

In the interest of clarity, API documentation may include a description of classes and methods in the 
API as well as "typical usage scenarios, code snippets, design rationales, performance discussions, and 
contracts", but implementation details of the API services themselves are usually omitted.

Reference documentation for a REST API can be generated automatically from an OpenAPI document, which 
is a machine-readable text file that uses a prescribed format and syntax defined in the OpenAPI 
Specification. The OpenAPI document defines basic information such as the API's name and description, 
as well as describing operations the API provides access to.

API documentation can be enriched with metadata information like Java annotations. This metadata can be 
used by the compiler, tools, and by the run-time environment to implement custom behaviors or custom 
handling.

## Dispute over copyright protection for APIs

In 2010, Oracle Corporation sued Google for having distributed a new implementation of Java embedded in 
the Android operating system. Google had not acquired any permission to reproduce the Java API, 
although permission had been given to the similar OpenJDK project. Google had approached Oracle to 
negotiate a license for their API, but were turned down due to trust issues. Despite the disagreement, 
Google chose to use Oracle's code anyway. Judge William Alsup ruled in the Oracle v. Google case that 
APIs cannot be copyrighted in the U.S and that a victory for Oracle would have widely expanded 
copyright protection to a "functional set of symbols" and allowed the copyrighting of simple software 
commands.

To accept Oracle's claim would be to allow anyone to copyright one version of code to carry out a 
system of commands and thereby bar all others from writing its different versions to carry out all or 
part of the same commands.

Alsup's ruling was overturned in 2014 on appeal to the Court of Appeals for the Federal Circuit, though 
the question of whether such use of APIs constitutes fair use was left unresolved.

In 2016, following a two-week trial, a jury determined that Google's reimplementation of the Java API 
constituted fair use, but Oracle vowed to appeal the decision. Oracle won on its appeal, with the Court 
of Appeals for the Federal Circuit ruling that Google's use of the APIs did not qualify for fair use. 
In 2019, Google appealed to the Supreme Court of the United States over both the copyrightability and 
fair use rulings, and the Supreme Court granted review. Due to the COVID-19 pandemic, the oral hearings 
in the case were delayed until October 2020.

The case was decided by the Supreme Court in Google's favor with a ruling of 6–2. Justice Stephen 
Breyer delivered the opinion of the court and at one point mentioned that "The declaring code is, if 
copyrightable at all, further than are most computer programs from the core of copyright." This means 
the code used in APIs are more similar to dictionaries than novels in terms of copyright protection.

## Examples

- ASPI for SCSI device interfacing
- Cocoa and Carbon for the Macintosh
- DirectX for Microsoft Windows
- Ark Engine for HarmonyOS
- EHLLAPI
- Java APIs
- ODBC for Microsoft Windows
- OpenAL cross-platform sound API
- OpenCL cross-platform API for general-purpose computing for CPUs & GPUs
- OpenGL cross-platform graphics API
- OpenMP API that supports multi-platform shared memory multiprocessing programming in C, C++, and 
Fortran on many architectures, including Unix and Microsoft Windows platforms.
- Server application programming interface (SAPI)
- Simple DirectMedia Layer (SDL)

# WHAT IS POSTMAN?

Postman is an API(application programming interface) development tool that helps to build, test and 
modify APIs. Almost any functionality that could be needed by any developer is encapsulated in this 
tool. It is used by over 5 million developers every month to make their API development easy and 
simple. It has the ability to make various types of HTTP requests(GET, POST, PUT, PATCH), save 
environments for later use, converting the API to code for various languages(like JavaScript, and 
Python). 

The software was created in 2012 by Abhinav Asthana, Ankit Sobti and Abhijit Kane in Bangalore, India 
in order to solve the API tests sharing problem. Originally, it was developed as a plugin for Google 
Chrome, then a rich client, and finally a thin client. It's now used by more than 500,000 companies 
worldwide. The developer, Postman Inc., originally from India, has its headquarters in San Francisco.

## Introduction to Postman for API Development

Postman stands as an indispensable tool for modern API development, offering a range of features that 
streamline the development process. Here are key aspects that make Postman a powerful ally in the realm 
of API development:

- **Versatile Request Methods**: Postman supports an array of HTTP request methods, encompassing GET, 
POST, PUT, DELETE, and PATCH. This versatility allows developers to interact comprehensively with APIs.

- **Flexible Request Body Formats**: Developers benefit from the flexibility of handling various 
request body formats, including form-data, URL-encoded data, raw data, and binary data. This 
adaptability caters to the diverse requirements of different APIs.

- **Authentication Simplified**: Postman simplifies the intricacies of authentication by providing 
support for various methods such as API keys, OAuth, and Basic Auth. This streamlines the process of 
securing API interactions, ensuring a robust and secure development environment.
 
- **Organized API Testing**: Collections in Postman serve as a powerful organizational tool, allowing 
developers to categorize and manage API requests efficiently. This organized structure facilitates 
seamless sharing and collaboration within development teams. Moreover, the platform enables the 
automation of testing through the use of JavaScript, enhancing the efficiency of the testing process.

- **Efficient Documentation**: Postman excels in the generation of API documentation directly from 
requests and collections. This feature provides a streamlined and centralized approach to documenting 
APIs, benefiting both internal development teams and external stakeholders. The documentation process 
is efficient, ensuring clarity and accessibility.

In essence, Postman transforms the API development landscape by combining versatility, flexibility, 
simplicity, and efficiency. Whether it’s interacting with APIs, handling authentication, organizing 
tests, or generating documentation, Postman offers a comprehensive suite of tools tailored to meet the 
demands of modern software development

## Features

Postman regroups API tests in collections, to mutualize their URLs and authentications. It includes:

- A free version with workspace sharing to three users maximum.

- Variables depending on the selected environment.

- A version control system of tests and environments.
 
- Access rights per roles (user or editor).

- Benchmarks.

- Importation and exportation in JSON.
 
- Tests exportation to various HTTP clients formats (cURL, PHP, Python, Java, Node.js...).

- Authentication by JSON Web Token (with possible OAuth2 configuration).

- REST, SOAP, GraphQL, and gRPC.

- A rich client.

- A thin client allowing to upload files to send to APIs.
 
- A debugging console which keeps previous requests and responses calls in memory .

- Scripts to automatize tests.

# WHAT IS POLYMORPHISM?

The literal meaning of polymorphism is the condition of occurrence in different forms.

Polymorphism is a very important concept in programming. It refers to the use of a single type entity 
(method, operator or object) to represent different types in different scenarios.

Let's take an example:

## Example 1: Polymorphism in addition operator

We know that the "+" operator is used extensively in Python programs. But, it does not have a single 
usage.

For integer data types, "+" operator is used to perform arithmetic addition operation.

```python
num1 = 1
num2 = 2
print(num1+num2)
```

Hence, the above program outputs 3.

Similarly, for string data types, "+" operator is used to perform concatenation.

```python
str1 = "Python"
str2 = "Programming"
print(str1+" "+str2)
```

As a result, the above program outputs Python Programming.

Here, we can see that a single operator "+" has been used to carry out different operations for 
distinct data types. This is one of the most simple occurrences of polymorphism in Python.

## Function Polymorphism in Python

There are some functions in Python which are compatible to run with multiple data types.

One such function is the len() function. It can run with many data types in Python. Let's look at some 
example use cases of the function.

### Example 2: Polymorphic len() function

```python
print(len("Programiz"))
print(len(["Python", "Java", "C"]))
print(len({"Name": "John", "Address": "Nepal"}))
```

Output:

```python
9
3
2
```

Here, we can see that many data types such as string, list, tuple, set, and dictionary can work with 
the **len()** function. However, we can see that it returns specific information about specific data 
types.

## Class Polymorphism in Python

Polymorphism is a very important concept in Object-Oriented Programming.

We can use the concept of polymorphism while creating class methods as Python allows different classes 
to have methods with the same name.

We can then later generalize calling these methods by disregarding the object we are working with. 
Let's look at an example:

### Example 3: Polymorphism in Class Methods

```python
class Cat:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def info(self):
        print(f"I am a cat. My name is {self.name}. I am {self.age} years old.")

    def make_sound(self):
        print("Meow")


class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def info(self):
        print(f"I am a dog. My name is {self.name}. I am {self.age} years old.")

    def make_sound(self):
        print("Bark")


cat1 = Cat("Kitty", 2.5)
dog1 = Dog("Fluffy", 4)

for animal in (cat1, dog1):
    animal.make_sound()
    animal.info()
    animal.make_sound()
```

Output:

```python
Meow
I am a cat. My name is Kitty. I am 2.5 years old.
Meow
Bark
I am a dog. My name is Fluffy. I am 4 years old.
Bark
```

Here, we have created two classes **Cat** and **Dog**. They share a similar structure and have the same 
method names **info()** and **make_sound()**.

However, notice that we have not created a common superclass or linked the classes together in any way. 
Even then, we can pack these two different objects into a tuple and iterate through it using a common 
**animal** variable. It is possible due to polymorphism.

## Polymorphism and Inheritance

Like in other programming languages, the child classes in Python also inherit methods and attributes 
from the parent class. We can redefine certain methods and attributes specifically to fit the child 
class, which is known as **Method Overriding**.

Polymorphism allows us to access these overridden methods and attributes that have the same name as the 
parent class.

### Example 4: Method Overriding

```python
from math import pi


class Shape:
    def __init__(self, name):
        self.name = name

    def area(self):
        pass

    def fact(self):
        return "I am a two-dimensional shape."

    def __str__(self):
        return self.name


class Square(Shape):
    def __init__(self, length):
        super().__init__("Square")
        self.length = length

    def area(self):
        return self.length**2

    def fact(self):
        return "Squares have each angle equal to 90 degrees."


class Circle(Shape):
    def __init__(self, radius):
        super().__init__("Circle")
        self.radius = radius

    def area(self):
        return pi*self.radius**2


a = Square(4)
b = Circle(7)
print(b)
print(b.fact())
print(a.fact())
print(b.area())
```

Output:

``` python
Circle
I am a two-dimensional shape.
Squares have each angle equal to 90 degrees.
153.93804002589985
```

Here, we can see that the methods such as ***__str__()***, which have not been overridden in the child 
classes, are used from the parent class.

Due to polymorphism, the Python interpreter automatically recognizes that the **fact()** method for 
object **a(Square** class) is overridden. So, it uses the one defined in the child class.

On the other hand, since the **fact()** method for object b isn't overridden, it is used from the 
Parent Shape class.

# WHAT IS A DUNDER METHOD?

Dunder methods, also known as magic methods or special methods, are predefined methods in Python that 
have double underscores (or “dunders”) at the beginning and end of their names. These methods provide a 
way to define specific behaviors for built-in operations or functionalities in Python classes. By 
implementing dunder methods, you can customize the behavior of your objects and make them work 
seamlessly with Python’s language constructs.

##  __init__ Method

In Python, __init__ is a special method known as the constructor. It is automatically called when a new 
instance (object) of a class is created. The __init__ method allows you to initialize the attributes 
(variables) of an object.

Here’s an example to illustrate the usage of __init__:

```python
class MyClass:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def display_info(self):
        print(f"Name: {self.name}")
        print(f"Age: {self.age}")

# Creating an instance of MyClass
obj = MyClass("John", 25)

# Accessing attributes and calling methods
obj.display_info()
```

### How Does __init__() Method Work?

The python __init__ method is declared within a class and is used to initialize the attributes of an 
object as soon as the object is formed. While giving the definition for an __init__(self) method, a 
default parameter, named ‘self’ is always passed in its argument. This self represents the object of 
the class itself. Like in any other method of a class, in case of __init__ also ‘self’ is used as a 
dummy object variable for assigning values to the data members of an object. 

The __init__ method is often referred to as double underscores init or dunder init for it has two 
underscores on each side of its name. These double underscores on both the sides of init imply that the 
method is invoked and used internally in Python, without being required to be called explicitly by the 
object. 

This python __init__ method may or may not take arguments for object initialisation. You can also pass 
default arguments in its parameter. However, even though there is no such concept of Constructor 
Overloading in Python, one can still achieve polymorphism in the case of constructors in Python on the 
basis of its argument.

### Init in Python: Syntax 

We can declare a __init__ method inside a class in Python using the following syntax:

```python
class class_name():
           
          def __init__(self):
                  # Required initialisation for data members
 
          # Class methods
                 …
                 …
```

### Types of __init__ Constructor

#### The Default __init__ Constructor

The default __init__ constructor in Python is the constructor that does not accept any parameters, 
except for the ‘self’ parameter. The ‘self’ is a reference object for that class. The syntax for 
defining a default __init__ constructor is as follows:

```python
class Default():
    
    #defining default constructor
    def __init__(self):
        self.var1 = 56
        self.var2 = 27
        
    #class function for addition
    def add(self):
        print("Sum is ", self.var1 + self.var2)

obj = Default()     # since default constructor doesn’t take any argument
obj.add()
```

#### Parameterised __init__ Constructor

When we want to pass arguments in the constructor of a class, we make use of the parameterised __init__ 
method. It accepts one or more than one argument other than the self.

```python
class Default():
    
    #defining parameterised constructor
    def __init__(self, n1, n2):
        self.var1 = n1
        self.var2 = n2
        
    #class function for addition
    def add(self):
        print("Sum is ", self.var1 + self.var2)

obj = Default(121, 136)              #Creating object for a class with parameterised init
obj.add()
```

#### The __init__ method with default parameters

As you might already know, we can pass default arguments to a member function or a constructor, be it 
any popular programming language. In the very same way, Python also allows us to define a __init__ 
method with default parameters inside a class. We use the following syntax to pass a default argument 
in an __init__ method within a class.

```python
class Teacher:
    # definition for init method or constructor with default argument
    def __init__(self, name = "Preeti Srivastava"):
        self.name = name
     # Random member function
    def show(self):
        print(self.name, " is the name of the teacher.")
        
t1 = Teacher()                             #name is initialised with the default value of the argument
t2 = Teacher('Chhavi Pathak')    #name is initialised with the passed value of the argument
t1.show()
t2.show()
```

### Conclusion

So, to sum it all up, __init__ is a reserved method for classes in Python that basically behaves as the 
constructors. In other words, this method in a Python class is used for initialising the attributes of 
an object. It is invoked automatically at the time of instance creation for a class. This __init__ 
constructor is invoked as many times as the instances are created for a class. We can use any of the 
three types of __init__ constructors – default, parameterised, __init__ with default parameter – as per 
the need of our programming module. The ‘self’ is a mandatory parameter for any member function of a 
class, including the __init__ method, as it is a reference to the instance of the class created.

## __repr__ Method

In Python, every object comes with a set of built-in methods, amongst which __repr__ is one that often 
needs clarification for its use. The __repr__ method is one of Python’s “dunder” (double underscore) 
methods and stands for “representation”; it’s meant to return an unambiguous string representation of 
an object that can be used to reproduce the same object when fed to the eval() function. It is most 
commonly used for debugging, so it is important that the representation is information-rich and 
explicit.

### When and Why to Use __repr__

Using __repr__ is particularly useful in scenarios where you need to understand and inspect objects 
during the development and debugging process. It comes into play when you are inspecting objects in a 
shell, logging information for debugging purposes, or when you need to have a clear representation of 
the object in log files that helps in understanding the state of the object.

### Importance in Debugging

__repr__ becomes a powerful ally in debugging because it can provide detailed insights into the 
objects. When you print an object or view it in a debugger, the __repr__ method is called, giving you a 
clear indication of the object’s state.

### Representation in Interpreter and Logs

In the Python interpreter and logs, the __repr__ method determines how an object is displayed. This is 
why it’s crucial for __repr__ to return a precise and developer-friendly string that can help identify 
the object’s state without ambiguity.

### Step-by-Step Implementation

1. **Define the Method**: In your class, define a method named __repr__ that takes only self as an 
argument.

2. **Return a String**: The method should return a string that ideally looks like a valid Python expression that could be used to recreate the object with the same state.

3. **Include Essential Attributes**: Include the class attributes that are important for understanding the object’s state in the returned string.

4. **Formatting**: Use string formatting to create a readable and informative representation.
 
### Example

```python
class Point:

    def __init__(self, x, y):

        self.x = x

        self.y = y

    def __repr__(self):

        return f"Point(x={self.x}, y={self.y})"
```

### Conclusion

Implementing __repr__ in your Python classes can greatly improve the debugging and development 
experience by providing clear and informative object representations. It’s a balance between clarity, 
completeness, and simplicity.

# WHAT IS A PYTHON DECORATOR?

Decorators are Python functions that allow you to wrap another function as an input and modify its 
behavior without altering the wrapped function’s code. They are used to extend the behavior of a 
particular object, such as a class, method, or function. This approach promotes reusability, 
modularity, and separation of concerns in your Python programs.

## Decorators in Python Syntax

The syntax for a decorator in Python is quite simple. It starts with the keyword **'def'** to define a 
function, followed by an (**@**) and the name of the decorator. After that, you can add any arguments 
needed and then pass your target function as an argument. Example:

```python
#Step 1: Define the decorator function
def decorator_name(target_function):

    #Step 2: Define the wrapper function
def wrapper( * args, ** kwargs):

    #Step 3: Do something before target_function is called
    results = target_function( * args, ** kwargs)

# Step 4: Do something after the call to target_function
return results
return wrapper
```

## Use cases for Decorators

Decorators are widely used for a variety of purposes, such as:

- Timing function execution

- Caching results (memoization)

- Authorization and authentication

- Logging and error handling

- Input validation

## Types of Decorators in Python

Decorators come in many forms and shapes, from built-in functions to custom user-defined functions. 
Here are some of the most common types:

### Function Decorator

Function decorators allow you to extend the functionality of a single function without changing its 
code. They are higher-order functions that take a function as input and return a new function with the 
updated behavior. Example:

```python
def simple_decorator(func):

    def wrapper():

    print("Before function execution")

func()

print("After function execution")

return wrapper

@simple_decorator

def greet():

    print("Hello, world!")

greet()
```

### Class Decorator

Class decorators allow you to extend a class's behavior without changing the original source code. They 
are similar to function decorators but work on classes instead of functions. They take a class as input 
and return a new class with modified or extended behavior. Class decorators can be used for various 
purposes, such as adding or modifying class attributes, methods, or properties. Example:

```python
def class_decorator(cls):

    class NewClass(cls):

    def new_method(self):

    print("This is a new method added by the decorator")

return NewClass

@class_decorator

class MyClass:

    def original_method(self):

    print("This is the original method")

obj = MyClass()

obj.original_method()

obj.new_method()
```

### Decorators with Arguments

Decorators with arguments provide additional customization and flexibility when modifying or extending 
the behavior of functions or classes. These decorators accept arguments and return another decorator 
function, which then takes the function or class as input and returns the modified function or class. 
Example:

```python
def decorator_with_args(arg1, arg2):

    def actual_decorator(func):

    def wrapper( * args, ** kwargs):

    print(f "Decorator argument 1: {arg1}")

print(f "Decorator argument 2: {arg2}")

func( * args, ** kwargs)

return wrapper

return actual_decorator

@decorator_with_args("Hello", "World")

def greet(name):

    print(f "Hi, {name}!")

greet("John")
```

## How to write a decorator in Python?

1. Define a higher-order function that takes a function as input.

2. Inside this higher-order function, define a nested function (a wrapper) that will modify or extend 
the input function's behavior.

3. Call the input function within the wrapper function and add any additional functionality you desire.

4. Return the wrapper function from the higher-order function

In this example, we will create a simple decorator that measures the execution time of a function.

```python
import time

def timer_decorator(func):

    def wrapper( * args, ** kwargs):

    start_time = time.time()

result = func( * args, ** kwargs)

end_time = time.time()

print(f "{func.__name__} executed in {end_time - start_time:.5f} seconds")

return result

return wrapper

@timer_decorator

def slow_function():

    time.sleep(2)

print("Slow function executed")

slow_function()
```

In the example, the **'@'** symbol is syntactic sugar that simplifies the process of applying a 
decorator to a function. When placed above a function definition, it indicates that the function should 
be passed as an argument to the decorator.

## Decorating Functions With Parameters

When decorating functions that accept parameters, you should use the *args and **kwargs syntax to 
ensure that your decorator can handle any number of positional and keyword arguments.

The *args syntax allows your wrapper function to accept any number of positional arguments, while 
**kwargs enables it to accept any number of keyword arguments.

Here is an example:

```python
def print_arguments_decorator(func):

    def wrapper( * args, ** kwargs):

    print(f "Positional arguments: {args}")

print(f "Keyword arguments: {kwargs}")

return func( * args, ** kwargs)

return wrapper

@print_arguments_decorator

def example_function(a, b, c, x = 1, y = 2, z = 3):

    return a + b + c + x + y + z

example_function(10, 20, 30, x = 5, y = 10, z = 15)
```
