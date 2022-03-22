# How to prevent multiple browsers in (Desktop) Robots.
When you create a Browser Session in a Robot, it persists until the host Basic Engine Robot has ended. It is up to you to close a browser window. This gets awkward when debugging robots, because pressing the **Reset** button in the Debugger does not delete the browser window.
Here is how to automatically delete these browser windows.
1. Add a **Browse** step to a website and execute it.  
![image](https://user-images.githubusercontent.com/47416964/159475806-375d5262-a64f-4d50-88e9-69e7e03a5e83.png)
1. Press **Reset** so the cursor goes to the beginning of the Robot.  
![image](https://user-images.githubusercontent.com/47416964/159475909-9622d773-0d89-4025-8fc2-012d4466a664.png)
1. Scroll to the far-right of the Browser window and add a **Click** Step to the Browser's Close button.  
![image](https://user-images.githubusercontent.com/47416964/159476026-6c4c740d-ab0a-49d3-84a0-28d399c97aa2.png)
1. Replace the second guard in the **Left Click** step (it's really a **Guarded Choice** Step) with **Location Not Found**.  
![image](https://user-images.githubusercontent.com/47416964/159476242-f4fbf8b1-35e8-4ee7-a8ab-a1c0cb7f4327.png)
1. Delete the **Time Out Error** Step.  
![image](https://user-images.githubusercontent.com/47416964/159476350-20821fe6-c3aa-497f-89ba-18940c3c5335.png)
1. Copy the Top Guard (Which is looking for the Browser' Close button) and paste into the Bottom Guard.  
![image](https://user-images.githubusercontent.com/47416964/159476447-c4911661-6802-4ace-a240-17d8114f21af.png) ![image](https://user-images.githubusercontent.com/47416964/159476627-d67319eb-25d8-4aa4-8a1f-3b9252dbc522.png)
1. Rename the step to **Close Browser**.  
![image](https://user-images.githubusercontent.com/47416964/159476759-81ee1892-4782-4bd2-8f5f-1c903d5c4147.png)
1. Your Robot now looks like this. If it sees the close button in the browser it will click it, if it doesn't see it it will just continue. Collapse this step and happily ignore it. No more mulitple browser windows!
![image](https://user-images.githubusercontent.com/47416964/159477011-895bcd8a-43b6-409b-8fbf-74b132d0c6a7.png)



