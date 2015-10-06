# 自定义的基于github网站的免费nexus
构建nexus仓库，存放自己开发的第三方Jar包。
***
### 发布jar到github流程
#####   本地代码开发，这个大家都懂的。
#####   将项目编译deploy到maven-repo项目的指定目录中，通过下边的命令执行:
```
mvn deploy -DskipTest=true -DaltDeploymentRepository=zhouyang-maven-repo::default::file:/Users/zhouyangzhou/work/maven-repo/repository
```
#####   将代码提交到github，大功告成。
***
*下边是github对外的仓库地址*
```xml
<repositories>
    <repository>
        <id>zhouyang-maven-repo</id>
        <url>https://raw.githubusercontent.com/glameyzhou/maven-repo/master/repository</url>
    </repository>
</repositories>
```
***
### 当前支持的jar
##### 公用的第三方类库版本控制（通过pom继承的方式实现）
```xml
  <parent>
    <groupId>org.glamey</groupId>
    <artifactId>super-pom</artifactId>
    <version>1.0.1</version>
  </parent>
```
##### 开发工具脚手架（工具类）
```xml
    <dependency>
      <groupId>org.glamey</groupId>
      <artifactId>scaffold</artifactId>
      <version>1.0.1</version>
    </dependency>
```
***
