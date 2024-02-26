# Design Methodologies

1.	***What do we mean by coupling and cohesion when discussing structured design?***

	Coupling refers to the level of interdependence between modules in a codebase. This dependence is based on the types of connections, complexity of the interfaces implemented by the modules and the type of information shared via connection. High coupling results in scenarios where changes in one module may affect others due to these connections. Low coupling allows modules to be altered with minimal effect on others. 
	
	Cohesion is a property of a single module, that refers to how well the various parts of a module work together to fulfill a single purpose. A module with high cohesion is focused in how it performs its purpose and the elements are all closely related. Low cohesion means the module serves more than one purpose and its elements are more separate.


2.	***What is the difference between top-down and bottom-up design? Which best describes a function oriented design?***

	When designing a system using the top-down approach, the highest level requirements are considered first and these are broken down into more concrete sub-components until no futher decomposition is necessary. The bottom-up approach is essentially the opposite of this. The lower-level components are developed first and then layers of abstraction are applied over them until the full system is formed and all requirements are met.
	
	In fucntion oriented design, the higher-level functionality of the software is established first and then the design is refined by designing the more detailed modules needed to fulfill each requirement. This naturally lends itself to a top-down approach.


3.	***In which design methodology would a class diagram be most useful?***

	A class diagram would be most useful when working within the object oriented design methodology, since it requires keeping track of the classes of all the objects and their relationships/dependencies.


4.	***What are the four pillars of object oriented programming? Give a single-sentence description of each.***

	* 	*Data Abstraction* – Keeping unnecessary data about an object hidden, to makes its behaviour and fucntion clearer. 
	*  *Encapsulation* – Enforcing the 'S' in SOLID, encapsulation is the process of storing data and its related functions in a single object.
	*  *Inheritance* – The ability to create subclasses/child classes from existing classes. Child classes will inherit behaviours and attributes from their parents classes, but these can be overridden within the child class.
	*  *Polymorphism* – The ability for objects to be treated differently based on how they are referenced/cast (e.g. an object being used interchangeably with an object from its parent class or one that implements the same interface). 

5.	***What is the strategy pattern? How would its implementation differ between a functional and object oriented system?***

	The strategy pattern is an approach to implementing algorithms that aims to maximise cohesion and loosen coupling. If you have a class that performs a particular task in a few different ways, each of the corresponding algorithms can be put into their own separate classes. The original class is known as `Context`, which will reference the desired algorithm as an object that implements a `Strategy` interface.
	
	This classic implementation is based on the OOP paradigm, but can be recontextualised for a function oriented system. A higher order fucntion can be used in lieu of an interface to call the relevant algorithm by taking the strategy as a parameter. 

6.	***Imagine your is creating a new online payment system. In order to gain maximum market share it can't be tied to a particular sector - it needs to work just as well when ordering a takeaway as when buying a new coat. Which design methodology would you suggest following? Give some justification for your decision.***

	I believe a structured design approach would make sense for this particular system. Our system will be more concerned with transforming data than storing it. Since we want the final product to work within various sectors, we will need to begin by establishing the higher-order functions that apply boradly and work down from there. The more subordinate modules can deal with specifics that may apply more to some retailers than others, so clients using the system who don't require those features are not burdened by them.