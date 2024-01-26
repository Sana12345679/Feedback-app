 ![image](https://github.com/Sana12345679/Feedback-app/assets/118968494/267f826b-10e6-49a2-a69d-dc07eca19a92)

In mit app inventor I created the basic design of the feedback app by using the following components:
•	Webviewer: for viewing the thingspeak graph from the web page.
•	Horizontal arrangement tool: To place the images and the buttons side by side.
•	Image tool: For inserting the images.
•	Button tool: For creating two buttons to record the feedback given by the customers. I created two buttons GOOD and BAD. 
•	Web tool: For loading the API of things speak for sending the values.
•	 Clock sensor: For disabling the buttons for a delay of 15 sec.
Before proceeding to the block screen of mit app inventor things to do:
	In the Webviewer  in the homeurl we need to type the thingspeak graphs link : https://thingspeak.com/channels/1341092/charts/1?bgcolor=%23ffffff&color=%23d62020&dynamic=true&results=60&type=line&update=15
	To make the text bold check the bold option after clicking the button set the size to 20.
	We should set the clock to interval of 15000 msec by default it would of 1000 msec we have to change the timer.


![image](https://github.com/Sana12345679/Feedback-app/assets/118968494/06467cce-4f3f-44a0-af6f-c3bf1622d938)
     



 
The Block screen:
When we click the GOOD button the process to be done is determined by when Good. Click the 
•	Set the web1 to the URL to https://api.thingspeak.com/update?api_key=Q4GE2Z6U42CG5DRT&field1=1
•	Now call the web 1 URL by using call function call___.get
•	Now we should disable the GOOD button for about 15 sec so as the time gap in thingspeak must be considered for that we use set Good Enabled to False.
•	Even same we should block code should be written for the BAD button as once we click a button both feedback buttons should be disabled as no response is accepted on tingspeak platform for about 15 sec so using set BAD Enabled to False.
•	Now last but not the least set timer to enabled it has a delay of 15 sec



When we click the GOOD button the process to be done is determined by when Good. Click the 
	Set the web1 to the url to https://api.thingspeak.com/update?api_key=Q4GE2Z6U42CG5DRT&field1=0
	Now call the web 1 url by using call function call___.get.
	Now we should disable the BAD button for about 15 sec so as the time gap in thingspeak must be considered for that we use set BAD Enabled to False.
	Even same we should block code should be written for the GOOD button as once we click a button both feedback buttons should be disabled as no response is accepted on tingspeak platform for about 15 sec so using set GOOD Enabled to False.
	Now last but not the least set timer to enabled it has a delay of 15 sec.

Now when the timer countdown is completed, we use the when clock. Timer then
	Set GOOD and BAD to be enabled the as timer countdown is completed so for that we use.
	Set GOOD enabled to true.
	Set BAD enabled to false.

 





