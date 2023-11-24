---
title: "JEAF Generator"
subtitle: "Join Next Generation Software Development"
layout: page
menubar_toc: false
show_sidebar: true
hero_image: ./images/jeaf_emotions.png
hero_height: is-fullwidth
callouts: jeaf_generator_callouts
---

# JEAF Generator

JEAF Generator can be used for code generation based on UML models. It supports a wide variety of artifacts that can be generated like:

* `Service Interfaces`
* `REST Resources / Controller / Clients`
* `POJO's`
* `OpenAPI specs`
* `Persistent Classes (JPA / Hibernate)`
* `and many more ...`

<br>

As JEAF Generator is designed to be used in all kinds of enterprise projects as it offers a large set of features that are required to provide scalable, high performance enterprise applications.

<br>

JEAF Generator is provided as Maven Plugin. Using Maven it can be integrated into your projects very easily. Main input for JEAF Generator is an XMI Export of your UML model. In addition you have to define inside your Maven build which parts of the model should be taken into account during the generation process and what should be generated.

<br>

Initially JEAF Generator was closely connected with anaptecs JEAF Framework. Meanwhile JEAF Generator is an independent generic Open Source solution that supports the following environments:

* **Enterprise Target Platforms**
  * `JEAF Framework`
  * `Spring / Spring Boot`
  * `JEE`

<br>  

* **UML Modeling Tools**
  * `MagicDraw UML`
  * `Eclipse Papyrus`

<br>

# Development Process

When working with JEAF Generator then development process in general
will look as follows:

| #   | Activity                                       | Additional Documentation |
| --- | ---------------------------------------------- | ------------------------ |
| 1.  | Create / update classes etc. in UML model      |                          |
| 2.  | Export UML model to XMI                        |                          |
| 3.  | Run JEAF Generator as part of your Maven Build |                          |
| 4.  | Implement parts that need to be done manually  |                          |
| 5.  | Test and integrate your changes                |                          |
