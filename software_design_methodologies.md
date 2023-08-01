# Software Design Methologies

1. What do we mean by coupling and cohesion when discussing structured design?


Both coupling and cohesion can be implemented to measure the quality of the design of a system.

The term 'coupling' describes the level of interdependence that exists between software modules, which are self-contained units performing specific tasks. When a high degree of coupling exists, modules are highly dependent on one another and are interconnected. Thus, when changes are made to one specific module, it is likely that there will be significant impacts on other modules. This can trigger a chain reaction, in which other modules may require modifications if they are tightly coupled. On the other hand, low coupling exists where modules are independent, meaning they have minimal dependence on other modules. Thus, when changes are made to one module, other modules are minimally impacted, giving rise to greater flexibility since the modules do not have much knowledge of other modules.

The term 'cohesion' describes how much the elements of a module cooperate to achieve one goal or function. High cohesion is desireable; a high degree of cohesion exists where elements are working towards a single goal, which is clearly stated and well-defined. Other characteristics and benefits of high cohesion include: code reusability, readability, testability and maintenance. On the other hand, low cohesion is described by elements that are loosely related with goals that are not well defined. Thus, the elements may be working towards multiple goals. Characteristics of low cohesion include complex codebases that are prone to bugs and lack a single purpose. Low cohesion is considered undesirable due to module interdependence, giving rise to difficulties in code maintenance, reusability, and readability.      


2. What is the difference between top-down and bottom-up design? Which best describes a function oriented design? 


A top-down design begins with the full software system, or a high-level structure. This system is subsequently split apart into smaller modules or components which contain finer details. Some scholars describe the top-down approach as breaking a big task into smaller problems which are worked out individually and repeatedly. Advantages include defining main components at the beginning on the design process, resulting in a well structured design. However, some issues may be encountered with this design, such that it is not always possible to split bigger problems into a smaller sub-set of problems.

A bottom-up design takes the opposite approach. The design begins with defining the components or modules before they are connected together to create larger components or systems. This process is repeated until the full system has been constructed. Advantages of this design includes a high degree of flexibility since individual components can be altered that are unlikely to impact upon the whole system. However, developers may encounter challenges when trying to ensure the components work together due to a limited vision of the system as a whole in the initial stages.

When the function of the programme is the main priority, Function Orientated Design is employed. This design is based on 'stepwise refinement' which is a top-down approach. Using this approach, we begin with a high-level system description before elaborating on and refining the lower level details.  


3. In which design methodology would a class diagram be most useful?


A class diagram would be most useful in Object-Oriented Design. This is due to the class-diagram's ability to depict the static structure of an application, the relationships between classes, and the structural and behavioural characteristics of the objects of a class.

Class diagrams are not as useful in Structured Design since it focuses on splitting a large system into smaller elements which is more suited to the use of flowcharts and data flow diagrams. Similarly, Function Oriented Design focuses more heavily on the function of a system.


4. What are the four pillars of object oriented programming? Give a single-sentence description of each.


The four pillars of object-orientated programming are:

- Abstraction: The complexity of an object is reduced since irrelevant data is omitted, creating an abstract representation of the object. 
- Encapsulation: Restricts access to object's components/internal details by 'bundling' data and its associated methods within a class into a single unit.
- Inheritance: A class can acquire the properties and behaviours (methods) of another class, creating a class hierarchy.
- Polymorphism: The ability of an object to take on multiple forms, providing its own unique implementation of the methods of a class.


5. What is the strategy pattern? How would its implementation differ between a functional and object oriented system?


A strategy pattern is a design pattern in which the behaviour of an object can be altered at run time. Therefore, an object can select from a variety of algorithms and behaviours as opposed to doing so statically. The foundation of the strategy design pattern is based on composition; is establishes a family of algorithms, encapsulates each individual algorithm, and allows them to be switched between at run time. The fundamental concept behind this pattern is to ensure that the algorithm is independent of the main object. Therefore, this enables the object to assign the behaviour of the algorithm to one of its strategies.

A strategy pattern is composed of three main components:
- Algorithm: Takes an input, performs operations on this input, and produces an output.
- Strategy: An interface used by all algorithms.
- Context: A parent process or run-time environment that attempts to use an alternative algorithm in response to specific circumstances.

In an object-oriented system, classes and interfaces will be used. However, in a functional orientated system, interfaces and different strategy classes are not necessary. Instead, functional orientated systems use only functions to implement strategy pattern. Higher-Order functions are those that can take one or multiple functions as parameters and, resultantly, return a function. Thus, this enables us to represent an abstraction comparable to that offered by an object-orientated interface. Syntax that is less specific to object-oriented programming is advantageous since it is shorter and easier to understand, especially when there are complex implementations.


6. Imagine you are creating a new online payment system. In order to gain maximum market share it can't be tied to a particular sector - it needs to work just as well when ordering a takeaway as when buying a new coat. Which design methodology would you suggest following? Give some justification for your decision.


An object-oriented design would provide the greatest flexibility, adaptability, and scalability that is required in the online payment system since it is not tied to a particular sector. 

Object-oriented programming utilises inheritance and polymorphism which could allow different payment methods to be used, such as credit cards and debit cards, which may be necessary across different sectors. For example, a paymentMethod parent class could be created which makes it possible to share similar functions, with the child classes implementing more specific methods for payments. Creating classes in this way is advantageous since it makes code readable, organised, and allows for code to be extended if necessary. An interface could also be used if there is a need to support different currencies in the system. This could allow for different currency conversion methods and promotes loose coupling within the system, making the system flexible and maintainable.

Moreover, object-oriented programming allows for the system to be easily extended without significantly affecting the codebase. This aligns with the open-closed principle, in which the payment system would be open for extension but closed for modification. Therefore, new payment methods could be added with ease without altering existing code, limiting the introduction of bugs. 