# A-E-D
v2

1. 需要maven命令行工具

---

2. 依赖atlassian的三个jar包
```
atlassian-extras-api-3.3.0.jar
atlassian-extras-common-3.3.0.jar
atlassian-extras-decoder-api-3.3.0.jar
```
---

3. 用maven命令将三个jar包导入到本地仓库

```
cd ${atlassian-x.x}/app/WEB-INF/lib
mvn install:install-file -Dfile=atlassian-extras-api-3.3.0.jar -DgroupId=com.atlassian.extras -DartifactId=atlassian-extras-api -Dversion=3.3.0 -Dpackaging=jar
mvn install:install-file -Dfile=atlassian-extras-common-3.3.0.jar -DgroupId=com.atlassian.extras -DartifactId=atlassian-extras-common -Dversion=3.3.0 -Dpackaging=jar
mvn install:install-file -Dfile=atlassian-extras-decoder-api-3.3.0.jar -DgroupId=com.atlassian.extras -DartifactId=atlassian-extras-decoder-api -Dversion=3.3.0 -Dpackaging=jar
```
参数 `${atlassian-x.x}` 是下载的atlassian项目路径，请自行替换
参数 `-Dfile` 是jar包位置

---

4. 下载 & 编译项目
4.1 使用ide内部的maven工具进行打包
4.2 使用命令行进行打包 `mvn package`

---

5. 生成 license code
运行 test/java/AtlassianLicenseGenerator 的 main方法