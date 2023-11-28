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
  This slot contains all generated Java classes. Every time JEAF Generator is executed all files in this directory will be at first deleted and then written again. Files in this directory must not be edited manually.  <br>

- `src`  <br>This slot contains all the classes that are intended to be edited manually. In case that a class does not exist in this directory then it will be written also into this directory. But JEAF Generator will never overwrite or edit any existing classes here.
  
  This is the slot where classes that contain any kind of business logic will be located. Usually this slot will point to your standard source code location.  <br>

- `res-gen`  <br>This slot contains all the generated resource files. All file in the directory and all of its sub directories will be overwritten every time when JEAF Generator will be executed. Files in this directory must not be edited manually.  <br>

- `res`  <br>This slot contains all the resources that are intended to be edited manually. In case that a resource does not exist in this directory then it will be written also into this directory. But JEAF Generator will never overwrite or edit any existing files here.  
  
  Usually this slot will point to your standard resource location.  <br>

Of course it’s possible to configure a concrete directory for each of these output slots according to your project settings.
