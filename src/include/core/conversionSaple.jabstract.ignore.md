```javascript 
/*
this file is an example of how data can be converted using multiple inheritance
*/
//readfirst !!
//@include Object.jabstract.md
ns sample {
///this allow the object to use multiple inheritance
class Person:CoreMultipleInheritanceObject{
// public constructor
  Person(){
      Convertors.Add("ToPersoanaJuridica",
            new CoreRegisteredDataConvertor(typeof(PersoanaJuridica),this.Type,StaticConvertor.Conversie1Callback);
  }
  
  //private destructor ? // public destructor ?
}
class PersonUsage {
///this is a sample of how data is dynamic converted !!!!
  convert(){
    
    originalPerson=new Person();
    
    return (PersoanaJuridica)originalPerson.Convertors.FindConvertor("ToPersoanaJuridica")(originalPerson);
    
  }
  ///this is a sample of how data is dynamic converted !!!!
  ///this is also correct
  //@return PersoanaJuridica
  convert2(){
    
    originalPerson=new Person();
    
    return originalPerson.Convertors.FindConvertor("ToPersoanaJuridica")(originalPerson);
    
  }
  //and this is also correct
  convert3(){
    
    originalPerson=new Person();
    
    return originalPerson.Convertors.FindConvertor("ToPersoanaJuridica")(originalPerson);
    
  }
  
}
}
```
