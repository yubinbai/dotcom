---
title: 'UML distilled - Martin Folwer'
date: 2012-12-19 20:15:35
tags: book-review
---

{% img /images/uml-distilled.jpg %}

Martin Folwer Publication Date: September 25, 2003 | ISBN-10: 0321193687 | ISBN-13: 978-0321193681 | Edition: 3

> Timeless: Reduce everything to its essence so that form harmonizes with function.

Overall
===
Graphical design notations have been with us for a while. For me, their primary value is in communication and understanding. A good diagram can often help communicate ideas about a design, particularly when you want to avoid a lot of details. Diagrams can also help you understand either a software system or a business process

Many people believe that in the future, graphical techniques will play a dominant role in software development.

The Unified Modeling Language (UML) is a family of graphical notations, backed by single meta-model, that help in describing and designing software systems, particularly software systems built using the object-oriented (OO) style.

The fundamental driver behind them all is that programming languages are not at a high enough level of abstraction to facilitate discussions about design.

The essence of sketching is selectivity.
===
(UML as blueprint is about completeness) In forward engineering, the idea is that blueprints are developed by a designer whose job is to build a detailed design for a programmer to code up. However, the creators of the UML see the diagrams as secondary; the essence of the UML is the meta-model. Diagrams are simply a presentation of the meta-model.

The UML, in its current state, defines a notation and a meta-model. The notation is the graphical stuff you see in models; it is the graphical syntax of the modeling language.

A language with prescriptive rules is controlled by an official body that states what is or isn't legal in the language and what meaning you give to utterances in that language. A language with descriptive rules is one in which you understand its rules by looking at how people use the language in practice.

My attitude is that, for most people, the UML has descriptive rules.

The waterfall style breaks down a project based on activity. To build software, you have to do certain activities: requirements analysis, design, coding, and testing.

The iterative style breaks down a project by subsets of functionality. You might take a year and break it into 3-month iterations.

You may well not put the system into production at the end of each iteration, but the system should be of production quality.

Most writers on software process in the past few years, especially in the object-oriented community, dislike the waterfall approach. Of the many reasons for this, the most fundamental is that it's very difficult to tell whether the project is truly on track with a waterfall process.

A common technique with iterations is to use time boxing. This forces an iteration to be a fixed length of time. A good rule of thumb is that the size of your unit test code should be about the same size as your production code.

Agile is an umbrella term that covers many processes that share a common set of values and principles as defined by the Manifesto of Agile Software Development (http://agileManifesto.org)

In terms of our discussion, agile processes are strongly adaptive in their nature. They are also very much people-oriented processes.

Agile processes tend to be low in ceremony. A high-ceremony, or heavyweight, process has a lot of documents and control points during the project.

Whether or not you use a waterfall approach, you still do the activities of analysis, design, coding, and testing.

Use cases describe how people interact with the system.

An activity diagram, which can show the work flow of the organization, showing how software and human activities interact.

• Class diagrams from a software perspective. These show the classes in the software and how they interrelate.
• Sequence diagrams for common scenarios. A valuable approach is to pick the most important and interesting scenarios from the use cases and use CRC cards or sequence diagrams to figure out what happens in the software.
• Package diagrams to show the large-scale organization of the software.
• State diagrams for classes with complex life histories.
• Deployment diagrams to show the physical layout of the software.

One of my concerns with blueprints is my own observation that it's very hard to get them right, even for a good designer.

I believe that detailed documentation should be generated from the code—like, for instance, JavaDoc. You should write additional documentation to highlight important concepts.

The class diagram should be supported by a handful of interaction diagrams that show the most important interactions in the system.

A class diagram describes the types of objects in the system and the various kinds of static relationships that exist among them.

The multiplicity of a property is an indication of how many objects may fill the property.

An important principle of using inheritance effectively is substitutability. I should be able to substitute a Corporate Customer within any code that requires a Customer, and everything should work fine.

Interaction diagrams describe how groups of objects collaborate in some behavior.

Despite this, object bigots like me strongly prefer distributed control. One of the main goals of good design is to localize the effects of change. Data and behavior that accesses that data often change together. So putting the data and the behavior that uses it together in one place is the first rule of object-oriented design.

If a caller sends a synchronous message, it must wait until the message is done, such as invoking a subroutine. If a caller sends an asynchronous message, it can continue processing and doesn't have to wait for a response.

If you find that you need a modeling construct that isn't in the UML but is similar to something that is, use the symbol of the existing UML construct but mark it with a keyword to show that you have something different.

A UML interface is a class that has only public operations, with no method bodies

Classification refers to the relationship between an object and its type.

The UML uses the generalization symbol to show generalization. If you need to show classification, use a dependency with the «instantiate» keyword.

Generalization sets are by default disjoint: Any instance of the supertype may be an instance of only one of the subtypes within that set.

Association classes allow you to add attributes, operations, and other features to associations.

Aggregation is the part-of relationship. It's like saying that a car has an engine and wheels as its parts.

The general rule is that, although a class may be a component of many other classes, any instance must be a component of only one owner. The "no sharing" rule is the key to composition.

An abstract class is a class that cannot be directly instantiated.

A qualified association is the UML equivalent of a programming concept variously known as associative arrays, maps, hashes, and dictionaries.

An object diagram is a snapshot of the objects in a system at a point in time.

A package is a grouping construct that allows you to take any construct in the UML and group its elements together into higher-level units.

Artifacts, which are the physical manifestations of software: usually, files.

Use cases are a technique for capturing the functional requirements of a system. Use cases work by describing the typical interactions between the users of a system and the system itself, providing a narrative of how a system is used.

A scenario is a sequence of steps describing an interaction between a user and a system.

A use case is a set of scenarios tied together by a common user goal.

As well as the steps in the scenarios, you can add some other common information to a use case.
• A pre-condition describes what the system should ensure is true before the system allows the use case to begin. This is useful for telling the programmers what conditions they don't have to check for in their code.
• A guarantee describes what the system will ensure at the end of the use case. Success guarantees hold after a successful scenario; minimal guarantees hold after any scenario.
• A trigger specifies the event that gets the use case started.

State machine diagrams are a familiar technique to describe the behavior of a system

The transition indicates a movement from one state to another.

Activity state: The ongoing activity is marked with the do/; hence the term do-activity.

The activity diagram allows whoever is doing the process to choose the order in which to do things.

UML 2 uses the terms flow and edge synonymously to describe the connections between two actions.

Interaction overview diagrams are a grafting together of activity diagrams and sequence diagrams.
