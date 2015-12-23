```javascript
/*
this is a placeholder for  code ideas modeling common objects to be used on local accounting and management software

A business describe basicaly the juridic person you represent. For example you can be a network and have
*/

interface IBusiness{
  // a business must represent a juridic entity so it have attached microformats that represent info like
  
   IMicroformatsInfoCollection IdentityData;
  
   String BusinessId; // unique hash in order to be linked with other object
  // return public name from IdentityData Collection
   String GetPublicName();
  
   IDelegateList<String,IDelegate> AttachedActions; // actions that can be performed with this object and can be requested by name
    
    /*
    hold a list of different administration data for a business like:
    employees
    customers
    contracts
    
    each 
    */
    List<IAdministrationData> IAdministrativeData;
    
  
}

/*
this is the interface for management

this is the equivalent of a Administration business object
*/
interface IAdministrationData{
  String AdministrationDataId;
  IMicroformatsInfoCollection IdentityData;
  String getName();
  List<IFinancialDataCollection> FinancialData;
  
}

/*
represent a public 
*/
interface IFinancialDataColection {

}







class Product{

}
```
