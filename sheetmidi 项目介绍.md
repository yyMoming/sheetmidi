# sheetmidi 项目介绍

### 1. 基本原理



<img src="D:\Work\demo\sheetmidi\images\step1.png" style="zoom:50%;" />

<img src="D:\Work\demo\sheetmidi\images\step2.png" style="zoom:50%;" />

### 2. 项目目录

.
├── conf
│   ├── aliyunoss.go	//阿里云配置信息
│   ├── conf.go	
│   ├── conf_test.go
│   ├── dirpath.go	//	项目目录的一些配置信息
│   ├── mlog.go		// 	log的配置信息
│   └── mysql.go  	// MySQL连接的配置信息
├── controller
│   ├── controller.go	// 控制器
│   └── controller_test.go
├── database
│   └── initMysql.go	// 数据库初始化
├── go.mod
├── GoSheetMidi
├── go.sum
├── ImageBuffer	//	临时文件保存
├── logs	// 日志保存
│   ├── sheetmidi.log -> sheetmidi.log.2021-11-27 00-00-00.log
│   ├── sheetmidi.log.2021-11-26 00-00-00.log
│   └── sheetmidi.log.2021-11-27 00-00-00.log
├── main.go
├── middleware
│   ├── CheckCommitMiddleware.go	// 检查提交的过程中是否存在覆盖问题
│   └── loggerMiddleware.go	//	日志中间件
├── models
│   ├── client.go	//	与后台算法的连接
│   ├── encode.go	//	文件传输避免分包粘包问题	
│   ├── mmysql.go	//  数据库操作
│   ├── models_test.go	
│   └── oss.go	//  OSS云存储
├── routers
│   └── routers.go	//	路由注册
└── setting	//	暂未配置

### 3. 主要使用的包

- github.com/gin-gonic/gin:	go语言的后端框架


- logrus:	日志记录


- binary：编解码


- github.com/aliyun/aliyun-oss-go-sdk/oss：云存储交互


- crypto/md5：哈希数据

### 4. 基本功能

- [x] 解析视唱图片
- [x] 查看已录入的数据
- [x] 修改已录入的数据

- 解析视唱图片和矫正检测错误

  ![](D:\Work\demo\sheetmidi\images\演示1.png)

- 查看、修改已有记录

![](D:\Work\demo\sheetmidi\images\演示2.png)