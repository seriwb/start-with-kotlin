# datasouce

JDBC系の依存を追加した場合は、application.propertiesにdatasourceの記述を追加しないといけない

```java
spring.datasource.url=
spring.datasource.username=
spring.datasource.password=
spring.datasource.driver-class-name=
```

DBの設定を書いたクラスを@Configurationで依存性を追加してあげれば、
プレフィックスを別のものにもできる。


https://qiita.com/syukai/items/0d4bf27f82fef9965cdd