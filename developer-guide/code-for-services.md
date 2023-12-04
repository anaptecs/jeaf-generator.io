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

**Source Code Examples**

<details>
  <summary><code>AccountingService.java</code></summary>
<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Faccounting-services-api%2Fsrc-gen%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Faccounting%2FAccountingService.java&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</details>
<details>
  <summary><code>AccountingServiceProxy.java (JEAF Framework only)</code></summary>
<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Faccounting-services-api-runtime%2Fsrc-gen%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Faccounting%2FAccountingServiceProxy.java&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</details>
<br>

## Code for REST Services

<br>

## Code for Service Objects

JEAF Generator will generate a matching Java class for every service object (stereotype `«ServiceObject»`) from the UML model. Here we have to distinguish two cases: The service object does not define any operations or it does.

In case that the service object does not have any operations in the model then a Java class will be written to `src-gen` and thus is not intended to be edited (`Booking`). In case that the service object has at least one operation then two classes will be generated, an abstract base class that contains everything that can be generated (`UserAccountBase` in `src-gen`) and a concrete subclass that is intended to be implements manually and that will contain the implementation of the operation that is defined in the model (`UserAccount` in `src`).

No matter if the class has operations or not, every attribute and association from the model will also be added to the generated classes (please also refer to [General Behavior of JEAF Generator](../general-behavior). The generated code will also offer Builders to create new instances of the objects. Attributes and associations that are marked as final in the model can only be set using the Builder to create the object.

Depending on configuration parameter `generateJacksonAnnotations` it is also supported that JSON / Jackson annotations are generated for service objects, so that they can be serialized using Jackson Databinding.

<br>

For further information please also refer to:

- [How to model Services APIs - How-to-model-Service-Objects](../../uml-modeling-guide/how-to-model-rest-service-apis)

<br>

**Source Code Examples**
<details>
  <summary><code>Bank.java</code></summary>
<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Faccounting-service-objects%2Fsrc-gen%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Faccounting%2FBank.java&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</details>
<details>
  <summary><code>AccountBase.java</code></summary>
<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Faccounting-service-objects%2Fsrc-gen%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Faccounting%2FAccountBase.java&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</details>
<details>
  <summary><code>Account.java</code></summary>
<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Faccounting-service-objects%2Fsrc-gen%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Faccounting%2FAccount.java&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</details>