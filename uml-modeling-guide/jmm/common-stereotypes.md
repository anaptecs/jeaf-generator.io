---
title: "UML Modeling Guide"
subtitle: "Common Stereotypes"
toc: false
menubar: uml_modeling_guide_menu
---

# Common Stereotypes

JEAF Generator provides a wide range of features in the area of code generation from UML models. On the pages of this section you will find information about very common stereotypes:<br>

- «JEAFDeprecated»
- «Transient»
- «Internal»

<br>

## «JEAFDeprecated»

Deprecations are markers that indicate that a specific model element should not be used any longer. To do so, you just have to apply the stereotype `«JEAFDeprecated»` to the model element. This can be anything from a whole class or interface to an parameter of an operation.

|                         |                                                                                    |                 |
| ----------------------- | ---------------------------------------------------------------------------------- | --------------- |
| **Stereotype**          | `«JEAFDeprecated»` (`«deprecated»` Stereotype from MagicDraw UML is not supported) |                 |
| **Applicable Elements** | `NamedElement` (all model elements)                                                |                 |
| **Tagged Values**       |                                                                                    |                 |
| **Name**                | **Type**                                                                           | **Description** |
| none                    |                                                                                    |                 |

<br>

## «Transient»

Stereotype can be used to mark attributes or roles inside the UML model as transient. Attributes / association end with this stereotype will be marked with keyword `transient` also in the generated code. This is especially helpful in scenarios where objects will be serialized e.g. using JSON.

|                         |               |                 |
| ----------------------- | ------------- | --------------- |
| **Stereotype**          | `«Transient»` |                 |
| **Applicable Elements** | `Property`    |                 |
| **Tagged Values**       |               |                 |
| **Name**                | **Type**      | **Description** |
| none                    |               |                 |

 <br>

## «Internal»

Stereotype can be used to mark attributes or roles as `internal`. This means that in the generated Java code they will be generated as any other properties but access methods will only have package visibility.

|                         |              |                 |
| ----------------------- | ------------ | --------------- |
| **Stereotype**          | `«Internal»` |                 |
| **Applicable Elements** | `Property`   |                 |
| **Tagged Values**       |              |                 |
| **Name**                | **Type**     | **Description** |
| none                    |              |                 |
