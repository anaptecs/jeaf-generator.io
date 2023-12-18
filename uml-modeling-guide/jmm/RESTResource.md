---
title: "UML Modeling Guide"
subtitle: "Stereotype «RESTResource»"
toc: false
menubar: jmm_menu
---

# Stereotype `«RESTResource»`
Stereotype `«RESTResource»` can be used to mark a service to also expose his operations at least partially also as REST Resource. 

Please be aware that the stereotype only makes sense to be used on interfaces that are marked as service using stereotype `«JEAFService»`.

<br>

| **Stereotype**          | `«RESTResource»` | |
| ----------------------- | -------------- | |
| **Applicable Elements** | `Interface`        |
| **Tagged Values**       |                       |                                                                                                                                                                                                          |
| **Name**                | **Type**              | **Description**                                                                                                                                                                                          |
| `path`   | `String` | Path under which the REST resource should be available. The attribute is optional. However as from a REST perspective it’s a best practice to define it. So it’s strongly recommended to do so already in the UML model. |
| `produces`   | `MediaType` | Optional definition of the media types that are used to encode the responses of the REST calls (e.g. `JSON`, `XML` etc.). |
| `consumes`   | `MediaType` | Optional definition of the media types that are supported to be used to encode REST requests (e.g. `JSON`, `XML` etc.). |
| `async`   | `Boolean` | Tagged value defines if the generated REST Resource / Controller should make use of server-side async processing.<br><br>Please be aware that async processing is not supported by all target platforms. |

<br>

For further information please refer to:
- [How to model REST Services](/uml-modeling-guide/how-to-model-rest-service-apis)
- [Generating Code for REST Services](/developer-guide/code-for-jeaf-services)


<br>

<div style="text-align: right"><code>Generated by JEAF Generator</code></div>

    