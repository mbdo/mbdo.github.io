---
layout: home
title: The Project
#description: (MBDO)
background: /assets/theme/images/uni_rennes-1.jpg
permalink: /
---

## Motivation

Time to market and continuous improvement are becoming key success indicators to deliver the cloud-native and Internet of Things (IoT) systems, which includes the IoT part of Cyber-Physical Systems (CPSs) as well. These systems are essential to the European Commission's Vision on Industry 5.0 , which is a sustainable, human-centric, and resilient Industry 4.0. In that context, the increasingly popular DevOps approach aims at combining software development ("Dev") and IT operations ("Ops") into a highly-integrated continuous loop. Through both agility and automation of complex pipelines across the various stakeholders of the entire lifecycle, DevOps aims to shorten the systems development time and provide continuous delivery with high software quality. Through this continuous delivery, the quality, sustainability, and resiliency of IoT systems can be continuously improved. 

## Models in DevOps

Automation in DevOps is enabled by leveraging multiple models, typically expressed in either explicit Domain-Specific Languages (DSLs) or, most often, implicitly using concrete syntaxes such as JSON, XML, or even just ad hoc annotations in a general-purpose programming language, such as Java. These models are used among others for (M1) code generation during design time [CFJ+16], and (M2) for configuration of the overall IoT system at runtime [BBF09, MBJ+09]. These uses of models yield individual advantages: Design time models and automated code generation lead to better efficiency of the developers, better quality of the results, and usually also to an improvement of agility, because refactoring becomes easier. Using models at runtime has the advantage that IT operations or even the end-user may reconfigure and adapt the models and thus the software part of a system, while it is already in operation. These models at runtime can thus be seen as primitive digital twins [BR16, KMR+20] of the represented IoT systems.

Models can and should be updated in four stages of the lifecycle of a system: (U1) automatically immediately (immediately self-adaptive, based on data and events) during the system’s operation (M2), (U1b) automatically, but with some delay (based on data collections, needs recalculation or training and especially quality assurance, e.g., overnight, therefore is slowly self-adaptive; needs M2), (U2) by human operators (needs M2), (U3) by human designers only (M1).		
Self-adaptive (U1, U1b), human-adaptable (U2) and design models (U3) are rather disjoint in their usage, but do share a larger overlap in the targets they describe: Design models describe requirements, structure, functional and extra functional concerns, while runtime models focus on component configurations, deployment and on measures in operations. Self-adaptive models (U1, U1b) are closely linked with the collection of data that through appropriate techniques of data science and AI enable the system to reflect on its own behaviour and identify possible optimizations, additional detailed knowledge about usage, etc. Self-adaptive models (U1, U1b) and also human-adaptable models (U2) will be present for adaptation in a digital twin of the system, while the structurally fixed design models (U3) also define the structure of a digital twin. Unfortunately, the models today are strictly separated, and can either be used during design or during runtime. This hinders optimizing represented systems, learning from its operation, and improving future iterations of it. There currently is no way to migrate a model from design to runtime or vice versa. Hence, improvements made during system runtime are lost or must be migrated to the design models manually, which is costly, error-prone, and, thus, rarely done. Even more challenging, we are not able to early model the requirements of the system and only late during development identify a part of a model that goes into a fixed, high-quality design (U3), a second part that is dedicated for adaptation by human operators (U2), and a third part that is self-adaptive (U1). Furthermore, it may be necessary to transfer parts of the underlying model infrastructure between these dimensions (U1) - (U3) on demand and potentially do this even during operation. The interplay of these three dimensions needs a solid and precise semantics and methodical investigation, to effectively accommodate Model-Based DevOps (MBDO) in the context of complex IoT systems, where adaptive services are provided by model-based digital twins. 

## Observations

- DevOps is a well-established practice for software intensive systems, and is increasingly considered for IoT. In that context, models play key roles for either or both code/test generation and configuration/deployment of these kinds of systems.
- Adaptive Systems are typically built with a MAPE-K loop [KC03, HM08] featuring an implicit or explicit model of their runtime configuration (reflective layer), which can be seen as a primitive digital twin.
- Full blown digital twins are already widely used in several domains (aerospace industry, automotive, building construction, etc.) but not that often for software intensive systems or IoT systems.
- A digital twin is a model (i.e., an abstraction of some aspect of reality in a given purpose), but its (conceptual) nature and its (technical) form are widely different from the typical software and systems engineering models considered at design time.

## Goals

Our goal in MBDO is to provide the foundations for a Model-Based DevOps framework unifying these different forms of models in the specific context of cloud-native and IoT systems. The proposed Model-Based DevOps framework would then allow engineers to smoothly go back and forth from Dev time to Ops time by leveraging semi-automatically generated digital twins of their systems.


