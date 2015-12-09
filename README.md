# businessCore
This is a collection of  representation of common business data to be used in order to generate core database and other representation of this kind of objects

## Specification
@todo
It have to be choosen an underline markup language and scripting engine details.

Our current proposal is to use xml representation and cover as much as possible of target languages (common denominator ) abilities. Class decorators like static, public, abstract, classic inheritance and classic polymorphism must be representable.

Also we will cover a more advanced inheritance and polimorphism - for example an country can be part of an address but also it can be an object for describing statistic. Our new polymorphism and inheritance will allow to use a single set of description and extend this object at runtime by adding additional "convertors" to other type of objects - this will be a facility of the core underline objects that all objects must be derived from.

there will be something like that(@todo):
```javascript
class Object1 {
  String property1;
  String property2;
  String accesingInternalInheritance(){
  String typename="an.external.type"
      Function internalConvertorFunction=Object.getInternalConvertorForType("an.external.type.",typeof(Object1));
      if(internalConvertorFunction)==null{
      //for example
      invertorConvertorFunction=function(typea,instance){
        //do something to convert
        return Object1
      };
      Object.addInternalConvertorForType("an.external.type",invertorConvertorFunction,typeof(Object1));
      }
      
      return "";
  }
  //here it can be another discusion about -it is attached by type or it is attached by instance 
}
```



We will define our own convertible "lowLevel" classes for: Object, String,  Number and DateTime in order to force a correct implementation of generator for example in order to fix processor aritmetics - so there will be big number aritmetics only. it is the choice of generator implementation how to do that.


Scripting:
At this moment we believe that is better to script using js. This means you will be able to use <link /> tag to reference external js ( most of them will be local, related to the source tree ) and  <script /> tag. Also that means all generators is required to parse js and generate code from js in order to implement some (if any) code.

It is the user choice to implement other kind of scripting but the main implementation engine (that we will provide) will fail to understand that code if no plugin provided.
@Maybe another kind of language, more simple will be created.


Rules of generation(@must be completed):
-everything is public until specified elsewhere. if not public, private or protected must be used.


#### Type notation
We will use java-like standard notation ( reverse domain notation ) for type. This is interesting also for the autodetection system of import 
@todo It must be figured out if the build system will autodetect files and dependencies based on actual import tags or it will have to be explicit writed down in a command file (like a build.xml (java like) or similar (vs studio, eclipse, netbeans )

As described elsewhere, there will be java/php like annotation for class decoration and ide type intelisense
for example

```javascript
///[SomeClassAnotationwith(parameters1="",parameters2="")]
///[AnotherAnnotationWithoutParames]
///[ItIsTheUserChoiceToFolowAnotherAnotationsorToIgnoreit]
class PublicClass{
  ///@Description
  ///Here it go
  ///@Todo
  ///More
  ///[@return ro.type.myType]
  ///it is not realy required as we use typed notation here
  ro.type.MyType MyFunction(String param1, String param2){
   return null; 
  }
}
```
It is the choice of the builder to specify another script language

###Core objects
There are in the wild some informations about how data is to be represented for example microformats.org cover a large part of business objects

##Client database
We recomend the use of sqlite in order to allow  database struct generation.
@todo a server emulation using ws server and application engine backend for sqlite in order to allow multiple acces to database in a db server like way
