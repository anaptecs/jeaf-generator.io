
---
title: "UML Modeling Guide"
subtitle: "Stereotype «JEAFComponent»"
toc: false
menubar: uml_modeling_guide_menu
---

# Stereotype `«JEAFComponent»`
Stereotype `«JEAFComponent»` is used to define JEAF Components in the UML model. JEAF Generator will use this stereotype as marker to identify for which model elements JEAF-specific classes for components should be generated.<br><br>Please be aware that all settings will applied for all services that are implemented by the component.

<br>

| **Stereotype**          | `«JEAFComponent»` | |
| ----------------------- | -------------- | |
| **Applicable Elements** | `Component`        |
| **Tagged Values**       |                       |                                                                                                                                                                                                          |
| **Name**                | **Type**              | **Description**                                                                                                                                                                                          |
| `transactionBehavior`   | `TransactionBehavior` | Attribute is used to define the transaction behavior of the component. Possible values are: `NOT_SUPPORTED`, `SUPPORTS`, `REQUIRED`, `REQUIRES_NEW`, `MANDATORY` and `NEVER`. <br>Default value is `REQUIRED`. |
| `layer`   | `Layer` |  |
| `useJEAFSecurity`   | `Boolean` | Attribute defines if JEAF Security should be used for this component. Default value is `true`.<br><br>For further details about JEAF Security please refer to [JEAF Security](https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546210729) |

<br>
For further information please refer to:<br><br>- [How to model Components](https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546177607 "https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546177607")<br><br>- [Generating Code for Components](https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546047011 "https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546047011")<br><br>- [JEAF Architecture Model - Component](https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/515276970/JEAF+Architecture+Model#Component "https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/515276970/JEAF+Architecture+Model#Component")<br><br>- [JEAF Security](https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546210729 "https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546210729")

    