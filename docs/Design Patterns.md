# Design Patterns

## Contents

- [Design Patterns](#design-patterns)
  - [Contents](#contents)
  - [Questions and Answers: Design Patterns](#questions-and-answers-design-patterns)
    - [What are Design Patterns and what problem they solve?](#what-are-design-patterns-and-what-problem-they-solve)
    - [What are the types of Design Patterns?](#what-are-the-types-of-design-patterns)
  - [Questions and Answers: Creational Patterns](#questions-and-answers-creational-patterns)
    - [What are Creational Design Patterns?](#what-are-creational-design-patterns)
    - [What is Singleton Design Pattern?](#what-is-singleton-design-pattern)
    - [How to make Singleton pattern thread safe?](#how-to-make-singleton-pattern-thread-safe)
    - [What is Factory pattern?](#what-is-factory-pattern)
    - [Why to use factory pattern?](#why-to-use-factory-pattern)
    - [How to implement Factory method pattern?](#how-to-implement-factory-method-pattern)
    - [What is Abstract Factory pattern?](#what-is-abstract-factory-pattern)
  - [Questions and Answers: Structural Patterns](#questions-and-answers-structural-patterns)
    - [What are Structural Design Patterns?](#what-are-structural-design-patterns)
  - [Questions and Answers: Behavioral Patterns](#questions-and-answers-behavioral-patterns)
    - [What are Behavioral Design Patterns?](#what-are-behavioral-design-patterns)
  - [Additional Resources and References](#additional-resources-and-references)

## Questions and Answers: Design Patterns

### What are Design Patterns and what problem they solve?

Design patterns are reusable solutions to common design problems encountered in software development. They provide proven approaches and templates for solving specific design challenges. Design patterns help address various problems, including:

- **Code Reusability**: Design patterns promote reusability by encapsulating successful design practices that can be applied to different projects and scenarios.
- **Maintainability and Scalability**: Design patterns enhance code maintainability by providing well-structured and organized solutions. They help separate concerns and make it easier to modify and extend code as the system evolves.
- **Flexibility and Adaptability**: Design patterns make software systems more flexible and adaptable to changes. They provide structures and guidelines that allow for easier modification and addition of new features without disrupting existing functionality.
- **Performance Optimization**: Design patterns can improve performance by providing efficient and optimized solutions to common design problems. They help eliminate redundant computations, reduce memory usage, and enhance overall system performance.
- **Collaboration and Communication**: Design patterns establish a common language and understanding among developers. They serve as a communication tool, facilitating effective discussions and sharing of design concepts.
- **Design Consistency**: Design patterns promote consistency in software design by offering standardized approaches to solving design problems. They help ensure that software systems follow established best practices and guidelines.

### What are the types of Design Patterns?

There are three main types of design patterns:

1. **Creational Patterns**: These patterns focus on object creation mechanisms, providing ways to create objects in a flexible and controlled manner. Examples include Singleton, Factory, Abstract Factory, Builder, and Prototype patterns.
2. **Structural Patterns**: These patterns deal with the composition of classes and objects, focusing on how they are structured and organized. Structural patterns help in building relationships between objects to form larger structures. Examples include Adapter, Decorator, Proxy, Composite, and Facade patterns.
3. **Behavioral Patterns**: These patterns address the interaction and communication between objects, defining the patterns of communication and behavior flow. They help in designing how objects collaborate to accomplish tasks. Examples include Observer, Strategy, Template Method, Command, and Iterator patterns.

## Questions and Answers: Creational Patterns

### What are Creational Design Patterns?

Creational design patterns are a category of design patterns that focus on object creation mechanisms. They provide ways to create objects in a flexible and controlled manner, ensuring that objects are created appropriately based on the requirements and constraints of the system.

The main goal of creational design patterns is to abstract the object creation process, decoupling it from the client code that uses the objects. This abstraction allows for greater flexibility, maintainability, and extensibility of the codebase.

Some commonly used creational design patterns include:

- **Singleton Pattern**: Ensures that only one instance of a class is created and provides a global access point to that instance.
- **Factory Method Pattern**: Defines an interface or base class for creating objects, but allows subclasses to decide which specific class to instantiate.
- **Abstract Factory Pattern**: Provides an interface for creating families of related or dependent objects, without specifying their concrete classes.
- **Builder Pattern**: Separates the construction of complex objects from their representation, allowing the same construction process to create different representations.
- **Prototype Pattern**: Creates new objects by cloning existing ones, avoiding the need for complex initialization.

### What is Singleton Design Pattern?

The Singleton design pattern is a creational design pattern that ensures the creation of only one instance of a class throughout the lifetime of an application. It provides a global access point to that instance, allowing other parts of the code to access it easily.

Key features of the Singleton pattern:

1. **Single Instance**: The Singleton pattern guarantees that only one instance of the class is created and exists at any given time.
2. **Global Access**: The Singleton instance is typically accessed through a globally available method or property, allowing other parts of the code to use it conveniently.
3. **Private Constructor**: The constructor of the Singleton class is made private to prevent direct instantiation of the class from outside. This ensures that the Singleton instance is controlled and limited to one.

Common use cases for the Singleton pattern include scenarios where you need to have a single, shared resource or manager throughout your application. Some examples include database connections, logging systems, caches, thread pools, and configuration managers.

Here's a basic example of implementing a Singleton in C#:

``` csharp
public class Singleton
{
    private static Singleton instance;
    
    // Private constructor to prevent direct instantiation
    private Singleton()
    {
        // Initialization code here
    }
    
    public static Singleton GetInstance()
    {
        if (instance == null)
        {
            instance = new Singleton();
        }
        
        return instance;
    }
}
```

In this example, the Singleton class has a private constructor and a static *GetInstance()* method that returns the Singleton instance. The first time *GetInstance()* is called, it creates a new instance of the Singleton class. Subsequent calls to *GetInstance()* return the same instance.

> It's important to note that in multi-threaded environments, you may need to consider thread safety and synchronization mechanisms to ensure the Singleton instance is created and accessed correctly.

The Singleton pattern allows for global access to a single instance, promoting efficient resource utilization and consistent behavior throughout the application. However, it should be used judiciously and carefully, as it can introduce tight coupling and potential challenges for testing and maintenance.

### How to make Singleton pattern thread safe?

To make the Singleton pattern thread-safe, you need to consider potential race conditions that may occur when multiple threads try to access or create the Singleton instance simultaneously. Here are a few approaches to ensure thread safety:

1. **Eager Initialization**: One way to achieve thread safety is by using eager initialization, where the Singleton instance is created at the time of class loading. This approach guarantees that the instance is created before any thread can access it. However, it may introduce unnecessary overhead if the instance is not always needed.

    ```csharp
    public class Singleton
    {
        private static readonly Singleton instance = new Singleton();

        private Singleton()
        {
            // Initialization code here
        }

        public static Singleton Instance => instance;
    }
    ```

2. **Double-Checked Locking**: Double-checked locking is a technique that combines laziness of instantiation with thread safety. It uses a lock to ensure that only one thread creates the instance, while allowing subsequent threads to access the instance without acquiring the lock.

    ``` csharp
    public class Singleton
    {
        private static Singleton instance;
        private static readonly object lockObject = new object();

        private Singleton()
        {
            // Initialization code here
        }

        public static Singleton Instance
        {
            get
            {
                if (instance == null)
                {
                    lock (lockObject)
                    {
                        if (instance == null)
                        {
                            instance = new Singleton();
                        }
                    }
                }
                return instance;
            }
        }
    }
    ```

3. **Using Lazy<T>**: In C#, you can also use the Lazy<T> class to achieve thread safety and lazy initialization of the Singleton instance. The Lazy<T> class handles synchronization internally and ensures that only one instance is created.

    ```csharp
    public class Singleton
    {
        private static readonly Lazy<Singleton> lazyInstance = new Lazy<Singleton>(() => new Singleton());

        private Singleton()
        {
            // Initialization code here
        }

        public static Singleton Instance => lazyInstance.Value;
    }
    ```

These approaches ensure that the Singleton instance is created only when needed and that concurrent access is handled correctly. However, it's important to note that the performance characteristics and behavior may vary based on the specific implementation and runtime environment.

### What is Factory pattern?

The Factory pattern is a creational design pattern that provides an interface or base class for creating objects without specifying their concrete classes. It encapsulates the object creation logic and allows the client code to work with objects of different types without being tightly coupled to their specific implementations.

The Factory pattern is useful in scenarios where you want to delegate the responsibility of object creation to subclasses or when the exact class of the created object needs to be determined at runtime. It promotes loose coupling and enhances flexibility and extensibility in the codebase.

Key components of the Factory pattern:

1. **Factory Interface or Base Class**: Defines a common interface or abstract class for creating objects. It declares factory methods that are responsible for creating specific types of objects.
2. **Concrete Factories**: Implement the factory interface or derive from the factory base class. Each concrete factory provides the implementation for creating a particular type of object.
3. **Product Interface or Base Class**: Represents the common interface or abstract class for the objects that the factory creates. It defines the operations that can be performed on the objects.
4. **Concrete Products**: Implement the product interface or derive from the product base class. Each concrete product represents a specific type of object created by the factory.

Here's a basic example of implementing a Factory pattern in C#:

``` csharp
// Product interface
public interface IProduct
{
    void PerformAction();
}

// Concrete products
public class ConcreteProductA : IProduct
{
    public void PerformAction()
    {
        Console.WriteLine("Performing action for Product A");
    }
}

public class ConcreteProductB : IProduct
{
    public void PerformAction()
    {
        Console.WriteLine("Performing action for Product B");
    }
}

// Factory interface
public interface IProductFactory
{
    IProduct CreateProduct();
}

// Concrete factories
public class ConcreteProductFactoryA : IProductFactory
{
    public IProduct CreateProduct()
    {
        return new ConcreteProductA();
    }
}

public class ConcreteProductFactoryB : IProductFactory
{
    public IProduct CreateProduct()
    {
        return new ConcreteProductB();
    }
}
```

In this example, we have an *IProduct* interface representing the common operations that can be performed on products. The *ConcreteProductA* and *ConcreteProductB* classes implement this interface.

The *IProductFactory* interface declares the factory method *CreateProduct()* responsible for creating *IProduct* instances. The *ConcreteProductFactoryA* and *ConcreteProductFactoryB* classes implement this interface and provide the specific implementation for creating *ConcreteProductA* and *ConcreteProductB* instances, respectively.

Using the factory, client code can create objects without being aware of the specific product types:

``` csharp
IProductFactory factory = new ConcreteProductFactoryA();
IProduct product = factory.CreateProduct();
product.PerformAction(); // Outputs: "Performing action for Product A"
```

The Factory pattern decouples the client code from the specific product implementations, allowing for flexibility and extensibility. New product types can be added by implementing the product interface and creating a corresponding factory, without modifying the existing client code.

> Note: The Factory pattern can have variations such as the Abstract Factory pattern, which provides a factory of factories to create families of related objects.

### Why to use factory pattern?

The Factory pattern offers several benefits and is used in software development for the following reasons:

- **Loose Coupling**: The Factory pattern promotes loose coupling between the client code and the created objects. By using factories, the client code doesn't directly instantiate the objects, reducing dependencies and making the code more flexible and maintainable.
- **Encapsulation of Object Creation**: The Factory pattern encapsulates the object creation logic within the factory, abstracting it from the client code. This improves code organization and allows for changes in the creation process without impacting the client code.
- **Flexibility and Extensibility**: The Factory pattern allows for the creation of objects of different types by using the same interface or base class. It enables the addition of new product types without modifying the existing client code, promoting extensibility and adaptability.
- **Centralized Control**: Using a factory centralizes the creation logic in one place, making it easier to manage and control the object creation process. This can include handling complex instantiation procedures, applying specific configurations, or managing resource allocation.
- **Separation of Concerns**: The Factory pattern separates the responsibility of object creation from the client code, adhering to the principle of single responsibility. It promotes modular design and improves code maintainability by keeping object creation logic isolated and focused.
- **Dependency Injection**: The Factory pattern can be used as a form of dependency injection, allowing the creation of objects with their dependencies resolved and injected automatically. This facilitates the management of object dependencies and promotes decoupling.
- **Testing and Mocking**: By using factories, it becomes easier to test and mock the client code. Mocking dependencies or substituting different product implementations during testing can be achieved by providing alternative factory implementations.

Overall, the Factory pattern provides a structured approach to object creation, offering flexibility, maintainability, and improved code organization. It enables loose coupling, encapsulation, and centralized control over the creation process, contributing to robust and modular software design.

### How to implement Factory method pattern?

To implement the Factory Method pattern, follow these steps:

1. Define a common interface or abstract base class for the products you want to create. This interface or base class should declare the methods that the products will implement.
2. Create concrete product classes that implement the interface or derive from the base class defined in step 1. Each concrete product represents a specific type of object that the factory will create.
3. Create a factory interface or abstract base class that declares the factory method. This factory method will be responsible for creating the products. The return type of the factory method should be the interface or base class defined in step 1.
4. Implement concrete factories that implement the factory interface or derive from the factory base class. Each concrete factory will provide the implementation for the factory method and create a specific type of product.

Here's a simplified example of implementing the Factory Method pattern in C#:

``` csharp
// Step 1: Define the product interface or base class
public interface IProduct
{
    void SomeOperation();
}

// Step 2: Create concrete product classes
public class ConcreteProductA : IProduct
{
    public void SomeOperation()
    {
        Console.WriteLine("ConcreteProductA: SomeOperation");
    }
}

public class ConcreteProductB : IProduct
{
    public void SomeOperation()
    {
        Console.WriteLine("ConcreteProductB: SomeOperation");
    }
}

// Step 3: Create the factory interface or base class
public interface IProductFactory
{
    IProduct CreateProduct();
}

// Step 4: Implement concrete factories
public class ConcreteProductFactoryA : IProductFactory
{
    public IProduct CreateProduct()
    {
        return new ConcreteProductA();
    }
}

public class ConcreteProductFactoryB : IProductFactory
{
    public IProduct CreateProduct()
    {
        return new ConcreteProductB();
    }
}
```

In this example, we have an *IProduct* interface representing the common operations that can be performed on products. The *ConcreteProductA* and *ConcreteProductB* classes implement this interface.

The *IProductFactory* interface declares the factory method *CreateProduct()*, responsible for creating *IProduct* instances. The *ConcreteProductFactoryA* and *ConcreteProductFactoryB* classes implement this interface and provide the specific implementation for creating *ConcreteProductA* and *ConcreteProductB* instances, respectively.

To use the factory, you can instantiate a specific factory and use the factory method to create the desired product:

``` csharp
IProductFactory factory = new ConcreteProductFactoryA();
IProduct product = factory.CreateProduct();
product.SomeOperation();  // Output: "ConcreteProductA: SomeOperation"
```

By using the factory method, the client code is decoupled from the specific product implementation, allowing for easy switching between different product types without modifying the client code.

### What is Abstract Factory pattern?

The Abstract Factory pattern is a creational design pattern that provides an interface for creating families of related or dependent objects without specifying their concrete classes. It allows the client code to work with objects of different types that belong to a common theme or family.

The Abstract Factory pattern is useful when there are multiple related product families or when the client code needs to create objects that are interdependent or compatible with each other. It promotes the creation of cohesive sets of objects and ensures that the created objects are compatible within their respective families.

Key components of the Abstract Factory pattern:

1. **Abstract Factory**: Declares an interface or abstract class for creating the abstract product objects. It provides factory methods for creating objects of different types within a family.
2. **Concrete Factories**: Implement the abstract factory interface or derive from the abstract factory base class. Each concrete factory is responsible for creating a family of related products.
3. **Abstract Products**: Declare the interface or abstract class for the products created by the factory. Each abstract product represents a specific type within a family of related products.
4. **Concrete Products**: Implement the abstract product interface or derive from the abstract product base class. Each concrete product represents a specific type of product within a family created by the factory.

Here's a basic example of implementing the Abstract Factory pattern in C#:

``` csharp
// Abstract Product A
public interface IProductA
{
    void OperationA();
}

// Concrete Product A1
public class ConcreteProductA1 : IProductA
{
    public void OperationA()
    {
        Console.WriteLine("ConcreteProductA1: OperationA");
    }
}

// Concrete Product A2
public class ConcreteProductA2 : IProductA
{
    public void OperationA()
    {
        Console.WriteLine("ConcreteProductA2: OperationA");
    }
}

// Abstract Product B
public interface IProductB
{
    void OperationB();
}

// Concrete Product B1
public class ConcreteProductB1 : IProductB
{
    public void OperationB()
    {
        Console.WriteLine("ConcreteProductB1: OperationB");
    }
}

// Concrete Product B2
public class ConcreteProductB2 : IProductB
{
    public void OperationB()
    {
        Console.WriteLine("ConcreteProductB2: OperationB");
    }
}

// Abstract Factory
public interface IAbstractFactory
{
    IProductA CreateProductA();
    IProductB CreateProductB();
}

// Concrete Factory 1
public class ConcreteFactory1 : IAbstractFactory
{
    public IProductA CreateProductA()
    {
        return new ConcreteProductA1();
    }

    public IProductB CreateProductB()
    {
        return new ConcreteProductB1();
    }
}

// Concrete Factory 2
public class ConcreteFactory2 : IAbstractFactory
{
    public IProductA CreateProductA()
    {
        return new ConcreteProductA2();
    }

    public IProductB CreateProductB()
    {
        return new ConcreteProductB2();
    }
}
```

In this example, we have two families of products: Product A and Product B. The *IProductA* and *IProductB* interfaces define the operations that can be performed on products within their respective families.

The *ConcreteProductA1*, *ConcreteProductA2*, *ConcreteProductB1*, and *ConcreteProductB2* classes implement the corresponding interfaces, representing concrete products within their families.

The *IAbstractFactory* interface declares factory methods for creating objects of both product families. The *ConcreteFactory1* and *ConcreteFactory2* classes implement this interface and provide the specific implementation for creating objects of the respective product families.

To use the abstract factory, you can instantiate a specific factory and use its factory methods to create products:

``` csharp
IAbstractFactory factory1 = new ConcreteFactory1();
IProductA productA1 = factory1.CreateProductA();
IProductB productB1 = factory1.CreateProductB();

productA1.OperationA();  // Output: "ConcreteProductA1: OperationA"
productB1.OperationB();  // Output: "ConcreteProductB1: OperationB"

IAbstractFactory factory2 = new ConcreteFactory2();
IProductA productA2 = factory2.CreateProductA();
IProductB productB2 = factory2.CreateProductB();

productA2.OperationA();  // Output: "ConcreteProductA2: OperationA"
productB2.OperationB();  // Output: "ConcreteProductB2: OperationB"
```

In this example, we create two concrete factories, *ConcreteFactory1* and *ConcreteFactory2*, which are responsible for creating products of their respective families. We then use these factories to create instances of *IProductA* and *IProductB*.

The Abstract Factory pattern allows for creating families of related objects without specifying their concrete classes. By using the abstract factory, the client code can create and work with objects from different families interchangeably, ensuring compatibility and cohesive usage.

> Note that the example provided is a basic illustration of the Abstract Factory pattern. In real-world scenarios, the number of product families and the complexity of the objects within them may vary. The Abstract Factory pattern helps in managing the creation of related objects, ensuring they adhere to a common theme or interface.

## Questions and Answers: Structural Patterns

### What are Structural Design Patterns?

Structural design patterns are a category of design patterns that focus on the composition and organization of classes and objects. These patterns deal with the relationships between objects, emphasizing how they can be combined to form larger structures or solve complex design problems.

The main goal of structural design patterns is to provide ways to define relationships and structures among objects in a flexible and efficient manner. They enable the creation of clean and maintainable code by promoting code reusability, separation of concerns, and modularity.

Some commonly used structural design patterns include:

- **Adapter Pattern**: Converts the interface of a class into another interface that clients expect. It allows incompatible classes to work together by providing a bridge between them.
- **Decorator Pattern**: Allows adding new behaviors or responsibilities to an object dynamically without modifying its structure. It provides a flexible alternative to subclassing for extending the functionality of objects.
- **Composite Pattern**: Represents a group of objects as a single object, forming a tree-like structure. It allows clients to treat individual objects and groups of objects uniformly.
- **Proxy Pattern**: Provides a surrogate or placeholder for another object, controlling access to it. It enables the creation of additional functionality around the original object while maintaining the same interface.
- **Bridge Pattern**: Decouples an abstraction from its implementation, allowing them to vary independently. It provides a way to handle complex class hierarchies and promotes flexibility in the system design.
- **Flyweight Pattern**: Minimizes memory usage by sharing data across multiple objects. It allows for efficient handling of large numbers of fine-grained objects, reducing memory overhead.
- **Facade Pattern**: Provides a simplified interface to a complex subsystem or set of classes. It encapsulates the complexities and dependencies of the subsystem, making it easier to use and understand.
- **Composite Pattern**: Represents a part-whole hierarchy of objects, allowing clients to treat individual objects and groups of objects uniformly. It enables the creation of complex structures while maintaining a simple interface.

These structural design patterns offer different techniques for organizing and composing objects, each addressing specific design challenges. They enhance code flexibility, modularity, and extensibility by promoting proper class relationships and separation of concerns.

## Questions and Answers: Behavioral Patterns

### What are Behavioral Design Patterns?

Behavioral design patterns are a category of design patterns that focus on the interaction and communication between objects and classes. They define the patterns of communication, collaboration, and behavior among objects to achieve specific functionalities and responsibilities.

The main objective of behavioral design patterns is to provide effective solutions for managing the behavior and interaction of objects, making the code more flexible, maintainable, and reusable.

Here are some commonly used behavioral design patterns:

- **Observer Pattern**: Establishes a one-to-many dependency between objects, where the subject notifies its observers automatically of any state changes. This pattern enables loose coupling between objects and facilitates event-driven communication.
- **Strategy Pattern**: Encapsulates interchangeable algorithms or behaviors and allows clients to select and switch between them at runtime. It enables flexibility by separating algorithms from the client code and promoting extensibility.
- **Command Pattern**: Encapsulates a request as an object, allowing clients to parameterize and queue requests, as well as support undo-redo operations. This pattern decouples the sender and receiver of a request, providing flexibility and extensibility.
- **Iterator Pattern**: Provides a way to access elements of a collection sequentially without exposing its underlying structure. It simplifies iteration and traversal over collections and provides a uniform interface.
- **State Pattern**: Allows an object to alter its behavior when its internal state changes. It encapsulates states in separate classes and enables dynamic switching between states, promoting modularity and flexibility.
- **Template Method Pattern**: Defines the skeleton of an algorithm in a base class, allowing subclasses to override specific steps of the algorithm. This pattern provides a common structure while allowing customization of certain parts.
- **Chain of Responsibility Pattern**: Establishes a chain of objects, where each object has a chance to handle a request or pass it to the next object in the chain. It decouples the sender and receiver and provides flexibility in handling requests.
- **Visitor Pattern**: Separates an algorithm from the objects it operates on, allowing new operations to be added without modifying the object structure. It promotes extensibility by externalizing operations into visitor classes.

These behavioral design patterns offer various techniques for managing object behavior, interaction, and communication. Each pattern addresses specific challenges and provides solutions for making code more flexible, modular, and reusable.

## Additional Resources and References

- [Design Patterns in C# by Dofactory](https://www.dofactory.com/net/design-patterns)
- [ChatGPT-3.5](https://openai.com/blog/chatgpt)
