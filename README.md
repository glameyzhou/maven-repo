# maven-repo，自定义的基于github网站的免费nexus
构建nexus仓库，存放自己开发的第三方Jar包。

<p>添加依赖的仓库地址：</p>
```xml
<repositories>
    <repository>
        <id>zhouyang-maven-repo</id>
        <url>https://raw.githubusercontent.com/glameyzhou/maven-repo/master/repository</url>
    </repository>
</repositories>
```
<p>将jar发布到本地maven仓库中</p>
```
mvn deploy -DskipTest=true -DaltDeploymentRepository=zhouyang-maven-repo::default::file:/Users/zhouyangzhou/work/maven-repo/repository
```
