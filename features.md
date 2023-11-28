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
<i class="fa fa-camera-retro"></i>
<i class="fa circle-check"></i>
<i class="fa-circle-check" style="color: #00b900;"></i>
:thumbsup:
:white_check_mark:
:heavy_check_mark:

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

