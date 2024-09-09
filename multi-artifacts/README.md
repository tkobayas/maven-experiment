You can experiment `mvn deploy` with local Nexus.

e.g.
```shell
mvn -s ./settings.xml -fae -ntp -Dfull clean deploy -DdeployAtEnd -DretryFailedDeploymentCount=3  -Dfull -Dmaven.test.failure.ignore=true -DskipTests=false
```

or

```shell
mvn -s ./settings.xml -fae -ntp -Dfull clean deploy -DdeployAtEnd -DretryFailedDeploymentCount=3  -Dfull -Dmaven.test.failure.ignore=true -DskipTests=false -Daether.connector.basic.parallelPut=false
```