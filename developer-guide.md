---
toc_title: " "
---

# Developer Guide

JEAF Generator is provided as Maven Plugin that is supposed to be integrated into your standard build process. All required configurations are done through the plugin configuration.

In general the development consists of the following steps:

| #   | Activity                                       | Details                                                                    |
| --- | ---------------------------------------------- | -------------------------------------------------------------------------- |
| 1.  | Create / update classes etc. in UML model      | - [UML Modeling Guide](./uml-modeling-guide)<br/>- [Modeling Guidelines]() |
| 2.  | Export UML model to XMI                        |                                                                            |
| 3.  | Run JEAF Generator as part of your Maven Build |                                                                            |
| 4.  | Implement parts that need to be done manually  |                                                                            |
| 5.  | Test and integrate your changes                |                                                                            |