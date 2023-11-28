---
title: "JEAF Generator"
subtitle: "Features"
description: JEAF Generator uses UML models to generate code for Spring, REST, Java, JakarataEE, JEE, Hibernate and others
toc_title: " "
menubar: empty_menu
---

# Features

JEAF Generator is designed for enterprise projects and offers a large set of features to implement scalable, high-load, high-performance applications. JEAF Generator realizes the link between UML and code.

<br>

JEAF Generator is provided as Maven Plugin. All required configurations can be done through the plugin configuration.

## Supported UML Modeling Tools

JEAF Generator uses UML models to generate code and configurations for various cases and target platform. No matter what is the expected output, an UML model is always the input.



## General Features

## Java

## Jackson / JSON
<i class="fa arrow-circle-up"></i>
<i class="fa fa-camera-retro"></i>
<i class="fa fa-check"></i>

## Spring

## OpenAPI

## Hibernate

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

<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-rest-api%2Fblob%2Fmaster%2Fjeaf-rest-request-executor-api%2Fsrc%2Fmain%2Fjava%2Fcom%2Fanaptecs%2Fjeaf%2Frest%2Fexecutor%2Fapi%2FRESTRequestExecutor.java&style=atom-one-dark&type=code&showBorder=on&showLineNumbers=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>