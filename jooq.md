# Spring用設定

JOOQをSpringで利用する



3.11からパッケージ名が変わっている
https://www.bunkei-programmer.net/entry/2019/01/28/101443

https://github.com/etiennestuder/gradle-jooq-plugin/issues/97
3.11.11だとコード生成でエラーになる。3.10.9だと大丈夫

## コード生成

https://www.jooq.org/doc/3.11/manual/code-generation/codegen-advanced/codegen-config-database/codegen-database-includes-excludes/

## 書き方

### Join
```java
Result<?> result = create.select()
                         .from(AUTHOR.join(BOOK)
                                     .on(BOOK.AUTHOR_ID.eq(AUTHOR.ID)))
                         .fetch();
```
http://www.jooq.org/doc/3.11/manual/sql-building/sql-statements/select-statement/join-clause/

