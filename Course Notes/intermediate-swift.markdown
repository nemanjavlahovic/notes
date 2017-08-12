## Intermediate Swift 3

by Brian Moakley on raywenderlich.com

### Chapter 2: Closures
* Difference between a closure and a function is that a closure doesn't have a name.
* You use closures by assigning them to a variable.
* in keyword is the separator between the header and the body of a closure.
* Swift knows that there is a return value if you specified in a variable, so there is no need to write "return" in a closure body.
* Best practice is to use closure as a last parameter in a function.

### Chapter 3: Structures
* Structs are value types.
* Structs can have functions.
* By default structs are immutable, and if you want to change internal data through a function - you must specify mutating keyword before func.

### Chapter 4: Properties
* Properties are variables that are included with objects.
* When you add properties to struct, it provides default initializer for you.
* Computed properties are read only, there is no way you can assign value.
* Type properties are properties assigned to all of the instances of the type, rather than individual instance. In Swift this is called static variable.
* Getters provide oldValue variable, while setters provide newValue.
* Property observers are sent from heaven.

### Chapter 5: Classes
* Unlike structs, classes need to have initializer implemented or have default values.
* When you create immutable instance of a reference type, ie: let location = Location(), you can still change the values of properties, but you can't assign another object to that variable.
* When you are comparing classes, you are comparing references to these objects. Operator === is used for comparing references.
* You want your User/Player objects to be reference type, because you don't want to have copies of these objects.
* When in doubt, start with a struct and migrate to a class if needed later.

### Chapter 6: Inheritance
* If you don't want your class to be subclassed, but final keyword before class and its name.

### Chapter 7: Initializers
* With convenience initializer you can limit amount of properties necessary for initialization of an object. For instance, you can provide a default value for user first name and last name, but create a convenience init for setting score.
* Once you add your own initializer, default initializer goes away. You can't create an instance without calling an init and providing values. var story = Story() becomes unavailable, but you can call Story(name: String).

### Chapter 8: Protocols
* To provide a functionality for a method defined in a protocol you use protocol extensions.
* Protocols just define behavior, not the implementation.
* When creating array, you can define it so it can only accept objects that conform to certain protocols. var vehicles: [Vehicle] = []
* Implementing CustomStringConvertible on your own objects makes it easier for making custom debug description. You define it through debugDescription variable.

### Chapter 9: Enumerations
* Enums can have all kinds of value types, strings, ints etc.
* You access enumeration value by calling enumCase.rawValue.
