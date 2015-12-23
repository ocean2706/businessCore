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
    
    List<IManagementData> ManagementDataInfo;
    List<FinancialDataColection> FinancialDataCollection;
  
}

/*
this is the interface for management
*/
interface IManagementData{
  String ManagementDataId;
  IMicroformatsInfoCollection IdentityData;
  
}

/*
represent a public 
*/
public FinancialDataColection {

}







class Product{

}
```
