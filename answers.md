## What does it mean for a method to "return" a value?

The return value is what an invoked method will be equal to. It is often indicated by the keyword `return`, or in some langauges is implicity done with the last line of a method.

## What is the difference between a procedure, a function, and a method?

A procedure is a set of statements that can be repeated on demand. A function takes inputs and transforms them into an output. A method is a procedure that is stored on an object.

## What's the difference between a hash and an array?

A hash is a collection of keys and their values. Values can be accessed by their key. An array is an indexed list of values. Elements can be accessed by their index. Hashes and arrays have different operations that can be performed on them.

## What's the difference between a hash and an object?

A hash is a collections of keys and their values. An object is a collection of state and behavior, and is an instance of a class. JavaScript "Objects" are more accurately described as hashes or dictionaries.

## When should you use map? Select? Reduce? Find?

* Map: Transform a collection into a different collection of the same size
* Reduce: Accumulate a collection into a single value
* Select/Filter: Retrieve only the items from a collection that match a condition
* Find: Retrieve the first item from a collection that matches a condition

## What's the difference between a class and an instance of a class?

A class is a blueprint for creating objects that share similar state and behavior. An instance is a concrete implementation of a class, also called an object.

## What's the difference between an instance method and a class method?

An instance method belongs to an object, and cannot be called on the class itself. A class method is owned by the class, and cannot be called on any one instance.

## What is a gem? Gemfile? Gemfile.lock?

* A gem is a collection of code that has been packaged for easy installation and reuse
* A Gemfile is a list of gems, their approximate versions, and which environments require them
* A Gemfile.lock is a list of gems, their _exact_ versions, and which environments require them

## What is a one to many relationship? Many to many?

A one to many relationship indicates that an entity can relate to many instances of another entity, but each one of them _only_ relates to one instance. In a many to many relationship, each entity can have an arbitrary number of relationships with the other entity.

## How does a database relate 2 tables?

A column in dependent table will store an independent tables's primary key as a foreign key. The database can only store values in the foreign key column that also exist as primary keys in the independent table. For example, if table A has primary keys 1, 3, and 5 and table B has a foreign key column that references table A, then 1, 3, 5 are the only legal values for that column.

## What does "single source of truth" mean in terms of related objects?

A single source of truth refers to coincidences of two objects in a many-to-many relationship. When querying an object to find out about its relations, the single source of truth is consulted instead of any of the related entities themselves.

## What is the purpose of the environment.rb file?

An environment.rb file imports all of the libraries and classes that should be available to the program at run time.

## What does an ORM do?

An object-relational mapper takes object relationships, which are have has-many/belongs-to relationships, and translates them to foreign-key relationships (and vice-versa). This is necessary because object data is naturally nested, and relational data is naturally flat.

## What is an API?

An API defines a contract where when a certain output or state change will be given if a particular input is provided. Also refers generically to web services, which are APIs that are accessed via HTTP.

## What is semantic HTML?

Semantic HTML refers to using and organizing HTML elements by their meaning and purpose, rather by their intended visual appearance. It became popular after HTML5, which introduced a variety of new semantic elements and repurposed several visual elements.

## What is the DOM?

The DOM is the browser's representation of an HTML document and its styles. It provides a way to programatically access and manipulate these. It is internally represented as a tree. It provides an eventing interface for its nodes as well.

## Describe the HTTP Request/Response cycle

A client issues an HTTP request to an HTTP server, which fulfills the request with an HTTP response. Every request is expected to have a matching response. If a response is not given within an expected timeframe (the "timeout"), it is considered failed. Clients can be browsers or computers that are also acting as servers for other requests.

## What's the difference between the web and the internet?

The internet is a network of networks. It's technologies and protocols that allow these computers to send messages and data to each other. Components include the TCP/IP protocols, the physical cabling connecting the computers, the IP address system, and DNS. The web is a system of technologies built on top of this, and includes browsers, HTML, CSS, JavaScript.

## What is validation, where can it occur, and what purpose does it serve?

Validation ensures the integrity of supplied data. It can be done:

* In the browser, via form validation. This helps the user enter data correctly.
* On the server, via things like strong params and model validations in Rails. These ensure that data supplied by a client is valid and nothing has been maliciously added.

## What is an event?

An event fires when an action occurs on a DOM node. These are often user-initiated (such as clicks or hovers), but may be system initiated (such as network request completing or the browser finishing loading the DOM). These events can be listened to, and functions can be executed in response.

## What is event bubbling?

When an event fires on a DOM node, it also fires on each of the parents of that DOM node sequentially. Each node can listen for the event and respond in turn, as well as stop the event from continuing to bubble.

## What is referential transparency?

Referential transparency is when an expression is equivalent to what the expression evaluates to. In other words, any valid operation on the result of an expression can be done on the expression itself.

## What are the 4 pillars of OOP?

* Encapsulation - An object's state and behavior are contained together, and access to an object's state is managed by the object's methods.
* Inheritance - An object's state and behavior can be further extend by other objects.
* Polymorphism - Two methods can share a name, but have different implementations. This can be achieved by having different method signatures with different bodies (overloading), or by changing the behavior of a method in a subclass (overriding).
* Abstraction - Hiding implementation details between public interfaces. Other objects don't need to know how something is done, only the contract that will be adhered to.

## What are some tenets of functional programming?

* Immutability - Values cannot be reassigned or modified once set
* Disciplined state - Wrapping state changes as tightly as possible, and pushing side effects to the end
* Pure functions - No side effects, no indirect input, outputs are deterministic
* First class functions - Function definitions can be stored and passed like any other value
* Higher-order functions - Functions can accept functions as arguments, return them, or both
* Referential transparency - Expressions are equivalent to what they evaluate to
* Type systems - Custom types can be defined that conform to predictable rules

## What's the difference between authentication and authorization?

Authentication is who you are, authorization is what you can do. For example, you may authenticate that a particular user is who they say they are based on their knowledge of a password, biometric identification, or ability to login to a social network you trust, and you may additionally authorize that user to delete any data they want.

## How do you avoid storing plain-text passwords?

By hashing a user's password upon account creation and storing the hashed password instead of the plain-text one. When a user logins and supplies their original password, you hash that password and compare it to the one you initially stored.

## What is serialization?

Turning a complex data structure, such as an object or hash, into a string. This is useful when passing or storing data through something that doesn't have types (such as HTTP or localStorage).

## Describe the MVC architecture pattern

A popular way of organizing code that emphasizes separation of concerns.

* Models - Manage the structure of data, as well as rules and meethods for storing and accessing it. Aware of neither models nor views.
* Views - Manage the presentation of data. Aware of neither models nor views.
* Controllers - Manage interactions. Interacts with models, sets data on views.

## What is Big O?

A way of describing how the time or memory needed to execute an algorithm grows with respect to the number of inputs. For example:

* An algorithm with a time complexity of O(1) will take the same amount of time to run no matter how many inputs are given.
* An algorithm with a time complexity of O(n) will take proportionally longer to run when given more inputs
* An algorithm with a time complexity of O(n^2) will take exponentially longer to run when given more inputs

## What is a closure?

When an inner scope accesses an outer scope after the outer scope has finished executing. For example, a function inside of a function can hold a reference to a variable that was declared in the outer function after the outer function has completed. The inner function "closed over" the outer function's scope, or accessed it via closure.

## What is CORS?

Cross-origin resource sharing. It's a method for safely allowing browsers to trust resources that come from a different domain that resulted from a script. It works by including an `Access-Control-Allow-Origin` header on HTTP responses that either explicitly white-lists the domain or implicitly includes it via a pattern.

## What's the semantic difference between PUT and PATCH?

PUT is for replacing one resource with another, PATCH is for modifying parts of a resource in-place.

## What is DRY?

"Don't repeat yourself", or consolidating implementations that are intended to do the same thing.
