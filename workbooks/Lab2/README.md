- - -
# Lab 2 - Use the Cordova CLI to add the MFP v8.0 Cordova Plugin

In this lab, we will use the Cordova CLI to add the MobileFirst Cordova plugin, These will be the typical steps you will need to go through when you want to add plugins to your application, adding the MobileFirst plugin will allow your app to use the MobileFirst platform different features. 
General Steps:

1. Within the Ionic application you will run Cordova CLI command to add the plugin.
2. Use the MobileFirst CLI to preview the application to make sure, the plugin was successfully added. 

##Steps

1. Change context into the MobileFirst project.

        cd IBMEmployeeApp        

2. **Add** the iOS platform, run the following command cordova platform add ios (we didn't check the platform folder to our git-repo so you will need to add it yourself) 

        cordova platform add ios
     <img src="images/Lab2-add-ios.png" width=500/>

3. **Run** the cordova plugin add cordova-plugin-mfp ( running this command will add some additional plugins to our project like: cordova-plugin-device, cordova-plugin, globalization	fetch.json, cordova-plugin-dialogs, cordova-plugin-mfp )

        cordova plugin add cordova-plugin-mfp
     <img src="images/Lab2-add-plugin.png" />

	>Note:  To be able to easily debug your application and view your application console log, run the following command to add the cordova console plugin 
	
		 cordova plugin add cordova-plugin-console

4. **Start** the mobile first server, navigate to your mobile first server installation folder and run the following command

        ./run.sh
       
  <img src="images/Lab2-mfp-server.png" width=500/>
  
5. **Run** the mfpdev app preview

        mfpdev app preview

  <img src="images/Lab2-run-mfpdev-preview.png"/>

6.  You will see the app start on your default browser

  <img src="images/Lab2-browser.png" width="250"/>

##Summary
In this lab, you enabled the MobileFirst Platform functionality for your existing Ionic/Cordova application by simply use the Cordova plugin add command
If you were unable to complete this lab, you can catch up by running this command: ** **You will still need to add the iOS platform and the mfp cordova plugin manually since the plugin folder is not committed to the git repo**

     git checkout -f step-2

   