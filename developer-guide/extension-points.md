---
title: "Developer Guide"
subtitle: "Extension Points"
toc: true
menubar: developer_guide_menu
---

## Introduction

JEAF Generator is extensible. First of all there is the possibility to use your own templates as extension or replacement of the provided ones.

However, there might be cases where the standard templates are fine for you in general, but you would like to have a small modification. In such cases writing your own templates might not be the desired option.

For such cases JEAF Generator has build in so called ***Extension Points***. Extension Points are hooks which are called by JEAF Generator during the code generation process.



## Extension Points

The following table describes the extension points as they are defined by version **`2`** of the JEAF Generator Extension Point API



| Extension Point                                              | Description                                                  | Examples                                                     | Applicable for UML model element | Target Output |
| ------------------------------------------------------------ | ------------------------------------------------------------ | ------------------------------------------------------------ | :------------------------------: | :-----------: |
| [**`AnnotationExtensionPoint`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/AnnotationExtensionPoint.xpt) | Extension Point can be used to add custom annotations to generated Java code. It can be used for types (e.g. classes, enumerations) as well as | - Add custom deprecation annotation to a class or property   |          `NamedElement`          |    `Java`     |
| [**`ClassExtensionPoint.xpt`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/ClassExtensionPoint.xpt) | Extension point can be used to customize generated classes in the following ways:<br>* Implemented interfaces<br>* Add code before and after every class property from the UML model<br>* Add custom operation to class or builder class<br>* Add code before and after every builder property from the UML model<br><br>For further details please have a look on the documentation in the sources. |                                                              |    `POJO` <br>`ServiceObject`    |    `Java`     |
| [**`JavaEnumerationExtensionPoint.xpt`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/JavaEnumerationExtensionPoint.xpt) | Extension point can be used to add literals to an enumeration that are not present in the UML model (aka "dynamic literals"). It's also supported that an enumeration has literals that are defined in the UML model and some others are added dynamically. | - Literals are dynamically resolved based on model elements that are tagged with a custom stereo |        `JEAFEnumeration`         |    `Java`     |
| [**`OpenAPIEnumExtensionPoint.ext`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/OpenAPIEnumExtensionPoint.ext) | Extension point can be used to add dynamic literals to enumeration definitions inside an  OpenAPI specification. | - Literals are dynamically resolved based on model elements that are tagged with a custom stereo |       `OpenAPIEnumeration`       |   `OpenAPI`   |
| [**`OpenAPISpecificationExtensionPoint.ext`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/OpenAPISpecificationExtensionPoint.ext) | Extension point can be used to customize generated OpenAPI specifications | - Add additional properties to the info section of an OpenAPI specification |     `OpenAPI3Specification`      |   `OpenAPI`   |
| [**`ServiceInterfaceExtensionPoint.xpt`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/ServiceInterfaceExtensionPoint.xpt) | Extension point can be used to customize generated service interfaces | - Add custom annotations to service interface or operations<br>- Add custom default implementation  for service operations |          `JEAFService`           |    `Java`     |



## How to implement extension points

<br>

### General considerations

Implementation of extension points is rather easy. All available extension points are located in resource directory **`jeafgenerator/api`**. For all extension points there is a default implementation that will be used when they are not overwritten. 

These default implementation are also intended to be your starting point. You can find there her: [JEAF Generator Extension API](https://github.com/anaptecs/jeaf-generator/tree/main/jeaf-generator/src/main/resources/jeafgenerator/api)

In order to avoid version clashes the JEAF Generator API is versioned in a very simple way. There is a special function in [**`JEAFGeneratorExtensionAPI.ext`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/JEAFGeneratorExtensionAPI.ext) that declares by using a simple integer value which version of extension API is supported by your implementation.

Currently version **`2`** is the latest version of the extension API.

<br>

### Steps to provide a custom implementation of extension points

| Step | Details                                                      |      |
| ---- | ------------------------------------------------------------ | ---- |
| 1.   | It's mandatory that you place your implementation of the extension points also in a resource directory with path **`jeafgenerator/api`**. Only then your templates etc. can be detected.<br><br>Same as with custom templates also your extension points need to be added to class path of JEAF Generator Maven Plugin |      |
| 2.   | You always have to implement extension point [**`JEAFGeneratorExtensionAPI.ext`**](https://github.com/anaptecs/jeaf-generator/blob/main/jeaf-generator/src/main/resources/jeafgenerator/api/JEAFGeneratorExtensionAPI.ext) so that JEAF Generator knows which version of the extension API is supported: |      |
| 3.   | Now you can pick the extension point that you want to customize from the list above.<br><br>For that, copy complete file with the default implementation of the extension point to your resources. Make sure to only change the functions / templates that should be customized. All the others need to be preserved as they are. |      |









