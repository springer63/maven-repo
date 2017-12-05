# maven-repo
maven repo
github maven仓库的使用

因为github使用了raw.githubusercontent.com这个域名用于raw文件下载。所以使用这个maven仓库，只要在pom.xml里增加：

```
<project>
<!--Add repositories-->
 <repositories>
     <repository>
         <id>haoch-maven-snapshot-repository</id>
         <name>haoch-maven-snapshot-repository</name>
         <url>https://raw.github.com/springer63/maven/snapshot/</url>
     </repository>
     <repository>
         <id>haoch-maven-release-repository</id>
         <name>haoch-maven-release-repository</name>
         <url>https://raw.github.com/springer63/maven/release/</url>
     </repository>
 </repositories>
<!-- Add dependencies -->
 <dependencies>
     <dependency>
         <artifactId>${artifactId}</artifactId>
         <groupId>com.github.${github_account}</groupId>
         <version>${version}</version>
     </dependency>
 </dependencies>
</project>
```

