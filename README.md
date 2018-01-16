# maven-archetype-tutorial
Simple tutorial explaining how to use Maven and Archetypes generation

                
1. Create archetype. (Run it on your project folder)
```bash
	mvn archetype:create-from-project
```

2. Add the new archetype to the local catalog.
```bash
	cd target\generated-sources\archetype
	mvn install or mvn install archetype:update-local-catalog
```

(Optional) Add the new Catalog in your Eclipse
```
	(Eclipse) Windows > Preference > Maven > Archetypes > (Add Local Catalog...) 
	Eg. C:\Users\Agostta\.m2\repository\archetype-catalog.xml
```

3. Generating new project
```bash
	mvn archetype:generate 
		"-DarchetypeGroupId=com.example.springboot.camel" 
		"-DarchetypeArtifactId=spring-boot-camel-archetype" 
		"-DgroupId=com.foo.bar" "-DartifactId=my-project-name" 
		"-Dpackage=com.foo.bar" "-DinteractiveMode=false"
```
	                
