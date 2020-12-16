---
title: "Exposing Collection Properties"
date: "2015-06-22"
description: Generally, exposing collection properties from domain Entities is an antipattern, because it leads to an anemic domain model and breaks encapsulation.
---

Generally, exposing collection properties from domain Entities is an [antipattern](/tag/antipattern/), because it leads to an [anemic domain model](/anemic-model/) and breaks [encapsulation](/encapsulation/). Entities should be responsible for managing their own internal state, and this includes the contents of their related collections. This is especially important for aggregate roots, which must ensure consistency of the entire aggregate prior to allowing persistence of the model to occur. Some tools, including some object-relational mapping tools, have difficulty supporting private collection properties. This can impact the goal of having [persistence ignorance (PI)](http://persistence-ignorance/) in the domain model, but wherever possible one should try to achieve both PI and proper encapsulation of the model.

## See Also

[Properly Exposing Collection Properties](http://blog.falafel.com/properly-exposing-collection-properties/)

[Exposing Private Collection Properties to Entity Framework](http://ardalis.com/exposing-private-collection-properties-to-entity-framework)