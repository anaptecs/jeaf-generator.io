---
title: "UML Modeling Guide"
subtitle: "Stereotype «Identifiable»"
toc: false
menubar: uml_modeling_guide_menu
---

# Stereotype `«Identifiable»`

Stereotype `«Identifiable»` can be used to mark an object as Identifiable. This means that it can be identified using an `ObjectID`. The stereotype is intended to be used in combination with stereotypes `«DomainObject»`, `«POJO»` and `«ServiceObject»`. In case that such kinds of classes will be marked as identifiable then the generated code will respect that.<br>

As objects with stereotype `«PersistentObject»` are always identifiable usage of `«Identifiable»` does not make sense.

![Identifiable](/images/jmm_identifiable.png)

| **Stereotype**          | `Identifiable` |
| ----------------------- | -------------- |
| **Applicable Elements** | `Class`        |
| **Tagged Values**       | none           |

<br>

For further information please refer to:

- [How to model Service APIs](../../how-to-model-rest-services-apis)

- [How to model Domain Objects](../../how-to-model-domain-objects)

- [How to model POJOs](../../how-to-model-pojos)
