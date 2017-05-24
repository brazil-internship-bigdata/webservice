Webapp for participact 
=========================

This webapp is based on sample of Jersey application available at https://jersey.github.io/download.html. The sample used to be the base of this webapp is multipart-webapp.

The aim of this webapp is to provide ktr and store data in CSV on a server. 


Contents
--------

The mapping of the URI path space is presented in the following table:

URI path                     | Resource class                                 | HTTP methods
---------------------------- | ---------------------------------------------- | --------------
**_/helloworld_**            | HelloWorldResource                             | GET
**_/helloworld_**   	     | HelloWorldResource                             | POST
**_/upload/csv_**            | MultipartResource                              | POST, in body of the request the parameter file is the file to upload                                          


Application is configured by using web.xml, which registers
[javax.ws.rs.core.Application](https://jax-rs-spec.java.net/nonav/2.0/apidocs/javax/ws/rs/core/Application.html)
descendant to get classes and singletons from it (see class MyApplication).

Running the Example
-------------------

Run the example as follows:

>     mvn clean compile exec:java -Dcheckstyle.skip

This deploys the example using [Grizzly](http://grizzly.java.net/) container. You can access the application at:

- <http://localhost:8080/helloworld-webapp/helloworld>

