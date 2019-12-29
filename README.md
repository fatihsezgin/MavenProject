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


For plugin, an maven project was created and pom.xml file is edited by;
```html

<groupId>org.example</groupId>
  <artifactId>MavenPlugin</artifactId>
  <packaging>maven-plugin</packaging>
  <version>1.0-SNAPSHOT</version>
  <build>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-compiler-plugin</artifactId>
        <configuration>
          <source>8</source>
          <target>8</target>
        </configuration>
      </plugin>
    </plugins>
  </build>
  <name>MavenPlugin Maven Mojo</name>
  <url>http://maven.apache.org</url>

    <dependencies>
      <dependency>
        <groupId>org.apache.maven</groupId>
        <artifactId>maven-plugin-api</artifactId>
        <version>3.0</version>
      </dependency>

      <!-- dependencies to annotations -->
      <dependency>
        <groupId>org.apache.maven.plugin-tools</groupId>
        <artifactId>maven-plugin-annotations</artifactId>
        <version>3.4</version>
        <scope>provided</scope>
      </dependency>
    </dependencies>

```
After that as I mentioned above, we need to add the plugin to your local repository by, 
`$ mvn install`

After that you can use the plugin with adding the groupId, artifactId, version to the pom.xml.
```html
    <groupId>org.example</groupId>
    <artifactId>MavenPlugin</artifactId>
    <version>1.0-SNAPSHOT</version>
```

Finally you can see the output of the plugin just type in the project directory
`$mvn org.example:MavenPlugin:1.0-SNAPSHOT:getCompileDate`
