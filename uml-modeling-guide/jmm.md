---
title: "UML Modeling Guide"
subtitle: "JEAF Generator Meta Model"
toc: false
menubar: uml_modeling_guide_menu
---

# JEAF Generator Meta Model

## Extension of UML Standard Meta Model

As described [in the introduction](../model-driven-software-development) the UML standard model is not meaningful enough to express everything that is needed for model driven software development. However UML defines a standard compliant way to extend its meta model. Therefore UML allows to define custom stereotypes.

Hereinafter all of JEAF’s extensions to the UML standard meta model will be called **“JEAF Generator Meta Model (JMM)”**.

<br>

## Stereotypes of JEAF Meta Model

The list below shows all stereotypes of JEAF Meta Model as they can be used for JEAF and JEAF Generator:<br>

- [Common Stereotypes](common-stereotypes)
- Service and Component Stereotypes
  - [«JEAF Service»](jeaf-service)
  - [«Service Object»](service-object)
  - [«Identifiable»](identifiable)
  - [«JEAF Enumeration»](jeaf-enumeration)
  - [«Application Exception»](application-execption)
  - [«System Exception»](system-exception)
  - [«Query Object»](query-object)
  - [«Load Strategy»](load-stratetgy)
  - [«REST Resource»](rest-resource)
  - [«REST Operation»](rest-operation)
  - [«Path Param»](path-param)
  - [«Header Param»](header-param)
  - [«Query Param»](query-param)
  - [«Cookie Param»](cookie-param)
  - [«Bean Param»](bean-param)
  - [«JEAF Component»](jeaf-component)
  - [«Domain Object»](domain-object)
  - [«POJO»](pojo)
  - [«Object Mapping»](object-mapping)
  - [«JEAF Activity»](jeaf-activity)
  - [«SecurityRole» (formerly named «JEAF Actor»)](security-role)
  - [«JEAF Service Provider»](jeaf-service-provider)
  - [«JEAF Service Provider Impl»](jeaf-service-provider-impl)
  - [«Interceptor»](interceptor)
- Persistence Stereotypes
  - [«Persistent Object»](persistent-object)
  - [«Field»](field)
  - [«Role»](role)
  - [«User Type»](user-type)
  - [«Persistence Unit»](persistence-unit)
- [Java Bean Validation Stereotypes](java-bean-validation-stereotypes)
- OpenAPI 3 Stereotypes
  - [«OpenAPI 3 Specification»](openapi-specification)
  - [«OpenAPI Type»](openapi-type)
  - [«OpenAPI Property»](openapi-property)
  - [«OpenAPI Example»](openapi-example)
  - [«OpenAPI Enumeration»](openapi-enumeration)
  - [«OpenAPI Server»](openapi-server)
  - [«OpenAPI Spec Reference»](openapi-spec-reference)

<br>

# Further information

Please also refer to [Model Driven Software Development](../model-driven-software-development)