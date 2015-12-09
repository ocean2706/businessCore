# businessCore
This is a collection of  representation of common business data to be used in order to generate core database and other representation of this kind of objects

## Specification
@todo
It have to be choosen an underline markup language and scripting engine details.

Our current proposal is to use xml representation and cover as much as possible of target languages (common denominator ) abilities. Class decorators like static, public, abstract, classic inheritance and classic polymorphism must be represented.

Also we will cover a more advanced inheritance and polimorphism - for example an country can be part of an address but also it can be an object for describing statistic. Our new polymorphism and inheritance will allow to use a single set of description and extend this object at runtime by adding additional "convertors" to other type of objects - this will be a facility of the core underline objects that all objects must be derived from. 

We will define our own convertible "lowLevel" classes for: Object, String,  Number and DateTime in order to force a correct implementation of generator in order to fix processor aritmetics - so there

#### Type notation
We will use java-like standard notation ( reverse domain notation ) for type. This is interesting also for the autodetection system of import 
@todo It must be figured out if the build system will autodetect files and dependencies based on actual import tags or it will have to be explicit writed down in a command file (like a build.xml (java like) or similar (vs studio, eclipse, netbeans )



###Core objects
There are in the wild some informations about how data is to be represented for example microformats.org cover a large part

##Client database
We recomend the use of sqlite for database structure
