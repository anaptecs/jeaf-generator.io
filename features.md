---
title: "JEAF Generator"
subtitle: "Features"
description: JEAF Generator uses UML models to generate code for Spring, REST, Java, JakarataEE, JEE, Hibernate and others
toc_title: " "
menubar: empty_menu
---

# Features

JEAF Generator realizes the link between UML models and code.It is designed for enterprise projects and offers a large set of features to implement scalable, high-load, high-performance applications. 

<br>

JEAF Generator is provided as Maven Plugin. All required configurations can be done through the plugin configuration.

<br>

## Supported UML Modeling Tools

JEAF Generator uses UML models to generate code and configurations for various cases and target platforms. No matter what is the expected output, an UML model is always the input.

Currently the following UML modeling tools are supported <sup>1)</sup>:

* [**MagicDraw UML** (commercial)](https://www.3ds.com/products-services/catia/products/no-magic/magicdraw/)
* [**Eclipse Papyrus** (Open Source)](https://projects.eclipse.org/projects/modeling.mdt.papyrus)

<br>

*<sup>1)</sup>* Enterprise Architect from Sparx Systems is not supported as it does not support the full UML 2.5 feature set. Unfortunately, some of the missing features are mandatory when you want to set up a feature rich, high quality model-driven process.*

<br>

## General Features

* Maven Configuration
* Maven
* Generated code can be extended with manual code

| Features                     | Details                                                                                                                    |
| ---------------------------- | -------------------------------------------------------------------------------------------------------------------------- |
| **General Features**         |                                                                                                                            |
| Maven Integration            | JEAF Generator is provided a Maven Plugin to easily integrate into your build process                                      |
| Maven Configuration          | All configurations are done via Maven Plugin configuration                                                                 |
|                              |                                                                                                                            |
| Customer-specific extension. | In addition to the already integrated templates for code generation it is also possible to add custom templates and checks |
|                              |                                                                                                                            |
|                              |                                                                                                                            |
|                              |                                                                                                                            |
|                              |                                                                                                                            |
|                              |                                                                                                                            |
|                              |                                                                                                                            |
|                              |                                                                                                                            |

## Java <i class="fa-brands fa-java fa-xl" style="color: #5F996B;"></i>

## Jackson / JSON

<i class="fas fa-check-circle fa-lg" style="color: #B92132;"></i>

## Spring

## OpenAPI

## Hibernate

## JakartaEE / JEE

## Reports

```java
public enum ContentType {
  JSON("application/json"), XML("application/xml");

  /**
   * Mime type that belongs to the content type-
   */
  private final String mimeType;

  /**
   * Initialize enumeration.
   * 
   * @param pMimeType Mime type the belong to the content type. The parameter must not be null.
   */
  private ContentType( String pMimeType ) {
    mimeType = pMimeType;
  }

  /**
   * Method returns the mime type that belongs to this content type.
   * 
   * @return String Mime type. The method never returns null.
   */
  public String getMimeType( ) {
    return mimeType;
  }
}
```

<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-rest-api%2Fblob%2Fmaster%2Fjeaf-rest-request-executor-api%2Fsrc%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Frest%2Fexecutor%2Fapi%2FRESTRequestExecutor.java&style=github&type=code&showLineNumbers=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>