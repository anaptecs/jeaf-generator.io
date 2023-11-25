---
title: "JEAF Generator"
subtitle: "Features"
toc_title: " "
menubar: empty_menu
---

![Current Version](https://maven-badges.herokuapp.com/maven-central/com.anaptecs.jeaf.generator/jeaf-generator/badge.svg)

# Features

JEAF Generator is provided as Maven Plugin that is supposed to be integrated into your standard build process. All required configurations are done through the plugin configuration.

## Development Process

In general the development consists of the following steps:

| Steps                                                          | Further Documentation                                                           |
| -------------------------------------------------------------- |:------------------------------------------------------------------------------- |
| `Create / update classes etc. in UML model`        | - [UML Modeling Guide](../uml-modeling-guide)<br/>- [UML Modeling Guidelines]() |
| `Export UML model to XMI`                               |                                                                                 |
| `Run JEAF Generator as part of your Maven build`  |                                                                                 |
| `Implement parts that need to be done manually`   |                                                                                 |
| `Test and integrate your changes`                     |                                                                                 |

<br>

## Next Steps

For further information we recommend to at least read section about of JEAF Generator [general behavior](https://anaptecs.atlassian.net/wiki/spaces/JEAF/pages/546080018 "/wiki/spaces/JEAF/pages/546080018") and then either continue reading the documentation (see links above / on the left) or to [checkout the example project from our Git repository](https://bitbucket.org/anaptecs/jeaf-generator-samples "https://bitbucket.org/anaptecs/jeaf-generator-samples").