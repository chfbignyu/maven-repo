##利用github搭建个人maven仓库 
###1.deploy 到本地 
例如：把项目deply到/home/huff/code/maven-repo/repository目录下 
切换到项目
mvn deploy -DaltDeploymentRepository=huff-mvn-repo::default::file:/project/maven-repo/repository   

###2.把本地目录提交到github上  
把/home/huff/code/maven-repo/repository目录提交到github上  参考：https://github.com/chfbignyu/maven-repo  

###3.配置github地址为仓库地址   
在pom.xml里面增加  
```html
	<repositories>
	    <repository>
	        <id>huff-maven-repo</id>
	        <url>https://raw.githubusercontent.com/chfbignyu/maven-repo/master/repository</url>
	    </repository>
	</repositories>
```
