---
title: "Developer Guide"
subtitle: "Generating Code for Services"
toc: true
menubar: developer_guide_menu
---

# Generating Code for Services

On this page you will find information about generated code for the following cases:

- Service Interfaces
- REST Services
- Service Objects
- Enumerations
- Exceptions
- Query Objects
- Load Strategy Objects

<br>

The diagram below shows the transformation of services, service objects, query objects and load strategy objects from the UML model into Java code.

![Code for Services](../../images/code_for_services.png)

<br>

## Code for Service Interfaces

As you can see in the diagram for every service (stereotype `«JEAF Service»`) in the UML model a matching Java interface will be generated. This interface will define exactly the same operations as they are defined in the UML model. Also all comments from the model will be present in the generated code.

In addition to the Java interface also also a so called `Service Proxy` will be generated for every service interface (class `AccountingServiceProxy` in example above). The service proxy is required for JEAF Core’s communication mechanism. The service proxy will be completely generated and is only required at runtime. Thus we propose to have separate Maven modules for services / service objects on the one hand and service runtime classes on the other one. If service runtime classes should be generated or not can be configured through the JEAF Generator Maven Plugin ([Integrate JEAF Generator into Maven Build - Configuration-Parameters-for-Services](../../developer-guide/maven-plugin-configuration/#configuration-parameters-for-services--rest-resources)).

<br>For further information please also refer to:

- [How to model Services APIs - How-to-model-Service-Interfaces](../../uml-modeling-guide/how-to-model-rest-service-apis)

<br>

**Source Code Examples **

<details>
  <summary>AccountingService.java</summary>
<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Faccounting-services-api%2Fsrc-gen%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Faccounting%2FAccountingService.java&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</details>

## Code for REST Services