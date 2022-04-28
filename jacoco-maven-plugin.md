## jacoco-maven-plugin

```xml
<plugin>
    <groupId>org.jacoco</groupId>
    <artifactId>jacoco-maven-plugin</artifactId>
    <version>0.8.5</version>
    <executions>
        <execution>
            <id>report</id>
            <phase>verify</phase>
            <goals>
                <goal>report</goal>
            </goals>
            <configuration>
                <dataFile>${project.build.directory}/coverage-reports/aggregate.exec</dataFile>
                <excludes>
                    <exclude>**/model/**/*.class</exclude>
                    <exclude>**/infrastructure/**/*.class</exclude>
                </excludes>
            </configuration>
        </execution>
    </executions>
</plugin>
```
