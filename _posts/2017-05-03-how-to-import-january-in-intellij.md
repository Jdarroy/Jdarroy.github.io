---
layout: post
title:  "Import January in ItelliJ"
date:   2017-05-03 14:13:35 +0100
categories: jekyll update
permalink: /import-january/
---
# How to import January in IntelliJ

In this tutorial, we will see how to import January in IntelliJ.

## Download IntelliJ (if you don't have it) :

There is two versions of IntelliJ, the first one is free, this is the community version, open source, and you have to pay for the second one.
Here you can download the last version :
[IntelliJ download page](https://www.jetbrains.com/idea/download/#section=windows)

Note : During this tutorial I'm using the complete edition of IntelliJ, so if some links are differents in your IntelliJ it could be because of that.

## Creating a new project :

  1. Now, you need to create a new project, to do that, open IntelliJ, a frame like that will be shown :

![Home Page](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_1.png?raw=true)

 2. Click on "Create New Project". This page will appear, just click on "Next" and "Next" again on the page after this one.

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_2.png?raw=true)

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_3.png?raw=true)

 3. Put a name for your project, here we use "JanuaryImport", and click "Finish" :

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_4.png?raw=true)

 4. Now your project is created, you will have a tree like that (if you don't see the project explorer do : ALT+1) :

![Create new project 1]()

## Importing January Library :

Now you need to import January from Maven. To do that, it's really simple, just follow those steps :

  1. Open **File->Project Structure..** :

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_5.png?raw=true)

  2. Now you are in the Project Structure :
      - Click on "Librairies"
      - Click on the green "+" icon on the left
      - Click on "From Maven..."

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_6.png?raw=true)

  3. Now type in the search bar "january", press enter. IntelliJ will search all the results, then select "com.github.yannick-mayeur:org.eclipse.january:2.02"

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_7.png?raw=true)

  Click on "OK" and "OK" a second time and you should have that :

![Create new project 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_8.png?raw=true)

  Just click on "Apply" and then "OK".

  4. Congratulations, January is now imported in your project and you can use it.

## Using BasicExample.java

You have now January and you want to be sure that it's working ?

This is the way to show you how to use January.

  1. Create a new Java File :
    - Right click on the src directory and select **New->Java Class**

![Create new class 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_9.png?raw=true)

  2. Put a name to the class, here "Basic" :

![Create new class 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_10.png?raw=true)

  3. In this file past this code :

  ```java
  public static void main(String[] args) {
        Dataset dataset = DatasetFactory.createFromObject(new double[] { 1,2, 3, 4, 5, 6, 7, 8, 9 });
        // Print the output:
        System.out.println("shape of dataset: " + Arrays.toString(dataset.getShape()));
        System.out.println("toString of dataset: " + dataset.toString());
        System.out.println("toString, with data, of dataset: \n" + dataset.toString(true));
    }
   ```

   Like that :

![Create new class 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_11.png?raw=true)

  4. Import the dependencies :

In IntelliJ to import a class, you just need to put your cursor on the required class and press "Alt+Enter" :

![Create new class 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_12.png?raw=true)

  5. Run the code :
    - Right-click on the Basic.java
    - Select "Run 'Basic.main()'"

![Create new class 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_13.png?raw=true)

  6. This code should appear :

![Create new class 1](https://github.com/PierreSachot/JanuaryIntelliJIntegration/blob/master/images/Screenshot_14.png?raw=true)
