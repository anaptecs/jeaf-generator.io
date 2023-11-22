# JEAF Generator
## Introduction
JEAF Generator can be used for code generation based on UML models. JEAF Generator supports a wide variety of artifacts that can be generated like Services, REST Resources, POJO's, OpenAPI specs, persistent classes and many more ...

As JEAF Generator is designed to be used in all kinds of enterprise projects it offers a large set of features that are required to provide scalable, high performant enterprise applications.

Even though they are closely connected, JEAF Generator is not limited to JEAF Framework. Almost all features are also supported for Spring / Spring Boot.

JEAF Generator is provided as Maven Plugin. Using Maven it can be integrated into your projects very easily. Main input for JEAF Generator is an XMI Export of your UML model. In addition you have to configure for Maven Plugin which parts of the model should be taken into account during the generation process and what should be generated. 

Example: 
* Code generation should only be done for Service Objects and classes that are located in package `com.anaptecs.jeaf.accounting` and below