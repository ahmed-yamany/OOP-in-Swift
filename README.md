# OOP

- is a  programming concept that organizes software design
- focuses on the object rather than logic

## OOP concepts

1. Object
2. Class
3. Encapsulation
4. Abstraction
5. Inheritance
6. Polymorphism

## object

referred to as an instance of a class, it contains member functions and variables, it occupies  space in the memory

## Class

- a class is a blueprint or a template of an object
- is a user-defined data type
- inside a class, we define variables, constants, and member functions
- it binds data and functions together in a single unit
- it does not consume memory at run time

<aside>
💡 - classes are not considered as a data structure it’s a logical entity
- class can exist without an object but object can not exist without a class

</aside>

## ****Encapsulation****

a mechanism of restricting the direct access to some components of an object,

Encapsulation is a concept by which we hide data and methods from outside intervention and usage

****Benefits of Encapsulation Programming****

- **Hiding Data:** Users will have no idea how classes are being implemented or stored. All that users will know is that values are being passed and initialized
- **More Flexibility:** Enables you to set variables as read or write -only.

```swift
class Maths {    
    let a: Int!
    let b: Int!
    private var result: Int?
   
    init(a: Int,b: Int) {
        self.a = a
        self.b = b
    }
    func add() {
        result = a + b
    }
    func displayResult() {
        print("Result - \(result)")
    }
}
let calculation = Maths(a: 2, b: 3)
calculation.add()
calculation.displayResult()
```

In the above example, we encapsulated the variable “result” by using the access specifier “private”. We hide the data of variable “result” from any outside intervention and usage.

## ****Abstraction****

Abstraction occurs when a programmer hides any irrelevant data about an object or an instantiated class to reduce complexity and help users interact with the object more efficiently.

an abstraction relates to how an object and its behaviors are presented to the user and encapsulation is a methodology that helps create that experience.

Think about the interface of your mobile phone. Whether you use an Android operating system or iOS, you don't interact directly with the code that allows your phone to connect to the internet, send a text message or play a video game. Instead, you interact with the code through a user interface that is designed to streamline your experience and make it easy to access the functions and methods you need to complete a task. In this case, the interface is abstracted away from the actual implementation of the code

## Inheritance

- Inheritance is a process by which a child class inherits the properties of its parent class.
- A parent class is called a superclass, and a child class is called a subclass
- A class that doesn’t inherit from a superclass is known as a base class

```swift
class Subclass: Superclass {
    // subclass definition goes here
}
```

**How Can You Disallow a Class from Being Inherited?**

You can prevent a class , method, property, or subscript from being overridden by marking it as final. Do this by writing the final modifier before the class , method, property, or subscript’s.

## Polymorphism

Polymorphism in Swift comes in two flavors.

1. Compile time polymorphism

1. *Runtime Polymorphism*

1. Compile time polymorphism “method overloading”

In method overloading, a function can perform different actions with the same function name, but should have a different signature

Method signature consists of the following:

1. Method name.

2. Number of parameters

3. Data Type and order of parameters.

```swift
func addNums(i: Int, j: Int) -> Int
{
	return i + j
}

func addNums(i: Int, j: Int, k: Int) -> Int
{
	return i + j + k
}

print(addNums(i: 2, j: 3)
print(addNums(i: 2, j: 3, k: 5))
```

1. Runtime polymorphism “method overriding”
    
    in runtime polymorphism, Swift invokes the actual method during the running of the program.
    
    It will not know which method to invoke during compile time.
    
    It works with inheritance.
    
    Method overriding is a concept where even though the method name and parameters passed are similar, the behavior is different based on the object type.
    
    ```swift
    class Animal 
    {
    	func makeNoise()
    	{
    		print("Durrr")
    	}
    }
    class Cat: Animal 
    {
    	override func makeNoise()
    	{
    		print("Meoooowwwww")
    	}
    }
    ```
    

references

[https://www.cosmiclearn.com/swift/polymorphism.php#compile](https://www.cosmiclearn.com/swift/polymorphism.php#compile)

[https://www.javatpoint.com/what-is-object-oriented-programming](https://www.javatpoint.com/what-is-object-oriented-programming)

[https://medium.com/swift-india/oops-in-swift-998738407423](https://medium.com/swift-india/oops-in-swift-998738407423)
