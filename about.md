---
layout: page
title: About
permalink: /about/
---

## PEOPLE

#### Project Leads:

Jonah Graham
Peter Chang
Committers:
Jonah Graham
Peter Chang
Tracy Miranda
Alex McCaskey
Jay Jay Billings
Matthew Gerring
Mentors:
Jay Billings
----

#### Interested Parties:

This project is of interest to members of the Science Working Group and the following projects:

EAVP
Triquetrum
ICE
DAWNSci
UOMo

----
## SOURCE CODE

#### Initial Contribution:

The initial contribuiton is expected to made in the first half of 2016.

The initial contribution consists of two parts:

----
#### Part 1:

The numeric datastructures are a fork of the Eclipse Dawnsci project that extracts Datasets and its associated mathematical libraries. As per the DAWNSci project proposal:

"The copyright of the initial contribution is held ~100% by Diamond Light Source Ltd. There may be some sections where copyright is held jointly between the European Synchrotron Radiation Facility and Diamond Light Source Ltd. No individual people or other companies own copyright of the initial contribution. Expected future contributions like the implementation of various interfaces will have to be dealt with as they arrive. Currently none are planned where the copyright is not European Synchrotron Radiation Facility and/or Diamond Light Source Ltd."

This part of the  initial contribution is made up of three plug-ins:

org.eclipse.dataset - main code of the project, include the numerical n-dimensional arrays and the mathematics that operates on them.
org.eclipse.dataset.test - test code for the project
org.eclipse.dataset.examples - example code and getting started with datasets
All of the dependencies of the initial contribution are libraries that are already part of Eclipse ecosystem in Orbit:

org.apache.commons.math3
org.apache.commons.lang
org.slf4j.api
org.junit
The initial contribution is currently actively developed by Diamond Light Source and collaborated on by Diamond Light Source, Kichwa Coders, and European Synchrotron Radiation Facility, among others. In the URLs below the https://github.com/jonahkichwacoders repositories are a fork of the eclipse/dawnsci repository. The fork was created to allow easy refactoring and demonstrate code structure.

----
#### Part 2:

The non-numeric datastructures are a fork of the Eclipse ICE project.

This part of the  initial contribution is made up of these plug-ins:

org.eclipse.ice.datastructures- main code of the project, includes the various components such as ResourceComponent, DataComponent
org.eclipse.ice.datastructures.test - test code for the project
All of the dependencies of the initial contribution are libraries that are already part of Eclipse ecosystem in Orbit:

ca.odell.glazedlists
org.slf4j.api
org.junit
The initial contribution is currently actively developed by Oakridge National Labs.

Source Repository Type:
GitHub
Source Repositories:
https://github.com/jonahkichwacoders/org.eclipse.dataset
https://github.com/jonahkichwacoders/org.eclipse.dataset.examples
https://github.com/eclipse/ice/tree/master/org.eclipse.ice.datastructures
https://github.com/eclipse/dawnsci/tree/master/org.eclipse.dawnsci.analysis.data...
