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

# Hello

| Hello | World |     |
| ----- | ----- | --- |
| `Code`      | Text  |     |
|       |       |     |
|       |       |     |


## Maven Build Helper Plugin

When working with JEAF Generator the standard Maven directory layout is not sufficient any longer as we have to distinguish between hand-written and generated code ([Directory Layout for generated output](../general-behavior)). This also requires that the additional locations of source code and resources are know to the build process in general. To do so we make use of [Maven Build Helper Plugin](https://www.mojohaus.org/build-helper-maven-plugin).

<br>

This means that in addition to the JEAF Generator Plugin also Maven Build Helper has to be added to your build. Depending on the structure of you Maven projects it might also be an option to add configuration Build Helper Plugin to your parent POM.

<div>
	<script src="https://emgithub.com/embed-v2.js?target=https%3A%2F%2Fgithub.com%2Fanaptecs%2Fjeaf-generator-samples%2Fblob%2Fmaster%2Fpom.xml%3Fts%3D4%23L118-L194&style=base16%2Fatelier-forest-light&type=code&showBorder=on&showFileMeta=on&showFullPath=on&showCopy=on"></script>
</div>

<br>
