### <img src="src/docs/asciidoc/images/spring-framework.png" width="80" height="80">Spring 5.2.x 源码编译&分析

- 通过`git`下载spring的源码，这边下载的是5.2.x版本

  ```bash
  git clone -b 5.2.x https://github.com/spring-projects/spring-framework.git
  ```

- 在源码根目录，spring-framework/，打开命令行窗口，执行下面命令。然后等待`BUILD SUCCESS`字样的提示，能看到说明编译成功

  ```bash
  gradlew :spring-oxm:compileTestJava
  ```

- 然后就可以用idea导入spring-framework工程。

**可能出现的问题（也许有也许没有！！）：**

- 如果在编译过程中遇到`exception during working with external system: java.lang.AssertionError
  `，那么需要修改`/spring-framework/gradle/wrapper/gradle-wrapper.properties`：

```properties
distributionBase=GRADLE_USER_HOME
distributionPath=wrapper/dists
## 替换成5.x版本
distributionUrl=https\://services.gradle.org/distributions/gradle-5.5.1-all.zip
zipStoreBase=GRADLE_USER_HOME
zipStorePath=wrapper/dists

```
