# Automatisation de test avec Console Luncher



Cloner le projet :
```
git clone https://github.com/moss-n/junit-automation.git
```

Télécharger Console Luncher: [click-me](https://repo1.maven.org/maven2/org/junit/platform/junit-platform-console-standalone/1.7.0/`)




```
$ ls
junit-automation  junit-platform-console-standalone-1.7.0-all.jar`



cd junit-automation/
junit-automation$ mkdir junit-automation/lib
junit-automation$ ls junit-automation/
Jenkinsfile  lib  README.md  src

```
Placer le jar dans un répertoire lib dans votre projet
```
$ cp junit-platform-console-standalone-1.7.0-all.jar  junit-automation/lib
$ ls junit-automation/lib
junit-platform-console-standalone-1.7.0-all.jar
```
En mode console, placez-vous sous le répertoire jiunit-automation, et compiler
votre projet
```
$ cd junit-automation/
junit-automation$ cd src/
junit-automation/src$ javac -cp "../lib/junit-platform-console-standalone-1.7.0-all.jar" Car.java App.java CarTest.java 
junit-automation/src$ java -jar "../lib/junit-platform-console-standalone-1.7.0-all.jar" -cp "." --select-class CarTest --reports-dir='rep



nano CarTest.java
```
:![CarTest.java - test sur le constructeur echoué](/vue1.png)
CarTest.java - test sur le constructeur echoué
``` 
junit-automation/src$ javac -cp "../lib/junit-platform-console-standalone-1.7.0-all.jar" Car.java App.java CarTest.java 

junit-automation/src$ java -jar "../lib/junit-platform-console-standalone-1.7.0-all.jar" -cp "." --select-class CarTest --reports-dir='rep
```
CarTest.java - test sur le constructeur réussi après modification de la methode de test
:![CarTest.java - test sur le constructeur réussi](/vue2.png)