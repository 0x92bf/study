#安装
* [下载地址](https://docs.mongodb.com/manual/tutorial/install-mongodb-enterprise-on-windows/)
##windows 下部署
* bin目录加入环境变量
* mkdir c:\data\db
* mkdir c:\data\log
* 创建一个配置文件位于 C:\mongodb\mongod.cfg，其中指定 systemLog.path 和 storage.dbPath。具体配置内容如下：\
`systemLog:
     destination: file
     path: c:\data\log\mongod.log
 storage:
     dbPath: c:\data\db`
 * 通过执行mongod.exe，使用--install选项来安装服务，使用--config选项来指定之前创建的配置文件。
 `"C:\mongodb\bin\mongod.exe" --config "C:\mongodb\mongod.cfg" --install`
 
 ##运行
 启动MongoDB服务  `net start MongoDB`\
 关闭MongoDB服务  `net stop MongoDB`\
 移除MongoDB服务  `"C:\mongodb\bin\mongod.exe" --remove`