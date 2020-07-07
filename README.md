## Spug



Spug是一款使用Python+Flask+Vue+Element组件开发的开源运维管理系统,系统前后端分离,帮助中小型企业完成主机、任务、发布部署、配置文件、监控、报警等管理。


### Feature 功能
----------------------------
  - CMDB 资产管理
  - Task 任务计划管理
  - CI/CD 部署、发布管理
  - Config File 配置文件管理
  - Monitor 监控(未完成）
  - Alarm  报警（未完成）


### Environment 环境
----------------------------
   * Python 3.x
   * Flask 1.0.x
   * Node 6.x
   * Element 2.x


### 快速启动
----------------------------
```
$ docker pull reg.qiniu.com/openspug/spug
$ docker run -d -p 80:80 reg.qiniu.com/openspug/spug

$ 访问：http://主机ip
$ 默认账号密码：admin/spug

# 可选参数：
$ docker run -d -e REGISTRY_SERVER="hub.qbangmang.com" -p 80:80 reg.qiniu.com/openspug/spug

$ -e MYSQL_HOST = "192.168.1.10"              // 指定数据库地址
  -e MYSQL_DATABASE="spug"                    // 指定数据库名称，
  -e MYSQL_USER="spuguser"                    // 指定数据库用户名
  -e MYSQL_PASSWORD="spugpwd"                 // 指定数据库密码
  -e MYSQL_PORT="3306"                        // 指定数据库端口

  -e REGISTRY_SERVER="hub.qbangmang.com"      // 指定私有镜像仓库
  -e REGISTRY_USER="hubuser"                  // 指定私有镜像仓库用户名
  -e REGISTRY_PASSWORD="hubpwd"               // 指定私有镜像仓库密码
```

更多Dockerfile [Dockerfile](https://github.com/openspug/spug/tree/master/docs/Dockerfile)


### 详细安装步骤
----------------------------

    [文档](https://github.com/openspug/spug/wiki/)


### Development 开发
----------------------------
```
   1. Clone code 克隆代码：
   $ git clone https://github.com/openspug/spug.git

   2. Start server 启动服务端：
   $ cd spug/spug_api
   $ pip install -r requirements.txt  //安装依赖包
   $ mv config.py.example config.py   //编辑配置文件
   $ python manage.py init_db         //初始化数据库
   $ python manage.py create_admin    //创建管理员
   $ python main.py                   //启动服务

   3. Start web  启动前端：
   $ cd spug/spug_web
   $ npm install
   $ npm run dev

   4. Visit 访问：
   $ http://$HOST:8080 (http://你的主机IP:8080 来访问 Spug)

```

### 前端单独使用
----------------------------
**Spug项目前后端分离，支持前端单独运行，也支持后端单独运行。


### Preview 预览
----------------------------
![image](http://image.qbangmang.com/login.gif)
![image](http://image.qbangmang.com/user.gif)
![image](http://image.qbangmang.com/host.gif)
![image](http://image.qbangmang.com/publish.gif)
![image](http://image.qbangmang.com/tasks.gif)








