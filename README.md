# MavenProject

For this project we create a jar file within the class that about parsing mathematical equations written by Mehmetcan Olgun.

Firstly, to create a jar file a maven project created and groupId, artifactId, version and packaging is declared by;

```html
    <groupId>edu.advanced</groupId>
    <artifactId>MavenProject</artifactId>
    <version>1.0-SNAPSHOT</version>
    <packaging>jar</packaging>
```

after that run this command
` $ mvn install`

it will create a jar file to the path of your local maven repository.
That means you can simply add this jar to your project with writing this 
```html

    <groupId>edu.advanced</groupId>
    <artifactId>MavenProject</artifactId>
    <version>1.0-SNAPSHOT</version>        
```
in which project you want to use.


For the plugin 

