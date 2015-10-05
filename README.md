# maven-repo
构建nexus仓库，存放自己开发的第三方Jar包。

<p>添加依赖的仓库地址：</p>
```xml
<repositories>
    <repository>
        <id>glamey-maven-repository</id>
        <url>https://raw.githubusercontent.com/glameyzhou/maven-repo/master/repository</url>
    </repository>
</repositories>
```
<p>本地发布jar使用下边的命令
```
mvn deploy -DskipTests=true -DaltDeploymentRepository=zhouyang-maven-repo::default::file:/Users/zhouyangzhou/work/maven-repo/repository
```
