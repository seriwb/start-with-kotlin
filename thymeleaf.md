# LiveReload関係

application-dev.ymlに以下を追加

```yml
spring:
  # Templates reloading during development
  thymeleaf:
    prefix: file:src/main/resources/templates/
    cache: false

  # Static resources reloading during development
  resources:
    static-locations: file:src/main/resources/static/
    cache:
      period: 0
```

build.gradleに以下を追加

```groovy
// LiveReload用
bootRun {
    sourceResources sourceSets.main
}
```


https://docs.spring.io/spring-boot/docs/2.0.0.M3//gradle-plugin/reference/html/#running-your-application-reloading-resources

- https://attacomsian.com/blog/spring-boot-auto-reload-thymeleaf-templates
- http://blog.enjoyxstudy.com/entry/2017/01/08/000000
- https://docs.spring.io/spring-boot/docs/current/reference/html/using-boot-devtools.html#using-boot-devtools-livereload
- https://stackoverflow.com/questions/38018575/error-module-not-specified-intellij-idea



# レスポンス関係

データの渡し方
- https://github.com/thymeleaf/thymeleaf-spring/issues/141


# テンプレートの書き方
- https://morizyun.github.io/java/library-thymeleaf.html
- https://qiita.com/rubytomato@github/items/ac65c2203d16d1a1bbd7#%E3%83%AA%E3%83%B3%E3%82%AFurl%E5%BC%8F
- https://qiita.com/NagaokaKenichi/items/c6d1b76090ef5ef39482
- https://qiita.com/opengl-8080/items/eb3bf3b5301bae398cc2
