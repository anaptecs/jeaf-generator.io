---
title: "UML Modeling Guide"
subtitle: "Stereotype «ObjectMapperFactory»"
toc: false
menubar: uml_modeling_guide_menu
---

# Stereotype `«ObjectMapperFactory»`
Stereotype «ObjectMapperFactory» can be used to define a complete Jackson ObjectMapperFactory. An object mapper factory consists of one or more module factories. This connection is defined using dependencies in UML.

<br>

| **Stereotype**          | `«ObjectMapperFactory»` | |
| ----------------------- | -------------- | |
| **Applicable Elements** | `Component`        |
| **Tagged Values**       |                       |                                                                                                                                                                                                          |
| **Name**                | **Type**              | **Description**                                                                                                                                                                                          |
| `defaultPropertyInclusion`   | `PropertyInclusion` |  |
| `enabledMapperFeatures`   | `MapperFeature` |  |
| `disabledMapperFeatures`   | `MapperFeature` |  |
| `enabledSerializationFeatures`   | `SerializationFeature` |  |
| `disabledSerializationFeatures`   | `SerializationFeature` |  |
| `enabledDeserializationFeatures`   | `DeserializationFeature` |  |
| `disabledDeserializationFeatures`   | `DeserializationFeature` |  |

<br>

For further information please refer to:
- [`«ModuleFactory»`](/uml-modeling-guide/jmm/ModuleFactory)

    