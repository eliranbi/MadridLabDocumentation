Introduction
============

This set of labs we will demonstrate how to take an existing Ionic/Cordova application and add the MobileFirst Platform v8.0 Cordova Plugin as well as demonstrate some of the capabilities provided by MobileFirst. The lab will cover bootstrapping, application customization, using MFP 8.0 adapters, MFP 8.0 Operational Analytics, custom report and more.

The activity will start with an Ionic project that has already been created (see git repo below). The application is an Employee Directory application, named IBMEmployeeApp

The following exercise includes 11 micro labs (\~20 min each)

-   Lab \# 1 - Understand the Ionic application and learn how to customize it

-   Lab \# 2 - Use Cordova CLI to add the new MFP v8.0 Cordova Plugin

-   Lab \# 3 - Load MFP framework and application Bootstrapping

-   Lab \# 4 - Use MFP CLI to register and manage your application

-   Lab \# 5 - Using MFP adapters frameworks (Server Side)

-   Lab \# 6 - Using MFP adapters frameworks (Client side)

-   Lab \# 7 - Overview MFP Operational Analytics

-   Lab \# 8 - How to capture custom events

-   Lab \# 9 - How to create custom charts and alerts.

-   Lab \# 10 - How to secure your application (Server side)

-   Lab \# 11 - How to secure your application (Client side)  

### Source code for labs

In order to get the latest code for the ionic application, run the following git command:

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
git clone https://github.com/eliranbi/IBMEmployeeApp
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To get the latest documentation, code snippets and adapter code, run the following git
command:

```
git clone https://github.com/eliranbi/MadridLabME13-15.git
```

The following directories are available once the repository has been cloned :


Once you clone the repo you will notice the following directories :

-   **AdapterServices** - This folder contains the MFP adapter project for implementing the back-end integration code.

-   **IBMEmployeeApp** - This folder contains the user interface project built using the [Ionic framework](http://ionicframework.com).

-   **LabDocuments** - This folder contains the workbooks for his lab.
-   **snippets** - This folder contains a collection of copy/paste fragments to simplify making the required source code changes in the labs. They are labeled by lab name and task, and should be easy to locate and use.the snippets code foe the lab. 
    

### Tools used in labs

This lab requires the following tools :

1.  The **MFP** mfpdev Command Line Interface (CLI) to interact with the MobileFirst Platform, create projects, create adapters, deploy to the mfp server, and view the **MFP** console etc.

1.  Choice of IDEs to edit code. Either choose the **Brackets IDE** or the **IntelliJ IDEA** IDE.

	The **Brackets IDE** was used throughout these labs and can be downloaded from here : <http://brackets.io>. Brackets is a modern, open source text editor that understands web design. Use the Brackets Extension manager to install additional plugins for code assistant and live preview. The extensions that are used in this tutorial are:

    -   ionic-brackets.

    -   Ionic Framework Code Hinting.

    -   Brackets Beautify

	<img src=images/Intro-03-brackets-extensions.png width=600>

	The **IntelliJ IDEA** will be used to create a MFP adapter and uset the built-in Maven project features, IntelliJ IDEA is a Java integrated development environment (IDE) for developing computer software. It is developed by JetBrains, and is available as an Apache 2 Licensed community edition. [https://www.jetbrains.com/idea/download/](https://www.jetbrains.com/idea/download/)

	<img src=images/Intro-Intellij.png width=600>

4. **Cordova** command line interface (CLI), This tool allows you to create new projects, build them on different platforms, and run on real devices or within emulators. The CLI is the main tool to use for the cross-platform workflow
5. **Ionic Framework** command line interface (CLI), The Ionic Framework command line utility makes it easy to start, build, run, and emulate Ionic apps. 


### Preview the Ionic app

Before we can start with preview our existing Ionic Employee Directory application, we need to get to the begining stage of our application, follow the steps below: 

1.  Start a command line terminal (i.e. `cmd` on Windows or `terminal` on OS X
    and Linux).

2.  Change context to the IBMEmployeeApp directory:

    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    cd IBMEmployeeApp
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

3.  In order to start from a known point for the first lab run the following
    command:

    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
    git checkout -f step-0
    ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


### Start by previewing the existing Ionic Employee Directory application.

1.  Start Brackets and choose “Open folder” and select the IBMEmployeeApp folder.

	<img src=images/Intro-04-open.png width=400>


2.  Use the Brackets file Navigator to locate and click on **IBMEmployeeApp/www/index.html**.

3.  Click the **lighting** icon in the upper right portion of the Brackets window to preview the completed application in the browser.

    <img src=images/Intro-05-brackets-icons.png width=80>

For the username and password use the combination of **demo/demo** to login

<img src=images/Intro-05.1-app-login.png width=220>
<img src=images/Intro-06-app-splash.png width=220>
<img src=images/Intro-07-app-list.png.png width=220>
<img src=images/Intro-08-app-details.png width=220>
<img src=images/Intro-09-app-slider.png width=220>
  


### Summary

This lab demonstrated a complete and operational Ionic application. In the next lab will require a reset of the workspace workspace to a known starting point using `git checkout`. Each lab uses a `git check` with a tag to reset to a known and working condition should the need arise.
