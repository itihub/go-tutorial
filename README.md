## GO tutorial 实践   

## 工程目录  

| Dir | tutorial link |  
| --- | --- |
| getting-started | https://golang.org/doc/tutorial/getting-started.html |    
| create-module | https://golang.org/doc/tutorial/create-module.html |  

## 总结  
### go module  
启动代码依赖跟踪```go mod init example.com/greetings```  
使用本地模块```go mod edit -replace example.com/greetings=../greetings```  
添加模块的依赖```go mod tidy```     

### 测试 
使用命令行运行测试```go test```  
使用命令行运行测试并详细输出```go test -v```  

### 本地编译与安装  
```go build```编译包及其依赖项，但不进行安装  
```go install```编译并安装软件包  

实践将代码进行编译以及本地安装  
1. 进入```hello\```目录下进行代码编译```go build```
2. 尝试运行编译后的可执行文件```hello.exe```  
3. 获取GO安装路径```go list -f '{{.Target}}'```  
4. Go 安装目录添加到系统环境变量中```set PATH=%PATH%;C:\path\to\your\install\directory```（当前会话有效）   
5. (4)代替方案，通过```GOBIN```方式 ```go env -w GOBIN=C:\path\to\your\bin```   
6. 进行安装```go install```  
7. 测试键入安装包的名称直接运行程序```hello```  
