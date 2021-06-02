# Reading WebPages with Kofax RPA
Kofax RPA provides 3 different ways to access websites
1. With a **Web Robot** using the built-in webkit engine in Kofax RPA
1. With a **Desktop Robot** using the built-in [Chromium Embedded Framework](https://en.wikipedia.org/wiki/Chromium_Embedded_Framework). This does **not** require a Windows Desktop
1. With a **Desktop Robot** using a Windows Desktop and a Desktop Browser like Internet Explorer or Firefox.

Reasons why some Websites don’t work with Kofax RPA Web robots.
* The Website is actively fighting robots and is aware of you.
* The website uses client-side scripts to slow down and delay robots.
* The website has sloppy javascript on it. Chrome & Firefox allow invalid scripts to run – Kapow is a stricter browser.
* The website has cross-frame javascripts. 

* The website is archaic and only works because of some unknown bug in Internet Explorer.
* Kofax RPA's web robots freeze a browser page after executing a step and perform the next steps. Some webpages don't like being frozen because they have internal javascript timers.

## Steps to take to get a website working in Kofax RPA
1. Pretend to be an iPhone in a web robot. Some websites give you a simpler, mobile-friendly version of the website when they see you are an iPhone.  
![image](https://user-images.githubusercontent.com/47416964/120484462-64a48d00-c3b3-11eb-863f-5f981af7fb5e.png)
1. Find a good FREEZE condition.
  * Try a 30 second wait at first to see if that works at all.
  * Open Tools/BrowserTracer (F12) to see what the web page is waiting for.
  * Then replace it with an Element Appears or Disappears.  
![image](https://user-images.githubusercontent.com/47416964/120484684-9ae20c80-c3b3-11eb-8d4d-1b0b4e9ab04a.png)
2. Be a good javascript hacker
  * Open the page in Chrome/Firefox/Internet Explorer.
  * Use Debugging tools and Network Monitor to see how the web page is communicating with the server
  * Call that javascript directly from the robot  
![image](https://user-images.githubusercontent.com/47416964/120484832-bea55280-c3b3-11eb-9c36-fd9714d52ab3.png)
  * Or call the REST service directly  
![image](https://user-images.githubusercontent.com/47416964/120484865-c664f700-c3b3-11eb-956e-23eae4db4562.png)
  * Or call directly the HTTP that the javascript
2. Use Chromium in a Desktop Automation robot
  * This will almost certainly work as it is effectively a normal browser.
  * Some Google Sites (like Google Calendar) will not work like this. You will need to use Google Developer APIs.
2. Use a classic browser on a Windows Desktop
  * Do this if it requires Flash or Internet Explorer or ActiveX.






