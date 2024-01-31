Application Layer
====

- Each layer contains **classes** and **annotations** that have specific responsible.
- One layer can use classes of other layer, but you should not allow circular dependency.

# Application Layers #

![Layered Architecture](layered-architecture.png)

This image was extracted from [Layered Architecture article.](https://herbertograca.com/2017/08/03/layered-architecture/")

## Add decycle

Include [decycle](https://github.com/obecker/decycle) in your application in order to respect layers contraints at your pom.xml.

```xml
    <properties>
        <decycle-maven-plugin.version>0.11.0</decycle-maven-plugin.version>
    </properties>

    <build>
        <pluginManagement>
            <plugins>
                <plugin>
                    <groupId>de.obqo.decycle</groupId>
                    <artifactId>decycle-maven-plugin</artifactId>
                    <version>${decycle-maven-plugin.version}</version>
                    <executions>
                        <execution>
                            <goals>
                                <goal>check</goal>
                            </goals>
                        </execution>
                    </executions>
                    <configuration>
                        <slicings>
                            <slicing>
                                <name>branches</name>
                                <patterns>br.edu.ifrn.conta.*=base, br.edu.ifrn.conta.{*}.**</patterns>
                                <constraints>
                                    <allow>controller, service, domain</allow>
                                    <allow>service, persistence, domain</allow>
                                    <allow>
                                        <one-of>controller, persistence</one-of>
                                    </allow>
                                    <allow>
                                        <one-of>dto, domain</one-of>
                                    </allow>
                                    <allow>
                                        <one-of>restclient, controller</one-of>
                                        <any-of>dto</any-of>
                                    </allow>
                                    <allow>
                                        <one-of>restclient, service</one-of>
                                    </allow>
                                    <allow>
                                        <one-of>restclient, persistence</one-of>
                                        <any-of>util</any-of>
                                    </allow>
                                    <allow>
                                        <one-of>restclient, domain</one-of>
                                    </allow>
                                </constraints>
                            </slicing>
                        </slicings>
                    </configuration>
                </plugin>                
            </plugins>
        </pluginManagement>

        <plugins>
            <plugin>
                <groupId>de.obqo.decycle</groupId>
                <artifactId>decycle-maven-plugin</artifactId>
            </plugin>
        </plugins>
    </build>
```

## Browser api using swagger

1. Build your app

2. Open file at target/site/decycle/main.html

### Hands on with [Conta Example Project.](https://github.com/persapiens/conta)

## :construction_worker: Task

Create one pull request for your project according to [Task Submission Guidelines.](../assessment.md#task-submission)

1. Draw the layers of your application.

2. Describe the layers of your application:
    1. The packages, classes and files of the layer.
    2. The responbility of the layer.
    3. The dependency of other layer of your application.

3. Add decycle or other similar tool and create contraints about your application layer.

4. Ensure that your application respect the constratins of the layours of your applicatoin.

Create a **separate commit** to each subtask.

