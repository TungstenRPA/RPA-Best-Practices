# Build an XML/JSON/CSV file from SQL data
  * Make sure the XML variable is global. This allows you to build the XML with each loop through the database results, without the XML variable being reset.  
![image](https://user-images.githubusercontent.com/47416964/159470065-b243c11c-542f-4521-ad3a-6e3d56fba0ff.png)
  * The SQL query ``` SELECT objectkey FROM Person where ... ``` retrieves the object keys you need. Mape the objectkey to **person.id**
  * **Find Person in Database** returns the entire database entry into an object.  
![image](https://user-images.githubusercontent.com/47416964/159470491-667f1fab-7c25-430f-8fd0-83f8e6faa8ed.png)
  * **Insert Content into XML** stores the *person*  object into the XML variable.
  * In the **Write Log** branch, your XML variable is ready.
![image](https://user-images.githubusercontent.com/47416964/159469956-fb972e00-7f40-49c5-bcc3-1d858c8acb47.png)
