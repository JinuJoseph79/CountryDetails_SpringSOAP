# Project
CountryDetails_SpringSOAP is a sample project for SOAP web services.
SOAP is a messaging protocol. Messages (requests and responses) are XML documents over HTTP. The XML contract is defined by the WSDL (Web Services Description Language). 
It provides a set of rules to define the messages, bindings, operations, and location of the service.

There are two possible approaches when creating a web service: Contract-Last and Contract-First. Here contract-first is used and 
we start with the WSDL contract, from which we generate the Java classes.

spring-boot-starter-web-services and wsdl4j dependencies are needed.

## Getting Started
This repository contains the code for the CountryDetails application. The code can be cloned to local directory.

Dependencies:
spring-boot-starter-web
spring-boot-starter-web-services
wsdl4j dependencies:
 
## Features
CountryDetails application is implementing SOAP web services with spring boot. Countries.xsd file is used to create the Java classes.
jaxb2-maven-plugin helps to generate the java code.The plugin uses the XJC tool as code generation engine. XJC compiles the XSD schema file into fully annotated Java classes.
Four additional classes added are:

CountryEndpoint – the endpoint that replies to the request
CountryRepository – the repository at the backend to supply country data
WebServiceConfig – the configuration defining the required beans
SpringSoapApplicationn – the Spring Boot App to make our service available for consumption

When country name is passed as request, country details is returned in response

WSDL is used to define the structure of requests and responses.
http://localhost:8080/ws/countries.wsdl.

## Testing 
Launch the WSDL URL http://localhost:8080/ws/countries.wsdl.

To test install Wizdler in chrome. After installing Wizdler,launch the WSDL URL, http://localhost:8080/ws/students.wsdl.
We will see a small icon at the corner of the Chrome browser, which you can click to see the services that are part of the WSDL. 
Go ahead and click the Wizdler icon and click the service getCounrty. Pass the country name and then response will have counrty details.

Junit test - In ClientLiveTest we wired in the CountryClient bean defined in our CountryClientConfig. 
Then, we used its getCountry to invoke the remote service. The counrty details is then asserted.

## Technology used
spring-boot-starter-web-services- SOAP services

wsdl4j -The Web Services Description Language for Java Toolkit (WSDL4J) allows the creation, representation, and manipulation of WSDL documents.

Java API for XML Binding (JAXB) and Configuring a JAXB 2 Maven Plugin -We do the mapping from XML to Java and Java to XML.
This is done using JAXB — a Java API for XML binding. A Maven JAXB Plugin helps us in generating the Java objects based on the XSD. 

Jaxb2Marshaller -to set either the "contextPath" or the "classesToBeBound" property on this bean, possibly customize the marshaller
and unmarshaller by setting properties, schemas, adapters, and listeners, and to refer to it.

## Environment

Operation System: Windows 10

Java Version: Java 8
 


