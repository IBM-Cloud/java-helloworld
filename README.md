# Java Hello World Sample

This project contains a simple servlet application.

[![Deploy to Bluemix](https://bluemix.net/deploy/button.png)](https://bluemix.net/deploy?repository=https://github.com/IBM-Bluemix/java-helloworld)

## Running the application locally in Eclipse with Liberty

1. Download and install [IBM Eclipse Tools for Bluemix](https://developer.ibm.com/wasdev/downloads/#asset/tools-IBM_Eclipse_Tools_for_Bluemix).
2. In the Servers view of Eclipse, right-click to create a new WAS Liberty server. Follow the steps in the wizard, which includes the option to download and install the WAS Liberty runtime.
3. Import this sample into Eclipse using *File -> Import -> Maven -> Existing Maven Projects* option.
4. Deploy the sample into Liberty server. Right click on the *JavaHelloWorldApp* sample and select *Run As -> Run on Server* option. Find and select the Liberty profile server and press *Finish*. 
5. Go to: [http://localhost:9080/JavaHelloWorldApp](http://localhost:9080/JavaHelloWorldApp)

## Running the application in Bluemix using Eclipse

1. Download and install [IBM Eclipse Tools for Bluemix](https://developer.ibm.com/wasdev/downloads/#asset/tools-IBM_Eclipse_Tools_for_Bluemix).
2. In the Servers view of Eclipse, right-click to create a new IBM Bluemix server. Follow the steps in the wizard.
3. Import this sample into Eclipse using *File -> Import -> Maven -> Existing Maven Projects* option.
4. Deploy the sample into Bluemix server. Right click on the *JavaHelloWorldApp* sample and select *Run As -> Run on Server* option. Find and select the Bluemix server and press *Finish*. 


## Running the application using the command-line

This project can be built with [Apache Maven](http://maven.apache.org/). The project uses [Liberty Maven Plug-in][] to automatically download and install Liberty from the [Liberty repository](https://developer.ibm.com/wasdev/downloads/). Liberty Maven Plug-in is also used to create, configure, and run the application on the Liberty server. 

Use the following steps to run the application locally:

1. Execute full Maven build to create the `target/JavaHelloWorldApp.war` file:
    ```bash
    $ mvn clean install
    ```

2. Download and install Liberty, then use it to run the built application from step 1:
    ```bash
    $ mvn liberty:run-server
    ```

    Once the server is running, the application will be available under [http://localhost:9080/JavaHelloWorldApp](http://localhost:9080/JavaHelloWorldApp).

Use the following command to run the built application in Bluemix:
    ```bash
    $ cf push <appname> -p target/JavaHelloWorldApp.war
    ```
## Liberty App Accelerator

For help generating other Liberty samples checkout the Liberty App Accelerator at [wasdev.net/accelerate](http://wasdev.net/accelerate)

[Liberty Maven Plug-in]: https://github.com/WASdev/ci.maven
