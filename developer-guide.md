---
title: "Developer Guide"
subtitle: "Introduction"
toc_title: " "
menubar: developer_guide_menu
---

![Current Version](https://maven-badges.herokuapp.com/maven-central/com.anaptecs.jeaf.generator/jeaf-generator/badge.svg)

# Developer Guide

JEAF Generator is provided as Maven Plugin that is supposed to be integrated into your standard build process. All required configurations are done through the plugin configuration.

## Development Process

In general the development consists of the following steps:

| Steps                                               | Additional Information                                                                    |
| --------------------------------------------------- |:----------------------------------------------------------------------------------------- |
| `1. Create / update classes etc. in UML model`      | - [UML Modeling Guide](../uml-modeling-guide)<br/>- [UML Modeling Guidelines]()           |
| `2. Export UML model to XMI`                        | - [MagicDraw XMI Export](magic-draw-xmi-export)                                           |
| `3. Run JEAF Generator as part of your Maven build` | - [Maven Integration](maven-integration)<br>- [Generating Code](overview-generating-code) |
| `4. Implement parts that need to be done manually`  |                                                                                           |
| `5. Test and integrate your changes`                |                                                                                           |

<br>

## Next Steps

For further information we recommend to have a look at the following sections:

- [JEAF Generator General Behavior](general-behavior) 
- [Checkout the example project from our Git repository](https://bitbucket.org/anaptecs/jeaf-generator-samples).