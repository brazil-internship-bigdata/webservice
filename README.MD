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
**_/form/part_**             | POST message returning entire string           | `curl -X POST -F "part=part1"  http://localhost:8080/multipart-webapp/form/part`
**_/form/part-file-name_**   | POST message returning part filename string.   | Be sure to execute this curl from project directory where pom.xml resides
                             |                                                | `curl -X POST -F "part=@pom.xml"  http://localhost:8080/multipart-webapp/form/part-file-name`
**_/form/xml-jaxb-part_**    | POST message returning xml jaxb part string.   | No curl sample available, please check test sources.

Application is configured by using web.xml, which registers
[javax.ws.rs.core.Application](https://jax-rs-spec.java.net/nonav/2.0/apidocs/javax/ws/rs/core/Application.html)
descendant to get classes and singletons from it (see class MyApplication).

Running the Example
-------------------

Run the example as follows:

>     mvn clean compile exec:java -Dcheckstyle.skip

This deploys the example using [Grizzly](http://grizzly.java.net/) container. You can access the application at:

- <http://localhost:8080/helloworld-webapp/helloworld>

