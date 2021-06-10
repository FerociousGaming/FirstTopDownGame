# FirstTopDownGame #

Ess Get eet
## For Development: ##
### Explanation ###
The architecture of this app is Maven. Maven helps with dependencies, testing, and creating a .jar file. 
As well, Maven works well with SonarCloud, which will scan our code for vulnerabilities.

### Adding outside dependencies ###
This is for when we add imports that have to be installed. When that's the case, we need to change the pom.xml
* For example, the following is only 1 dependency: junit.
    * You have to figure out what the proper groupId, artifactId, and version are
    * the scope is for what our project uses it for (junit is for unit tests only).

```
<dependencies>
    <dependency>
        <groupId>junit</groupId>
        <artifactId>junit</artifactId>
        <version>4.13.1</version>
        <scope>test</scope>
    </dependency>
</dependencies>
```

### Useful CLI commands: ###
_This should be in the repository folder_
* mvn clean
    * removes the /target folder. Note that each of the following includes this to ensure new files.
    * _mvm stands for maven_
* mvn clean test
    * Runs the junit tests. Note that this is done before creating the jar anyway
* mvn clean package
    * Generates jar file for distribution

### Testing the project/jar file: ###
* Just run the code in 'debug mode' like a normal person would
* If a GUI-only project, you can just double click the generated .jar file
* If that doesn't work, double click the runApp.bat file.
    * This just runs (from the command line) whatever .jar file is in the /target folder

### Checking bugs, vulnerabilities, and code smells ###
SonarCloud: https://sonarcloud.io/dashboard?id=FerociousGaming_FirstTopDownGame

<br>
<br>

## Resources that I used to create this: ##
https://maven.apache.org/guides/getting-started/index.html

https://maven.apache.org/guides/getting-started/maven-in-five-minutes.html

https://blog.danskingdom.com/allow-others-to-run-your-powershell-scripts-from-a-batch-file-they-will-love-you-for-it/
