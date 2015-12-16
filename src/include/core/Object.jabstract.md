```javascript
/*
this is a placeholder to represent a class that can be used as a core using a non existent language similar to ecma script /csharp etc
*/

namespace ro.businesscore.core{
/*
The name of the core class is NativeObject
in order not to polute possible implementations of for example java that use the term object
in java code generator for example , there will be a class NativeObject derived directly from java.Object class implementing 
but if somebody will implement a vm directly for the class tree, it can be maped directly to the internal native object representation (overcomming )
in businessCore everything is a NativeObject, including NativeString, NativeNumber or NativeDateTime.
*/
//@[Native]
//@[@ClassAlias Object] // this will alow us to use Object as a reference to NativeObject Type
class NativeObject{
  getType(){
  return this.internal.Type;
  }
}
/*
Multiple Inheritance Object is extending the  base object
in order to allow performance implementation for simple
objects that don`t need multiple transfromation as writed in the spec
*/
//@[Native]
class MultipleInheritanceObject:NativeObject{
    ConversionList<String,
}
//this allow us to use String internaly in businessClass but to refer to NativeString class and properties
//@[Native]
//@[@ClassAlias String]
class NativeString{

}

//a Number in businessClass is a NativeNumber in generated class !!! which is a BigNumber native (no js 0.1 to 0.2 arithmetic representation )
//@[Native]
//@[@ClassAlias Number]
class NativeNumber {
}
//@[Native]
//@[@ClassAlias DateTime]
class NativeDateTime {
}

//this class will be automated derived from NativeObject
/*class TimeSpan{
}
*/

/*
operators overloading must be described here
*/
}
```
