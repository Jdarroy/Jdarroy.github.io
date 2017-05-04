---
layout: post
title:  "Get Started With January on The Command Line"
date:   2017-05-03 14:13:35 +0100
categories: jekyll update
permalink: /get-started-with-january/
---
# Get Started With January on The Command Line

## Requirements

* Knowing how to use **vi** or any other command line editor
* Havin **maven** installed
  * On Windows: https://www.mkyong.com/maven/how-to-install-maven-in-windows/
  * On Linux: `apt install maven`

## How-to

1. Go into the directory you want to create your project in and execute
   following command:
   ```maven
   mvn archetype:generate \
   -DgroupId=com.test \
   -DartifactId=mvnExample \
   -DarchetypeArtifactId=maven-archetype-quickstart \
   -DinteractiveMode=false
   ```
This may take some time if it is the first time you use Maven. After the
execution of the command you can move into the newly created folder and see the
folders and files of the project.

2. Now you have to add the January dependency to you project, in order to do
   that edit the pom.xml file with vi or whatever you prefer. You have to add
following code between the two 'dependencies' tags:
   ```xml
   <dependency>
	   <groupId>com.github.yannick-mayeur</groupId>
	   <artifactId>org.eclipse.january</artifactId>
	   <version>2.0.2</version>
   </dependency>
   ```
3. You can now add some code that uses the January library into the `App.java`
   file at `src/main/java/com/test`. Here is some example code:
   ```java
   Dataset dataset = DatasetFactory.createFromObject(new double[] { 1,2, 3, 4, 5, 6, 7, 8, 9 });
   // Print the output:
   System.out.println("shape of dataset: " + Arrays.toString(dataset.getShape()));
   System.out.println("toString of dataset: " + dataset.toString());
   System.out.println("toString, with data, of dataset: \n" + dataset.toString(true));
   ```

   Don't forget to import the relevant libraries:
   ```java
   import java.util.Arrays;
   import org.eclipse.january.dataset.Dataset;
   import org.eclipse.january.dataset.DatasetFactory;
   ```

4. You can then compile the project with `mvn clean package` and execute it
   with<br>`mvn exec:java -Dexec.mainClass="com.test.App"`
