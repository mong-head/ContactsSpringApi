# Contacts API

* 설정
  * pom.xml
    * dependencies
      * spring context, web-mvc, web
      * DB : spring-jdbc, mybatis, mybatis-spring, commons-dbcp, postgresql (관련 설정 : `context-datasource.xml`)
  * web.xml
    * listener 설정
      * listener path 설정 : `spring/context-*.xml` (src/main/resources/spring/ 에 위치함)
    * servlet 설정
      * servlet name 설정 : dispatcher
      * servlet path 설정 : `/WEB-INF/dispatcher-servlet.xml`
  * listener(application context 관련 설정) (src/main/resources/spring/ 에 위치함)
    * `context-common.xml` : component scan 설정 (repository, service, controller annotation 설정)
    * `context-datasource.xml` : datasource 설정 (jdbc, db name, db password등)
    * `context-mapper.xml` : 