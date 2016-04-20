Lab 1 - Review Ionic Application & Customization
=======================================================================

This short lab (10min) introduces the Ionic application artifacts and code. 

Steps
-----

1.  Start a command line terminal (i.e. `cmd` on Windows or `terminal` on OS X and Linux).

1.  Change context to the IBMEmployeeApp directory:

    ```
cd IBMEmployeeApp
```

1.  In order to start from a known point for the first lab run the following command:

	```
git checkout -f step-0
```

	> **Note:** this checkout will also add the **/snippets** and **/extras** folders for use in the editing steps later on.

1.  Run the application using the Ionic serve command to start the default browser and point to **localhost:8100/\#/**. This will also track and reload any application code changes.

	```
ionic serve
```
	<img src=images/Lab1-00-ionic-serve.png width=480>
	
	<img src=images/Lab1-01-browser.png width=280>
 

1. Review the project structure on the left side 
	
	
	<img src=images/Lab1-02-app-dir.png width=280> 
  
	- **package.json** - contains all application dependencies.
	- **platfroms directory** - contains the added device platforms that have been added to the project (iOS, Android etc).
	- **plugins directory** - contains the different cordova plugins added to the project.
	- **resource directory** - contains the application splash screen and the app icon for the different platforms (default to Ionic)
	- **scss directory** - contains application color theme definitions.
	- **www directory** - contains application assets such as; css files, images, data files, html files, javascript files etc.
	- **lib directory** - contains the ionic libs and any additional libs that might add.
	- **index.html** - the main html file for the application.
	- **app.js** - the main javascript file for the application.
	- **controllers.js** - JavaScript file containing the controllers that have been defined for each page (view). See [Angular Controllers](https://docs.angularjs.org/guide/controller) for more information.
	- **services.js** - JavaScript file containing service, or network, calls used by the application. See [Angular Services](https://docs.angularjs.org/guide/services) for more information.

1. New review the index.html file

	<img src=images/Lab1-03-index.png>

	Notice that there are three different sections: 
	
	- The first section adds a reference to the Ionic framework css and javascript files along with reference to custom css style.
	- The second section adds a reference to the app.js, controllers.js and services.js files. These files include the application business, flow, and transaction logic.
	- The third section is the actual bootstrapping of the application. The bootstrap is performed by including the **ng-app** directive to auto bootstrap the app and **ng-controller** directive which attaches a controller class to the view. This is a key aspect of how angular supports the principles behind the Model-View-Controller design pattern.

> **To learn more**, visit the [ng-app](https://docs.angularjs.org/api/ng/directive/ngApp) and [ng-controller](https://docs.angularjs.org/api/ng/directive/ngController) sections of the Angular documentation.

Application Customization
-------	
The demo asset was built in a way that will allow easy customization to match the most common use cases for demos or POCs. The splash and login screens are easily modified by editing the exising PNG files to match a  company logo and color scheme.

The master detail list can represent anything from employees, bank accounts, car insurance policiesor or store locations. 

**Take a look at the image below:**

<img src=images/Lab1-04-splash.png>

- To change the **splash/login background** refer to section A
- To change/add **splash/login customer logo** or change the slogo/application name refer to section B
- To change the **buttons color scheme** refer to section C, you can find all the default Ionic color schemes at the following link: [http://ionicframework.com/docs/components/#buttons](http://ionicframework.com/docs/components/#buttons) 
	
8. Open the **splash.html** page under /pages/splash.html and customize your splash to the color scheme and the logo/application name of the last customer you have met.

9. If you look again in your browser you will see the ionic automatically apply and load your changes 


Summary
-------

This lab introduced the Ionic application source code and demonstrated how to easily customize the look and feel to match future POC or custom demo needs.

If you were unable to complete this lab, you can catch up by running this
command:

```
git checkout -f step-1
```