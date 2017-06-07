
# Webapp for participact 
========================


This webapp is based on sample of Jersey application available at https://jersey.github.io/download.html. The sample used to be the base of this webapp is multipart-webapp.

The aim of this webapp is to provide ktr and store data in CSV on a server. The service provide also a interface f monitoring 


Running the Example
-------------------

Run the example as follows:

>     mvn clean package jetty:run



Contents
--------

The base of the URI is :

[http://localhost:8080/multipart-webapp/]( /)

The mapping of the URI path space is presented in the following table:

URI path                         | Resource class                                 | HTTP methods
-------------------------------- | ---------------------------------------------- | --------------
**_/index.jsp_**                   | HTML page                                      | GET
**_/api/helloworld_**            | HelloWorldResource                             | GET
**_/api/helloworld_**   	     | HelloWorldResource                             | POST
**_/api/upload/csv_**            | UploadResource                                 | POST, set the file in the parameter 'file' in the body of the request                                 
**_/api/upload/ktr_**            | UploadResource                                 |POST, set the file in the parameter 'file' in the body of the request 
**
**_/api/download/ktr_**          | Download Resource                              |POST, set the file in the parameter 'file' in the body of the request 
**

Application is configured by using web.xml, which registers
[javax.ws.rs.core.Application](https://jax-rs-spec.java.net/nonav/2.0/apidocs/javax/ws/rs/core/Application.html)
descendant to get classes and singletons from it (see class MyApplication).




