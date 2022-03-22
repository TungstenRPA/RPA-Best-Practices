# Useful Videos
* [Configuring Kofax RPA for Microsoft SQL Server](https://kofax.app.bigtincan.com/pfiles/KkoeJP7wRa4bVZqMlg26tKhwTvcAfLcGg12YNx0OjGAzmp3yXW)
* [Creating/reading/updating/deleting data in SQL with Kofax RPA](https://kofax.app.bigtincan.com/pfiles/zj9eyoR347XnA2DLMEqptohWTdsPClhVglZ560dmbOPkQVNqGa)
* [Attended Robot with Kofax Transformation](https://kofax.app.bigtincan.com/pfiles/jdrRlDXkZ6Jn59w1OgoYt0heTqslCxhQBpoqN4WPzaYx72AQyG) 
* [Introduction to Robot Lifecycle Management](https://kofax.app.bigtincan.com/pfiles/3pKyn45JXwNMZLDVoBwatbheTNsqC1C0gjAzkQ2mr690aYRevP)
# Tips for Basic Engine Robots
* [Build XML, SON or CSV from database](Build%20XML%2CJSON%2CCSV%20from%20database.md)
# Tips for Robots (Desktop, Terminal, Chromium)
* Write very small robots that do only one task each. Coordinate them together with a Basic Engine Robot.  *R: means that it is a (Desktop) Robot.*  
![image](https://user-images.githubusercontent.com/47416964/159471729-faa30620-b691-424f-b00a-8c8054f2835a.png)
* [Prevent multiple Browsers opening while debugging a robot](Prevent%20Multiple%20Browsers.md).
* Always use **Location** guards wherever possible in a **Guarded Choice** Step. Avoid Wait guards and Tree Change guards. Watch [this video](https://kofax.app.bigtincan.com/pfiles/xmdrWZMQJvLG65K1yEW7tjFLtZCjUQFMEknz9oYw2O47plVXAq/f/1038408817) to see why!  
  *This example handles the case when a login succeeds, password is wrong (an expected behaviour), or something unknown happens (so we throw an exception to generate a error message in Robot logs)*  
![image](https://user-images.githubusercontent.com/47416964/159472902-89f92db6-e54a-4e42-8c68-ae369fa9c243.png)

# [RPA-Best-Practices Wiki](https://github.com/KofaxRPA/RPA-Best-Practices/wiki) (work in progress)
