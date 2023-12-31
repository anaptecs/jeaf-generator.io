---
title: "UML Modeling Guide"
subtitle: "Stereotype «JEAFDeprecated»"
toc: false
menubar: jmm_menu
---

# Stereotype `«JEAFDeprecated»`
Deprecations are markers that indicate that a specific model element should not be used any longer. To do so, you just have to apply the stereotype `«JEAFDeprecated»` to the model element. This can be anything from a whole class or interface to an parameter of an operation.

<br>

| **Stereotype**          | `«JEAFDeprecated»` | |
| ----------------------- | -------------- | |
| **Applicable Elements** | `NamedElement`        |
| **Tagged Values**       |                       |                                                                                                                                                                                                          |
| **Name**                | **Type**              | **Description**                                                                                                                                                                                          |
| `description`   | `String` | Explanation which the element is deprecated and what should be done as an alternative. |
| `since`   | `String` | Information since when a model element is deprecated e.g. a concrete version or data. |
| `removedWith`   | `String` | Information when the deprecated element will no longer be available e.g. a version or date. |



<br>

<div style="text-align: right"><code>Generated by JEAF Generator</code></div>

    