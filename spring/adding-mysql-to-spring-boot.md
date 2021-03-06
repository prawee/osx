# How to adding MySQL to Spring boot

## update POM

1. go to https://mvnrepository.com
2. find by "mysql connector"
3. click on MySQL Connector/J
4. choose lasted version 
5. copy code from maven tab

```bash
<!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
<dependency>
    <groupId>mysql</groupId>
    <artifactId>mysql-connector-java</artifactId>
    <version>8.0.15</version>
</dependency>
```

6.Open pom.xml on your project and add this code to dependencies path

```bash
...
<dependencies>
    ...
    <!-- https://mvnrepository.com/artifact/mysql/mysql-connector-java -->
    <dependency>
        <groupId>mysql</groupId>
        <artifactId>mysql-connector-java</artifactId>
        <version>8.0.15</version>
    </dependency>
    ...
</dependencies>
...
```

## Configure

### src/main/resources/application.properties

```bash
spring.datasource.username={username-of-mysql}
spring.datasource.password={password-of-mysql}
spring.datasource.url=jdbc:mysql://localhost:3306/{db-name}
spring.jpa.hibernate.ddl-auto=update
```
