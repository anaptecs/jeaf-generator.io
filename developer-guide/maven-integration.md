---
title: "Developer Guide"
subtitle: "Integrate JEAF Generator into Maven Build"
toc_title: " "
toc: false
menubar: developer_guide_menu
---

# Integrate JEAF Generator into Maven Build

JEAF Generator is provided as Maven Plugin and thus can be easily integrated into your build process. This side will describe how to do that.

<br>

## Maven Build Helper Plugin

When working with JEAF Generator the standard Maven directory layout is not sufficient any longer as we have to distinguish between hand-written and generated code ([Directory Layout for generated output](../general-behavior)). This also requires that the additional locations of source code and resources are know to the build process in general. To do so we make use of [Maven Build Helper Plugin]([Build Helper Maven Plugin &#x2013; Introduction](https://www.mojohaus.org/build-helper-maven-plugin).

 <br>

This means that in addition to the JEAF Generator Plugin also Maven Build Helper has to be added to your build. Current recommend version of Maven Build Helper Plugin is

```xml
<!-- 
  Build helper plugin adds directories with generated sources / resources to build:
  - src-gen/main/java
  - src-gen/test/java
  - src-gen/main/resources
  - src-gen/test/resources
		 
  In addition to directories with generated code also default directories have to be set 
  here when directory layout is customized.
-->
<plugin>
  <groupId>org.codehaus.mojo</groupId>
  <artifactId>build-helper-maven-plugin</artifactId>
  <version>${maven.build.helper.version}</version>
  <executions>
    <execution>
      <id>sources</id>
      <phase>generate-sources</phase>
      <goals>
        <goal>add-source</goal>
      </goals>
      <configuration>
        <sources>
          <source>${basedir}/src/main/java</source>
          <source>${basedir}/src-gen/main/java</source>
        </sources>
      </configuration>
    </execution>
    <execution>
      <id>test-sources</id>
      <phase>generate-test-sources</phase>
      <goals>
        <goal>add-test-source</goal>
      </goals>
      <configuration>
        <sources>
          <source>${basedir}/src/test/java</source>
          <source>${basedir}/src-gen/test/java</source>
        </sources>
      </configuration>
    </execution>
    <execution>
      <id>resources</id>
      <phase>generate-resources</phase>
      <goals>
        <goal>add-resource</goal>
      </goals>
      <configuration>
        <resources>
          <resource>
            <directory>${basedir}/src/main/resources</directory>
          </resource>
          <resource>
            <directory>${basedir}/src-gen/main/resources</directory>
          </resource>
        </resources>
      </configuration>
    </execution>
    <execution>
      <id>test-resources</id>
      <phase>generate-test-resources</phase>
      <goals>
        <goal>add-test-resource</goal>
      </goals>
      <configuration>
        <resources>
          <resource>
            <directory>${basedir}/src/test/resources</directory>
          </resource>
          <resource>
            <directory>${basedir}/src-gen/test/resources</directory>
          </resource>
        </resources>
      </configuration>
    </execution>
  </executions>
</plugin>
```