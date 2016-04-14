- - -
# Lab 4 - Use MFP CLI to register and manage your application


The MobileFirst platform provide a web console that allow you to easily view and manage your application instances, platforms and versions, 
managing your application requires an application registration, registering your application will also allow you to securely connect to the MobileFirst server and will enable you to use the adapter framework and analytics capabilities of the MFP server.

##Steps

1. Open the **IBMEmployeeApp** project using your favorite IDE. You are going to copy some code from `snippets/lab4.js` file to the `app.js` file in your MobileFirst project.

  > Note:  You may use any IDE you like to perform the labs.  The examples shown use the Brackets IDE.

2. Open the **`app.js`** file in the folder **`IBMEmployeeApp/www/js`** locate the **wlCommonInit()** function and add the following code immediately after the last line of the code inside

  <img src="images/Lab4-wlcommoninit.png" width=500/>


   ``` javascript
  
	//Calling to the MobileFirst Server    
	WLAuthorizationManager.obtainAccessToken().then(
	        function (accessToken) {
	          console.log(">> Success - Connected to MobileFirst Server");          
	        },
	        function (error) {
	          console.log(">> Failed to connect to MobileFirst Server");          
	        }
	);
		 
			 


   ```
  
  Your code should look like this:
  
    <img src="images/Lab4-obtainAccessToken.png" width=500/>
    
      > Note:  That we are the **WLAuthorizationManager.obtainAccessToken()** method the btains an access token for the specified resource scope from the MobileFirst authorization server.
      **WLAuthorizationManager** class is instantiated as a singleton and can be used anywhere in the application to obtain the client ID and authorization header. It is also called internally to handle MobileFirst OAuth-based security model protocol.
      

	> Note:  That **WLAuthorizationManager.obtainAccessToken()** method replace the deprecated **WL.Client.connect()** method that been used in earlier version of MFP to establishes a connection to the MobileFirst       
  
3. Now before we can preview the application we need to register the application with the MobileFirst Server, **Run** the following command 

        mfpdev app register

  ![cli mfp create](images/Lab4-app-register.png)
        
4. The Operations Console is a browser-based interface through which you can manage artifacts deployed to your server.  View the **Operations Console** by running

        mfpdev server console


  ![cli mfp create](images/Lab4-mfp-console.png)

  The MobileFirst Operations Console will start in your default browser, you can see the application 'Employee' under the "Application" list on the  dashboard left side.

  <img src="images/Lab4-mfp-oc.png" width="650"/>

5. Use the cordova emulate command to preview the application on the emulator.

        cordova emulate

6. Let's take a look at the console logs, while the iOS simulator is selected press the Simulator's debug menu and select the "Open console logs option" 

  <img src="images/Lab4-debug.png" width=400/>


  Then in the search box on the top right corner enter ">>" you should be able to see the connection success message

  ![cli mfp start](images/Lab4-logs.png)
  
  As you can see the application was successfully connected to the MFP server.
  
7. Delete the ">>" and enter "Response Content" you will see that the server responded with "access_token"

  ![cli mfp console](images/Lab4-access-token.png)

8. Close the simulator and go back to the web console, lets take a look at the built-in management capabilities of the platform, you can also enter the following url in your browser  **http://localhost:9080/mfpconsole/index.html#/dashboard**

9. **Press** on the "Employee" application under the "Application" menu on the left side, you will see the Employee Management feature.

  ![cli mfp console](images/Lab4-manage.png)
  

10. **Select** "Access Disable" option
11. In the "URL of latest version" input filed simply enter "http://www.cnn.com"
12. In the "Default notification message*" enter "Application disabled, please download latest version"
	  
	![cli mfp console](images/Lab4-access-disable.png)	

13. Press the "Save button"

	![cli mfp console](images/Lab4-access-saved.png)


14. **Run** the application again using the cordova emulate command

        cordova emulate

	You should see the "Access disabled" notification when the application start.

	  <img src="images/Lab4-disabled-msg.png" width=280/>

15. **Press** the "Upgrade" button, you will see the browser on your phone open the cnn.com website.
		
	  <img src="images/Lab4-cnn.png" width=280/>
	
  
##Summary
In this lab, you added javascript code to connect to the MobileFirst server when the application start, and used the built-in management features of the platform.

If you were unable to complete this lab, you can catch up by running this command:

     git checkout -f step-4