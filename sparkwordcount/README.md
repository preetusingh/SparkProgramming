##Objective: Implementation of WordCount using Spark application with Scala IDE and Maven 

####Download Scala IDE:- 
Scala IDE is an eclipse project which provides a very intuitive development environment for Scala and Spark application. Download Scala IDE and install it.  

####Create a Maven project:-
Maven is a popular package management tool for Java-based languages that allows us to link libraries present in public repositories.We can use Maven itself to build our project, or use other tools like Scala’s sbt tool or Gradle.

1. Go to: File-> New -> Project -> Maven project  and create a maven project.Fill Group Id and Artifact Id & click finish. 
Group Id = org.test and Artifact Id = sparkwordcount

2. Update pom.xml:- Download pom.xml sample and update it in above maven project. It has spark dependency jar entry which will be downloaded while building. 

3. Add Scala Nature to this project :- 
Right click on project -> configure - > Add Scala Nature. 

4. Update Scala compiler version for Spark:- 
Scala IDE by default uses latest version(2.11) of Scala compiler, however Spark uses version 2.10.So we need to update appropriate version for IDE. 
Right click on project- > Go to properties -> Scala compiler -> update Scala installation version to 2.10.5 
  
5. Remove Scala Library Container from build path :- (Optional)
Jars required in already added via spark core(via pom.xml), so multiple jars is not required.
Right click on the project -> Build path -> Configure build path  and remove Scala Library Container.

6. Update source folder src/main/java to src/main/scala (Right click -> Refactor -> Rename  to scala).Now create a package under this name it as com.devinline.spark.

7. Create a Scala object under package created above name it as WordCount.scala
Right click on package -> New -> Scala Object  and add WordCount at the end of Name.

9. Create an input file in project named as Food.txt and enter some words into it. 

10. Execute WordCount program :-  Right click on WordCount.scala - > Run as -> Scala application. It should create an output directory output.txt  and it should contain two file : part-00000 and _SUCCESS.
Sample output is part-00000.
