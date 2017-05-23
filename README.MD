Helloworld webapp Example
=========================

This example demonstrates how to create simple Jersey application,
package it into WAR file and how to run it using [Grizzly
container](http://grizzly.java.net).

Contents
--------

The mapping of the URI path space is presented in the following table:

URI path            | Resource class       | HTTP methods
------------------- | -------------------- | --------------
**_/helloworld_**   | HelloWorldResource   | GET

Application is configured by using web.xml, which registers
[javax.ws.rs.core.Application](https://jax-rs-spec.java.net/nonav/2.0/apidocs/javax/ws/rs/core/Application.html)
descendant to get classes and singletons from it (see class MyApplication).

Running the Example
-------------------

Run the example as follows:

>     mvn clean compile exec:java -Dcheckstyle.skip

This deploys the example using [Grizzly](http://grizzly.java.net/) container. You can access the application at:

- <http://localhost:8080/base/helloworld>
