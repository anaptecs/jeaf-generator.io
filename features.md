---
title: "JEAF Generator"
subtitle: "Features"
description: JEAF Generator uses UML models to generate code for Spring, REST, Java, JakarataEE, JEE, Hibernate and others
toc_title: " "
menubar_toc: true
#menubar: empty_menu
---

# Features

JEAF Generator realizes the link between UML models and code.It is designed for enterprise projects and offers a large set of features to implement scalable, high-load, high-performance applications. 

JEAF Generator is provided as Maven Plugin. All required configurations can be done through the plugin configuration.

<br>

## Supported UML Modeling Tools

JEAF Generator uses UML models to generate code and configurations for various cases and target platforms. No matter what is the expected output, an UML model is always the input.

Currently the following UML modeling tools are supported: <sup>1)</sup>

* <a href="https://www.3ds.com/products-services/catia/products/no-magic/magicdraw/" target="_blank">**MagicDraw UML** (commercial)</a>
* <a href="https://projects.eclipse.org/projects/modeling.mdt.papyrus" target="_blank">**Eclipse Papyrus** (Open Source)</a>

<br>

<sup>1)</sup> *Enterprise Architect from Sparx Systems is not supported as it does not support the full UML 2.5 feature set. Unfortunately, some of the missing features are mandatory when you want to set up a feature rich, high quality model-driven process.*

<br>

## General Features

| Features                        | Description                                                                                                                                       | Additional Information                                                                                                                                       |
| ------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `Maven Integration`             | JEAF Generator is provided a Maven Plugin to easily integrate into your build process. All configurations are done via Maven Plugin configuration | - [Integrate JEAF Generator in Maven Build](developer-guide/maven-integration)<br>- [Maven Plugin Configuration](developer-guide/maven-plugin-configuration) |
| `Extensible generated code`     | Generated code can be extended with manual code                                                                                                   |                                                                                                                                                              |
| `Customer-specific extensions`  | In addition to the already integrated templates for code generation it is also possible to add custom templates and checks                        |                                                                                                                                                              |
| `Supports JakartaEE and JEE`    | Besides JakartaEE it is still supported to use legacy JEE types e.g. Validation Annotations                                                       |                                                                                                                                                              |
| `Configurable code formatting`  | The formatting of the generated code can be configured according to your rules.                                                                   |                                                                                                                                                              |
| `Configurable order of imports` | Ordering of imports and static imports can be configured according to your rules.                                                                 |                                                                                                                                                              |

<br>

## Java

| Features                             | Description                                                                             | Additional Information |
| ------------------------------------ | --------------------------------------------------------------------------------------- | ---------------------- |
| `POJO`                               | Generate POJO classes from a UML model. Generated code uses builder pattern by default. |                        |
| `Exception classes`                  |                                                                                         |                        |
| `Object Mappers`                     |                                                                                         |                        |
| `Java Bean Validation annotations`   |                                                                                         |                        |
| `Custom Java Validation Constraints` |                                                                                         |                        |
| `Builder Validation`                 |                                                                                         |                        |
| `Generate Java Generics`             |                                                                                         |                        |
| `Bi-directional assocations`         |                                                                                         |                        |
| `Soft Links`                         |                                                                                         |                        |
| `of(...) / valueOf(...)`             |                                                                                         |                        |
| `hashCode(...) / equals(...)`        |                                                                                         |                        |

<br>

## Jackson / JSON

| Features                      | Description | Additional Information |
| ----------------------------- | ----------- | ---------------------- |
| `Jackson annotations`         |             |                        |
| `Bi-directional associations` |             |                        |
| `ID based data deduplication` |             |                        |
| `JSON Serializers`            |             |                        |

<br>

## Spring

| Features                                             | Description                                                     | Additional Information |
| ---------------------------------------------------- | --------------------------------------------------------------- | ---------------------- |
| `Service Interfaces`                                 |                                                                 |                        |
| `REST Controller`                                    |                                                                 |                        |
| `Bean Params`                                        |                                                                 |                        |
| `Spring Security`                                    |                                                                 |                        |
| `Usage of generic response types for REST Resources` |                                                                 |                        |
| `REST Request / Response Validation`                 |                                                                 |                        |
| `REST Request / Response Logging`                    |                                                                 |                        |
| `Configure REST libraries (Spring Web MVC, JAX-RS)`  |                                                                 |                        |
| `REST Client`                                        | independent of REST Controller (client only), generic responses |                        |
| `Activity Interfaces / Implementation`               |                                                                 |                        |

<br>

## OpenAPI

| Features                                       | Description                                                                                   | Additional Information |
| ---------------------------------------------- | --------------------------------------------------------------------------------------------- | ---------------------- |
| `OpenAPI Specification`                        |                                                                                               |                        |
| `Split OpenAPI spec in multiple modules`       |                                                                                               |                        |
| `OpenAPI Data Types`                           | nice JSON (flat), no nested object structure in JSON representation but strong typing in Java |                        |
| `Mapping of generic response types to OpenAPI` |                                                                                               |                        |
| `OpenAPI Spec Validation`                      |                                                                                               |                        |

<br>

## Hibernate

| Features                                  | Description          | Additional Information |
| ----------------------------------------- | -------------------- | ---------------------- |
| `Hibernate Entities (Persistent Objects)` |                      |                        |
| `Hibernate OR-Mapping`                    | incl. fetch strategy |                        |
| `Bi-directional associations`             |                      |                        |
| `many-to-many relations`                  |                      |                        |
| `Hibernate Composite types`               |                      |                        |
| `Persistence Units`                       |                      |                        |

<br>

## JakartaEE / JEE

| Features                             | Description | Additional Information |
| ------------------------------------ | ----------- | ---------------------- |
| `REST Resources`                     |             |                        |
| `REST Request / Response Validation` |             |                        |
| `REST Request / Response Logging`    |             |                        |
| `Bean Params`                        |             |                        |

<br>

## JEAF Framework

| Features                               | Description | Additional Information |
| -------------------------------------- | ----------- | ---------------------- |
| `Service Interfaces`                   |             |                        |
| `Service Objects`                      |             |                        |
| `Domain Objects`                       |             |                        |
| `Service Proxies / REST Client`        |             |                        |
| `Service Provider Interfaces`          |             |                        |
| `Service Provider Implementation`      |             |                        |
| `Activity Interfaces / Implementation` |             |                        |
| `JEAF Components and Runtime classes`  |             |                        |
| `JUnit tests for JEAF Services`        |             |                        |

<br>

## Reports

| Features                  | Description                    | Additional Information |
| ------------------------- | ------------------------------ | ---------------------- |
| `Types Report`            | Business perspective, glossary |                        |
| `Breaking Changes Report` |                                |                        |
| `REST Deprecation Report` |                                |                        |
| `Java Deprecation Report` |                                |                        |
| `Security Roles Report`   |                                |                        |

<br>
