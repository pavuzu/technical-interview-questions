# SOLID and Other Principles​

## Contents

- [SOLID and Other Principles​](#solid-and-other-principles)
  - [Contents](#contents)
  - [Questions and Answers: SOLID Principles](#questions-and-answers-solid-principles)
    - [What are SOLID Principles?](#what-are-solid-principles)
    - [What is the difference between SOLID Principles and Design Patterns?](#what-is-the-difference-between-solid-principles-and-design-patterns)
    - [What is Single Responsibility Principle?](#what-is-single-responsibility-principle)
    - [What is Open-closed Principle?](#what-is-open-closed-principle)
    - [What is Liskov Substitution Principle?](#what-is-liskov-substitution-principle)
    - [What is Interface Segregation Principle?](#what-is-interface-segregation-principle)
    - [What is Dependency Inversion Principle?](#what-is-dependency-inversion-principle)
  - [Questions and Answers: Other Software Development Principles](#questions-and-answers-other-software-development-principles)
    - [What is DRY principle?](#what-is-dry-principle)
    - [What is YAGNI principle?](#what-is-yagni-principle)
    - [What is KISS principle?](#what-is-kiss-principle)
  - [Additional Resources and References](#additional-resources-and-references)

## Questions and Answers: SOLID Principles

### What are SOLID Principles?

The SOLID principles are a set of design principles that help in creating maintainable and extensible software. These principles promote loose coupling, high cohesion, and modular design, making the software easier to understand, modify, and test. They were introduced by Robert C. Martin (Uncle Bob) as a guideline for object-oriented design and development. The acronym SOLID represents five principles:

- **S**ingle Responsibility Principle (SRP)
- **O**pen/Closed Principle (OCP)
- **L**iskov Substitution Principle (LSP)
- **I**nterface Segregation Principle (ISP)
- **D**ependency Inversion Principle (DIP)

### What is the difference between SOLID Principles and Design Patterns?

**SOLID Principles** focus on guiding the design of individual components and the overall architecture of the system. They provide fundamental guidelines for creating maintainable and flexible code.

**Design Patterns**, on the other hand, provide reusable solutions to common design problems. They offer higher-level abstractions and blueprints for organizing and coordinating multiple components.

While SOLID Principles address the structure and relationships between components, Design Patterns provide specific solutions for design challenges. Both concepts are often used together to create robust and maintainable software systems.

### What is Single Responsibility Principle?

> A class should have one, and only one, reason to change.

The **Single Responsibility Principle (SRP)** states that a class should have only one reason to change. Each class should be responsible for a single piece of functionality or behavior. This principle helps in maintaining code clarity and reducing the impact of changes by isolating responsibilities.

### What is Open-closed Principle?

> You should be able to extend a classes behavior, without modifying it.

The **Open-Closed Principle (OCP)** states that software entities (classes, methods, etc.) should be open for extension but closed for modification. This can be achieved by using abstractions, interfaces, and inheritance to allow for adding new functionality through extension rather than modifying existing code.

### What is Liskov Substitution Principle?

> Derived classes must be substitutable for their base classes.

The **Liskov Substitution Principle (LSP)** states that objects of a base class should be replaceable with objects of its derived classes without altering the correctness of the program. Derived classes should adhere to the contract defined by the base class and should be substitutable in any context where the base class is used.

### What is Interface Segregation Principle?

> Make fine grained interfaces that are client specific.

The **Interface Segregation Principle (ISP)** states that clients should not be forced to depend on interfaces they do not use. It is better to create specific interfaces with a focused set of methods rather than one large interface. This allows clients to depend only on the interfaces that are relevant to them.

### What is Dependency Inversion Principle?

> Depend on abstractions, not on concretions.

The **Dependency Inversion Principle (DIP)** encourages  relying on abstractions (interfaces, abstract classes) to define dependencies instead of concrete implementations. High-level modules should depend on abstractions rather than low-level modules. This helps in achieving loose coupling, flexibility, and easier testing and maintenance.

## Questions and Answers: Other Software Development Principles

### What is DRY principle?

The **DRY (Don't Repeat Yourself)** principle advocates for avoiding code duplication by promoting code reuse and maintaining a single, unambiguous representation of knowledge or functionality. It enhances maintainability, modularity, and reduces the risk of inconsistencies and bugs.

### What is YAGNI principle?

The **YAGNI (You Ain't Gonna Need It)** principle advises against implementing functionality or code that is not currently needed. It promotes simplicity, avoiding over-engineering, and focusing on delivering immediate requirements.

### What is KISS principle?

The **KISS (Keep It Simple, Stupid)** principle is a design principle that emphasizes simplicity in software development. It suggests that systems and solutions should be kept simple rather than complex. By prioritizing simplicity, developers can create code that is easier to understand, maintain, and debug. The KISS principle encourages avoiding unnecessary complexity and striving for straightforward, minimalistic designs.

## Additional Resources and References

- [The Principles of OOD](http://butunclebob.com/ArticleS.UncleBob.PrinciplesOfOod)
- [Pablo's SOLID Software Development](https://lostechies.com/wp-content/uploads/2011/03/pablos_solid_ebook.pdf)
- [C# Best Practices : Dangers of Violating SOLID Principles in C#](https://learn.microsoft.com/en-us/archive/msdn-magazine/2014/may/csharp-best-practices-dangers-of-violating-solid-principles-in-csharp)
- [ChatGPT-3.5](https://openai.com/blog/chatgpt)
