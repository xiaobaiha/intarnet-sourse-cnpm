# cnpm 内网源公司部署
[TOC]
## 服务器配置
### 0. 服务器环境要求
- mysql  
创建数据库cnpmdb
- node(4.2.2以上版本)
### 1. 下载项目源码
- 进入项目存放的文件夹
- git clone https://github.com/xiaobaiha/intarnet-sourse-cnpm.git 
- 将 docs/db.sql导入mysql 的cnpmdb数据库中
- 编辑 config/index.js, 找到
> database: {  
    db: 'cnpmdb',  
    username: 'root',  
    password: '123456',  
    ...  
}

将username和password替换为服务器mysql的用户名和密码，保存
### 2. 进行部署
- 进入项目根目录
- npm install
- node dispatch.js启动服务 可以通过127.0.0.1:7002看到内网源的web页面

## 客户端配置
### 0. 客户端环境要求
- npm/node
- cnpm (npm i cnpm -g)
### 1. 配置cnpm内网源
> cnpm config set registry="http://服务器IP:7001"
### 2. 使用cnpm
语法与npm相同
