---
title: "UML Modeling Guide"
subtitle: "Stereotype «LoadStrategy»"
toc: false
menubar: uml_modeling_guide_menu
---

# Stereotype `«LoadStrategy»`
Stereotype `«Load Strategy»` is used to model so called load strategy objects. They can be used to tell a service which information should be returned from a service. Usage of load strategy pattern usually only makes sense when a rather big mesh of objects can be returned by a service. In such cases clients might not need all the information that will be returned. Using load strategy pattern clients can define the information they are expecting. 

To define which information are really needed a load strategy object defines a set of boolean fields representing parts of the service object model that might be returned by the service.

<br>

| **Stereotype**          | `«LoadStrategy»` | |
| ----------------------- | -------------- | |
| **Applicable Elements** | `Class`        |
| **Tagged Values**       |                       |                                                                                                                                                                                                          |
| **Name**                | **Type**              | **Description**                                                                                                                                                                                          |

<br>

For further information please refer to:
- [How to model Load Strategy Objects](/uml-modeling-guide/how-to-model-rest-service-apis)
- [Generating Code for Load Strategy Objects](/developer-guide/code-for-jeaf-services/#code-for-load-strategy-objects)

    