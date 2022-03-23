# maven-plugins
Maven useful plugins 


## maven-compiler-plugin
```xml 
<!-- Set a JDK compiler level -->
			<plugin>
				<groupId>org.apache.maven.plugins</groupId>
				<artifactId>maven-compiler-plugin</artifactId>
				<version>3.10.1</version>
				<configuration>
					<source>11</source>
					<target>11</target>
					<encoding>UTF-8</encoding>
				</configuration>
			</plugin>
```

## maven-jar-plugin
```xml
<!--  to stop default jar generation-->
			<plugin>
				<artifactId>maven-jar-plugin</artifactId>
				<version>3.2.2</version>
				<executions>
					<execution>
						<id>default-jar</id>
						<phase>none</phase>
					</execution>
				</executions>
			</plugin>
```

##
```xml
<!-- to create executable jar -->
			<plugin>
				<artifactId>maven-assembly-plugin</artifactId>
				<configuration>
					<archive>
						<manifest>
							<mainClass>com.demo.App</mainClass>
						</manifest>
					</archive>
					<descriptorRefs>
						<descriptorRef>jar-with-dependencies</descriptorRef>
					</descriptorRefs>
					<finalName>demo-app</finalName>
					<appendAssemblyId>false</appendAssemblyId>
				</configuration>
				<executions>
					<execution>
						<id>make-assembly</id> <!-- this is used for inheritance merges -->
						<phase>package</phase> <!-- bind to the packaging phase -->
						<goals>
							<goal>single</goal>
						</goals>
					</execution>
				</executions>
			</plugin>
```
