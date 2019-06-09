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

## Layout

- https://github.com/ultraq/thymeleaf-layout-dialect
- https://qiita.com/t-iguchi/items/7d52141fd0ddda0657e6#thymeleaf3%E3%81%AB%E3%81%AA%E3%81%A3%E3%81%A6%E5%A4%89%E3%82%8F%E3%81%A3%E3%81%A6%E3%81%84%E3%82%8B%E3%82%88%E3%81%86%E3%81%AA%E3%81%AE%E3%81%A7%E6%9B%B8%E3%81%8D%E7%9B%B4%E3%81%97%E3%81%BE%E3%81%97%E3%81%9F
