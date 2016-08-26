---
layout: post
title: "Differences between dependencymanagement and dependencies in maven"
description: ""
category: quick-fix
tags: [maven]
---
Dependency Management allows to consolidate and centralize the management of dependency versions without adding dependencies which are inherited by all children. This is especially useful when you have a set of projects (i.e. more than one) that inherits a common parent.

Another extremely important use case of dependencyManagement is the control of versions of artifacts used in transitive dependencies. This is hard to explain without an example. Luckily, this is illustrated in the documentation.

If the dependency was defined in the top-level pom's dependencyManagement element, the child project did not have to explicitly list the version of the dependency. if the child project did define a version, it would override the version listed in the top-level POM’s dependencyManagement section. That is, the dependencyManagement version is only used when the child does not declare a version directly.

[来源stackoverflow]  
[http://stackoverflow.com/questions/2619598/differences-between-dependencymanagement-and-dependencies-in-maven
](http://stackoverflow.com/questions/2619598/differences-between-dependencymanagement-and-dependencies-in-maven)  
[http://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Dependency_Management
](http://maven.apache.org/guides/introduction/introduction-to-dependency-mechanism.html#Dependency_Management)  
