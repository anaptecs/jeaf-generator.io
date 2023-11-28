---
title: "Developer Guide"
subtitle: "General Behavior"
toc_title: " "
menubar: developer_guide_menu
---

![Current Version](https://maven-badges.herokuapp.com/maven-central/com.anaptecs.jeaf.generator/jeaf-generator/badge.svg)

# General Behavior

## Directory Layout for Generated Output

In order to ensure a strict separation between generated and hand-written code and resources JEAF Generator is working with the following directories / output slots:

- `src-gen`<br>
  This slot contains all generated Java classes. Every time JEAF Generator is executed all files in this directory will be at first deleted and then written again. Files in this directory must not be edited manually.  <br><br>

- `src`  <br>This slot contains all the classes that are intended to be edited manually. In case that a class does not exist in this directory then it will be written also into this directory. But JEAF Generator will never overwrite or edit any existing classes here.
  
  This is the slot where classes that contain any kind of business logic will be located. Usually this slot will point to your standard source code location.  <br><br>

- `res-gen`  <br>This slot contains all the generated resource files. All file in the directory and all of its sub directories will be overwritten every time when JEAF Generator will be executed. Files in this directory must not be edited manually.  <br><br>

- `res`  <br>This slot contains all the resources that are intended to be edited manually. In case that a resource does not exist in this directory then it will be written also into this directory. But JEAF Generator will never overwrite or edit any existing files here.  
  
  Usually this slot will point to your standard resource location.  <br><br>

Of course it’s possible to configure a concrete directory for each of these output slots according to your project settings.

<br>

# Error Handling

JEAF Generator is supposed to work as fault tolerant as possible. When ever possible we try to avoid that the whole code generation process is aborted. In general JEAF Generator distinguishes between errors and warnings.

Both of them will be listed at the end of the generator output as a summary. So to get an overview it’s not required to check the complete log. When JEAF Generator detects a warning for a specific model element it tries to point out the exact element that caused the problem as well as an description of the identified issue. The same is done for errors. However in case of a warning code generation for the model element is still possible whereas this is not the case when an error is found. In this case the model element will be ignored and JEAF Generator will try to process the next element of the UML model.

You can find the complete list of all error messages / warnings on site [JEAF Generator Error Codes](../error-codes).
