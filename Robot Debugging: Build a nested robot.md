Advanced Tips for building and debugging Robots. 
# Using **Nesting and Guards** to quickly build and debug a complex robot
Let's imagine that your robot has to do the following 5 steps
1. Open a browser.
2. Login to a website.
3. Search the website.
4. Loop through the results.
5. Logout of the Website.

You could build the robot like this :  
![image](https://user-images.githubusercontent.com/47416964/159478262-4cfa4175-d9e8-46a6-8615-2c0507440dde.png)  
but this is hard to debug. Everytime you want to restart debugging the robot will go back to the beginning and do all the previous steps, which is painful when you are building the loop or logout steps.  
Alternatively you could build the robot like this, where it quickly works out if the browser/desktop is ready for step 1, 3 or 4 and quickly resumes.  I have only shown two test steps, but you could add tests for all 5 steps.
![image](https://user-images.githubusercontent.com/47416964/159501830-ce785fa1-78e7-40a6-9bed-fbf38cbb3fbb.png)  
This technique also makes it easy to BUILD the robot.  
You build the first step(s) as normal    
![image](https://user-images.githubusercontent.com/47416964/159502910-397382cd-472e-4726-9f7f-1e0880552f55.png)  
and when they are working you wrap them in a Guarded Choice step  
![image](https://user-images.githubusercontent.com/47416964/159503104-521f4bc8-20e6-482d-83da-ba562410e63f.png)  
and then continue with the next step.  
![image](https://user-images.githubusercontent.com/47416964/159503229-37ad4a1b-4da1-4376-848f-81a2d2a983b2.png)  
and you keep repeating this until your robot is finishing. All the while you only have to debug the steps you are currently on.




