

# JDBC関連

```
compile('org.springframework.boot:spring-boot-starter-jooq')
```

↑のようにJDBC関連の依存を入れた場合は、DataSourceがないとアプリケーションが起動しない
https://docs.spring.io/spring-boot/docs/2.1.4.RELEASE/reference/html/boot-features-sql.html#boot-features-connect-to-production-database

```
***************************
APPLICATION FAILED TO START
***************************

Description:

Failed to configure a DataSource: 'url' attribute is not specified and no embedded datasource could be configured.

Reason: Failed to determine a suitable driver class


Action:

Consider the following:
        If you want an embedded database (H2, HSQL or Derby), please put it on the classpath.
        If you have database settings to be loaded from a particular profile you may need to activate it (no profiles are currently active).
```
