# IntelliJ IDEA 中的 Maven 项目初体验及搭建 Spring MVC 框架

在「[详述 IntelliJ IDEA 创建 Maven 项目及设置 java 源目录的方法](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/articles/basic-course/maven-project.md)」一文中，我们已经将 IntelliJ IDEA 中的 Maven 项目的框架搭建完成。接着上文，在本文中，我们更近一步，利用 Tomcat 运行我们的 Web 项目。

![gitcode-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/gitcode-project.png)

如上图所示，我们进一步扩展了项目的结构，在`java`目录下新建了一系列的目录层级，并在`annotation`目录下建立一个名为`AnnotationController`的 Java 类，用于测试 Spring MVC 框架；在`WEB-INF`目录下，新建了一个`pages`目录，用于存放`jsp`页面，并新建了一个名为`springmvc-servlet.xml`的文件，用于书写 Spring MVC 框架的配置项。接下来，我们依次看看这些文件的内容：

- 控制类：`AnnotationController`

```
package com.hit.action.demo.annotation;

import org.springframework.stereotype.Controller;
import org.springframework.web.bind.annotation.RequestMapping;
import org.springframework.web.bind.annotation.ResponseBody;
import org.springframework.web.servlet.ModelAndView;

import javax.servlet.http.HttpServletRequest;

/**
 * author:Charies Gavin
 * https:github.com/guobinhit
 */
@Controller
public class AnnotationController {

    // 请求映射地址 http://localhost:8080/gitcode/test，其中 8080 为默认端口
    @RequestMapping(value = "/test")
    public String goTest(HttpServletRequest request) {
        // 输出请求 URL 路径
        System.out.println(request.getRequestURL());
        // 返回逻辑名
        return "index";
    }
}
```

- Spring MVC 配置文件：`springmvc-servlet.xml`

```
<?xml version="1.0" encoding="UTF-8"?>
<beans xmlns="http://www.springframework.org/schema/beans"
       xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
       xmlns:mvc="http://www.springframework.org/schema/mvc"
       xmlns:context="http://www.springframework.org/schema/context"
       xsi:schemaLocation="http://www.springframework.org/schema/beans
                        http://www.springframework.org/schema/beans/spring-beans-3.2.xsd
                        http://www.springframework.org/schema/mvc
                        http://www.springframework.org/schema/mvc/spring-mvc-3.2.xsd
                        http://www.springframework.org/schema/context
                        http://www.springframework.org/schema/context/spring-context-3.2.xsd ">

    <!-- 声明注解开发方式 -->
    <mvc:annotation-driven/>

    <!-- 包自动扫描 -->
    <context:component-scan base-package="com.hit.action"/>

    <!-- 内部资源视图解析器，前缀 + 逻辑名 + 后缀 -->
    <bean class="org.springframework.web.servlet.view.InternalResourceViewResolver">
        <property name="prefix" value="/WEB-INF/pages/"/>
        <property name="suffix" value=".jsp"/>
    </bean>
</beans>
```

- 全局配置文件：`web.xml`

```
<!DOCTYPE web-app PUBLIC
 "-//Sun Microsystems, Inc.//DTD Web Application 2.3//EN"
 "http://java.sun.com/dtd/web-app_2_3.dtd" >

<web-app version="2.5" xmlns="http://java.sun.com/xml/ns/javaee"
         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://java.sun.com/xml/ns/javaee
         http://java.sun.com/xml/ns/javaee/web-app_2_5.xsd">

    <!-- 如果修改 Spring 配置文件的位置和名称，则通过以下方式进行声明全局配置文件 -->
    <context-param>
        <param-name>contextConfigLocation</param-name>
        <param-value>/WEB-INF/springmvc-servlet.xml</param-value>
    </context-param>

    <!-- 配置 Spring 监听器 -->
    <listener>
        <listener-class>org.springframework.web.context.ContextLoaderListener</listener-class>
    </listener>

    <!-- 配置 DispatcherServlet 对 url 进行过滤 -->
    <servlet>
        <servlet-name>springmvc</servlet-name>
        <servlet-class>org.springframework.web.servlet.DispatcherServlet</servlet-class>

        <!-- 显示配置用于解析 DispatcherServlet 的配置文件 -->
        <!-- 如果不显示指定，则 Spring MVC 会自动扫描 WEB-INF 下以 servlet-name 标签声明的名称开头以 servlet 结尾的配置文件 -->
        <init-param>
            <param-name>contextConfigLocation</param-name>
            <param-value>/WEB-INF/springmvc-servlet.xml</param-value>
        </init-param>
        <!-- 显示指定加载顺序-->
        <load-on-startup>1</load-on-startup>
    </servlet>
    <servlet-mapping>
        <servlet-name>springmvc</servlet-name>
        <!-- 如果声明 /* 则会拦截所有请求，包括 action 返回的 .jsp 页面 -->
        <url-pattern>/</url-pattern>
    </servlet-mapping>

    <!-- 配置欢迎页 -->
    <welcome-file-list>
        <welcome-file>index.jsp</welcome-file>
    </welcome-file-list>
</web-app>
```

如上述代码以配置文件所示，我们对 Spring MVC 框架进行了简单的配置，其中有两点需要我们特别注意，分别是：

- 配置文件，如果不显示指定，则 Spring MVC 会自动扫描`WEB-INF`下以`servlet-name`标签声明的名称开头以`servlet`结尾的配置文件；
- 拦截请求，如果声明`/*`则会拦截所有请求，包括 action 返回的`.jsp`页面，因此一般声明`/`即可，可以防止请求重复拦截。

此外，因为我们这是 Maven 项目，自然不需要我们再手动导入`jar`啦，只需要在`pom.xml`文件中配置依赖即可：

```
<?xml version="1.0" encoding="UTF-8"?>

<project xmlns="http://maven.apache.org/POM/4.0.0" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
         xsi:schemaLocation="http://maven.apache.org/POM/4.0.0 http://maven.apache.org/xsd/maven-4.0.0.xsd">
    <modelVersion>4.0.0</modelVersion>

    <groupId>com.hit</groupId>
    <artifactId>gitcode</artifactId>
    <version>1.0-SNAPSHOT</version>
    <packaging>war</packaging>

    <dependencies>
        <dependency>
            <groupId>junit</groupId>
            <artifactId>junit</artifactId>
            <version>4.10</version>
            <scope>test</scope>
        </dependency>

        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-web</artifactId>
            <version>RELEASE</version>
        </dependency>

        <dependency>
            <groupId>org.springframework</groupId>
            <artifactId>spring-webmvc</artifactId>
            <version>RELEASE</version>
        </dependency>
    </dependencies>
</project>
```

接下来，配置 Tomcat，运行 Web  项目：

![configuration-tomcat](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/configuration-tomcat.png)

![configuration-tomcat-2](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/configuration-tomcat-2.png)

如上图所示，依次对 Tomcat 进行配置，完成后，运行项目：

![run-project](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/run-project.png)

如上图所示，项目成功运行。在这里，很多同学可能会遇到如下错误：

![http-status-500](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/http-status-500.png)

造成上述错误的原因是`jar`包冲突，一般是`servlet-api.jar`和`jsp-api.jar`这个两个`jar`包冲突导致的。至于为什么会出现`jar`包冲突，很有可能是在写`Controller`的时候，需要导入`javax.servlet.http.HttpServletRequest`，这时看到项目中竟然没有引入该`jar`，自然是顺手就在`pom.xml`中添加了该`jar`的依赖，好吧，冲突种子就在这里种下啦！实际上，在 Tomcat 的`lib`目录中，已经包含上述两个`jar`包：

![tomcat-lib-ls](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/tomcat-lib-ls.png)

**解决方法**：如果是 Maven 项目，就删除`pom.xml`文件中对`servlet-api.jar`和`jsp-api.jar`的依赖；如果是非 Maven 项目，就手动排除这两个`jar`包。然后，进入 IntelliJ IDEA  的`Project Structure -> Modules -> Dependencies`配置页：

![modules-dependencies](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/images/basic-course/run-maven-springmvc/modules-dependencies.png)

如上图所示，检查 Tomcat 是否引入；如果引入，则检查是否勾选 Tomcat 前的`Export`选项，实际上不勾选这个选项是正确的，勾选`Export`之后，会在项目启动后，将该 Tomcat 导出到本地仓库，从而导致两份 Tomcat，再次产生`jar`包冲突。除此之外，还要检查 JDK、Tomcat 以及 Maven 的版本，以防止版本不兼容的问题，例如：

- `Maven 3.3.1`及以上的版本需要`JDK 1.7`及以上的版本；
- `Spring 4`需要`JDK 1.7`以上的版本等。

如果还解决不了问题的话，呃，再检查检查  IntelliJ IDEA  的 Java 编译器的版本吧，囧！



----------
———— ☆☆☆ —— [返回 -> 史上最简单的 IntelliJ IDEA 教程 <- 目录](https://github.com/guobinhit/intellij-idea-tutorial/blob/master/README.md) —— ☆☆☆ ————
