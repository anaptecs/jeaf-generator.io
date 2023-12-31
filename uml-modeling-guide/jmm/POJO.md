---
title: "UML Modeling Guide"
subtitle: "Stereotype «POJO»"
toc: false
menubar: jmm_menu
---

# Stereotype `«POJO»`
Stereotype `«POJO»` can be used to model a POJO (Plain old Java object). It depends on your individual programming model what POJOs will be used for. 

<br>

| **Stereotype**          | `«POJO»` | |
| ----------------------- | -------------- | |
| **Applicable Elements** | `Class`        |
| **Tagged Values**       |                       |                                                                                                                                                                                                          |
| **Name**                | **Type**              | **Description**                                                                                                                                                                                          |
| `hasCustomImplementation`   | `Boolean` | Tagged value can be used to define if the class has some custom implementation. If set to `true` then a base class with all the information from the UML model will be generated and a an empty class for the custom implementation |
| `compositeDataType`   | `Boolean` |  |
| `compositeDataTypePublicFieldName`   | `String` |  |
| `compositeDataTypeReadonly`   | `Boolean` |  |
| `compositeDataTypeCustomSerialization`   | `Boolean` |  |
| `technicalBaseClass`   | `Boolean` |  |
| `readOnly`   | `Boolean` |  |
| `validateOnBuild`   | `Boolean` |  |
| `ofMethod`   | `OfMethodType` |  |
| `suppressSubtypesMapping`   | `Boolean` |  |

<br>

For further information please refer to:
- [How to model POJOs](/uml-modeling-guide/how-tos/how-to-model-pojos)
- [Generating Code for POJOs](/developer-guide/code-for-pojos)


<br>

<div style="text-align: right"><code>Generated by JEAF Generator</code></div>

    